---
tags:
  - project
  - active
stack:
  - React
  - NestJS
  - MongoDB
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
repos:
  - ~/repos/marco-frontend
  - ~/repos/marco-backend
---

# Marco ERP

Own product. Multi-tenant ERP replacing [[SEM]]. No client yet — potential clients: [[ALUVAL Nicaragua]], [[Vidrieria FMorales]].

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
- [[Marco ERP - Backend]] — repo + code KG
- [[Marco ERP - Frontend]] — repo + code KG
