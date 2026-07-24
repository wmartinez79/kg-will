---
tags:
  - project
  - active
  - repo
stack:
  - NestJS
  - TypeScript
  - MongoDB
  - AWS Lambda
  - SQS
status: in-progress
type: repo
parent: Marco ERP
repo_path: ~/repos/marco-backend
graph_path: ~/repos/marco-backend/graphify-out
remote: git@github.com-wmartinez79:wmartinez79/marco-backend.git
---

# Marco ERP - Backend

Backend repo for [[Marco ERP]]. NestJS API, MongoDB, JWT + `X-Tenant-ID` tenant isolation.

## Repo
- Local path: `~/repos/marco-backend`
- Remote: `git@github.com-wmartinez79:wmartinez79/marco-backend.git`
- Framework: NestJS, TypeScript
- Modules: `api/src/domain/` — auth, tenant, user, roles-permissions, customer, inventory, product-builder, invoice, quote, seller, settings, module-admin
- Lambda workers: `lambda-process-adjustments-bulk`, `lambda-process-initial-inventory`
- Rules: integer cents (no floats), soft delete only, stock changes via `StockWarehouseMasterService.applyDelta`, events only after persistence

## Code Knowledge Graph
This repo has its own `graphify` knowledge graph, separate from this vault's graph.
- Report: `~/repos/marco-backend/graphify-out/GRAPH_REPORT.md`
- Graph data: `~/repos/marco-backend/graphify-out/graph.json`
- Visual explorer: `~/repos/marco-backend/graphify-out/graph.html`
- Snapshot: 2707 nodes · 6955 edges · 145 communities (as of 2026-06-14, commit-dependent — re-run `graphify update .` in-repo after code changes)
- Hub communities: Product Catalog Domain, Inventory Adjustments, JWT Auth Core, Permission System, Role & RBAC, Lambda Workers, Stock Master

## Links
- [[Marco ERP]]
- [[Marco ERP - Frontend]]
