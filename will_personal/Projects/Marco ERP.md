---
tags:
  - project
  - active
stack:
  - React
  - NestJS
  - MongoDB
  - MongoDB Atlas
  - AWS Lambda
  - SQS
  - S3
  - Docker
  - TypeScript
  - TanStack Query
  - Zod
  - Tailwind
  - shadcn/ui
status: in-progress
type: ERP
owner: Will Martinez
potential_clients:
  - Aluval Nicaragua
  - Vidrieria FMorales
  - Taller Instalaciones Martinez
repos:
  - ~/repos/marco-frontend
  - ~/repos/marco-backend
---

# Marco ERP

Own product. Multi-tenant ERP replacing [[SEM]]. No client yet — potential clients: [[ALUVAL Nicaragua]], [[Vidrieria FMorales]], [[Taller Instalaciones Martinez (Client)|Taller Instalaciones Martinez]].

## Summary

Marco ERP is a multi-tenant SaaS-style ERP built to replace [[SEM]], a legacy Visual FoxPro 6 CRM/ERP still running at ALUVAL Nicaragua. One deployment serves multiple tenants, isolated by `X-Tenant-ID` at the API layer and per-tenant RBAC.

Core focus is inventory-driven business operations: tracking stock across warehouses, building sellable products from components, and running the sales cycle (quotes → invoices) against customers. Bulk data operations (initial inventory load, stock adjustments) are offloaded to async Lambda workers via S3/SQS so large CSV imports don't block the API.

Design principles carried through the whole system:
- **Money as integers** — all amounts stored as integer cents, never floats
- **No hard deletes** — every domain entity is soft-deleted
- **Single path for stock changes** — all inventory mutations go through `StockWarehouseMasterService.applyDelta`
- **Events after persistence** — domain events fire only once the underlying write is committed, not before

### Modules
| Module | Purpose |
|---|---|
| **auth** | Login, JWT issuance, session handling |
| **tenant** | Tenant provisioning and management |
| **user** | User accounts within a tenant |
| **roles and permissions** | RBAC — permission keys (`resource.action`) scoped per tenant |
| **customer** | Customer records and related info |
| **inventory** | Stock across warehouses — primary/core module |
| **product-builder** | Configures sellable products from components |
| **invoice** | Invoicing |
| **quote** | Quotes/estimates, feeds into invoicing |
| **seller** | Salesperson records |
| **settings** | Per-tenant configuration |
| **module-admin** | Enable/manage modules per tenant |

## Architecture

```
Client → REST API (NestJS) → MongoDB
Client → REST API → S3 (CSV upload) + SQS → Lambda → MongoDB
```

### Backend ([[Marco ERP - Backend|marco-backend]])
- **Framework:** NestJS, TypeScript
- **Database:** MongoDB with replica set (required for transactions)
- **Auth:** JWT with tenant isolation via `X-Tenant-ID` header
- **RBAC:** Permission keys (`resource.action`) per tenant
- **Lambda workers:** Two SQS-triggered workers for async bulk CSV processing
  - `lambda-process-adjustments-bulk`
  - `lambda-process-initial-inventory`
- **Rules:** Integer cents (no floats), soft delete only, stock changes via `StockWarehouseMasterService.applyDelta`, events only after persistence

### Frontend ([[Marco ERP - Frontend|marco-frontend]])
- **Framework:** React + Vite, TypeScript, Node.js v22
- **State:** TanStack Query for server state
- **Forms:** React Hook Form + Zod
- **UI:** Tailwind CSS v4 + Radix UI + shadcn/ui, lucide-react icons
- **HTTP:** `httpClient` (ky) — auto-attaches `Authorization`, `X-Tenant-ID`, `x-lang`
- **i18n:** i18next with `en.ts` and `es.ts` locale files
- **Testing:** Vitest + Testing Library (unit), MSW (integration), Playwright (e2e)

## Hosting Plan

Target: AWS (Lambda/S3/SQS, already in stack) + MongoDB Atlas.

- **Pre-revenue (now → first paying client):** Atlas M0 (free, 512MB) + AWS free tier (Lambda/S3/SQS/API Gateway) — ~$0/mo. M0 has no replica-set-backed multi-doc transactions, so this tier is dev/demo/pilot only, not production for a paying tenant.
- **Production (once a tenant is paying):** upgrade to Atlas M10 (~$57-75/mo, dedicated, replica set, backups) — funded by that tenant's subscription, not personal capital.
- Sequencing: build and demo on the free tier now, close [[ALUVAL Nicaragua]] first, let their first month(s) of payment cover the M10 upgrade.

## Monetization Plan

Tiered pricing by company size/complexity, not per-seat — ERP value depends on full-company adoption (sales, warehouse, accounting all in one system), so per-user pricing would work against that. Draft 3 tiers:

| Tier | Fits | Included | Differentiator |
|---|---|---|---|
| Starter | Single-location (ALUVAL-size) | 1 warehouse, core modules (inventory, invoice, quote), ~5 users | Entry price, replaces SEM 1:1 |
| Growth | Multi-branch | Multi-warehouse, product-builder module, ~15 users | Adds modules legacy SEM can't do |
| Business | Larger operator | Unlimited warehouses, full module set, advanced RBAC, priority support | For a client bigger than the first two |

Actual price points still need validation against ALUVAL's willingness to pay — anchor is time/error savings over free-but-legacy SEM, not feature count.

### First Two Customers & Grace Periods

Pilot rollout plan, not simultaneous with the Vidrieria FMorales reactivation described above:

| Client | Tier fit | Grace period (free) | Notes |
|---|---|---|---|
| [[ALUVAL Nicaragua]] | Starter | 3-4 months, possibly up to 6 | Has an in-house IT/sysadmin employee (network, systems) — technical gatekeeper for rollout, likely an ally for onboarding/integration questions but also someone who'll evaluate the system critically |
| [[Taller Instalaciones Martinez (Client)\|Taller Instalaciones Martinez]] | Starter | 6-8 months | Brother's aluminum/glass workshop — also Will's rental tenant (separate relationship, see [[Taller Instalaciones Martinez]]) |

Grace periods let both clients migrate off legacy tooling (SEM for ALUVAL, none/manual for Instalaciones Martinez) and validate the product before billing starts — first real revenue funds the Atlas M10 upgrade per the Hosting Plan above.

## Backend Modules (`api/src/domain/`)
- **auth** — authentication
- **tenant** — tenant management
- **user** — user management
- **roles and permssions** — roles and  RBAC permissions
- **customer** — customers and additional information
- **inventory** — inventory management (primary module)
- **product-builder** — product configuration
- **invoice** — invoicing
- **quote** — quotes/estimates
- **seller** — sellers
- **settings** — tenant settings
- **module-admin** — module administration

## People
- William Martinez — Software Architect and Lead developer
## Links
- [[SEM]]
- [[ALUVAL Nicaragua]]
- [[Vidrieria FMorales]]
- [[Taller Instalaciones Martinez (Client)|Taller Instalaciones Martinez]]
- [[Marco ERP - Backend]] — repo + code KG
- [[Marco ERP - Frontend]] — repo + code KG
