# Graph Report - kg-will  (2026-07-26)

## Corpus Check
- 52 files · ~7,258 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 298 nodes · 402 edges · 29 communities (20 shown, 9 thin omitted)
- Extraction: 94% EXTRACTED · 5% INFERRED · 0% AMBIGUOUS · INFERRED: 21 edges (avg confidence: 0.84)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `4fac2788`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- [[_COMMUNITY_Resume & Skills|Resume & Skills]]
- [[_COMMUNITY_Income, Clients & July Bills|Income, Clients & July Bills]]
- [[_COMMUNITY_Debts, Loans & Credit Cards|Debts, Loans & Credit Cards]]
- [[_COMMUNITY_Marco ERP & SEM Projects|Marco ERP & SEM Projects]]
- [[_COMMUNITY_Pluto TV Org & Contacts|Pluto TV Org & Contacts]]
- [[_COMMUNITY_Obsidian App Config|Obsidian App Config]]
- [[_COMMUNITY_Work Experience Roles|Work Experience Roles]]
- [[_COMMUNITY_In All Media Client|In All Media Client]]
- [[_COMMUNITY_Repo Documentation (CLAUDE.md)|Repo Documentation (CLAUDE.md)]]
- [[_COMMUNITY_Marco ERP Backend Repo|Marco ERP Backend Repo]]
- [[_COMMUNITY_Marco ERP Frontend Repo|Marco ERP Frontend Repo]]
- [[_COMMUNITY_Sales Sling Elastic Beanstalk|Sales Sling Elastic Beanstalk]]
- [[_COMMUNITY_Sales Sling Lambda|Sales Sling Lambda]]
- [[_COMMUNITY_Freelance Work Mode|Freelance Work Mode]]
- [[_COMMUNITY_Queso CRM Project|Queso CRM Project]]
- [[_COMMUNITY_Contractor Work Mode|Contractor Work Mode]]
- [[_COMMUNITY_Contact Jimmy Valverde|Contact: Jimmy Valverde]]
- [[_COMMUNITY_Contact Mike Gazlay|Contact: Mike Gazlay]]
- [[_COMMUNITY_Obsidian App Settings|Obsidian App Settings]]
- [[_COMMUNITY_Bill Inbox Template|Bill Inbox Template]]
- [[_COMMUNITY_Community 20|Community 20]]
- [[_COMMUNITY_Community 21|Community 21]]
- [[_COMMUNITY_Community 22|Community 22]]
- [[_COMMUNITY_Community 23|Community 23]]
- [[_COMMUNITY_Community 24|Community 24]]
- [[_COMMUNITY_Community 25|Community 25]]
- [[_COMMUNITY_Community 26|Community 26]]
- [[_COMMUNITY_Community 27|Community 27]]

## God Nodes (most connected - your core abstractions)
1. `William Donald Martínez Avellan` - 39 edges
2. `Finance Overview` - 19 edges
3. `Marco ERP` - 14 edges
4. `In All Media` - 14 edges
5. `SEM` - 13 edges
6. `Will` - 13 edges
7. `Pluto TV / Paramount` - 11 edges
8. `In All Media` - 10 edges
9. `Payment History` - 9 edges
10. `Experience` - 9 edges

## Surprising Connections (you probably didn't know these)
- `Enhancement Payment System` --semantically_similar_to--> `Pluto TV / Paramount`  [INFERRED] [semantically similar]
  Resume.md → will_personal/Companies/Pluto TV Paramount.md
- `Finance Overview` --semantically_similar_to--> `Resume`  [INFERRED] [semantically similar]
  will_personal/Finance Overview.md → will_personal/Resume.md
- `William Donald Martínez Avellan` --references--> `Banex / Findesa`  [EXTRACTED]
  will_personal/Resume.md → Resume.md
- `William Donald Martínez Avellan` --references--> `Bupartech`  [EXTRACTED]
  will_personal/Resume.md → Resume.md
- `William Donald Martínez Avellan` --references--> `Docker`  [EXTRACTED]
  will_personal/Resume.md → Resume.md

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Consolidated USD Debt Calculation (Loans + Credit Cards @ BCN Rate)** — finance_debts_total_debt_consolidated_usd, finance_loans, finance_credit_cards [EXTRACTED 1.00]
- **July Bills Paid Via Credit Card (Increasing Card Balances)** — finance_credit_cards_bac_amex_black, finance_credit_cards_bac_pricesmart, 2026_2026_07 [EXTRACTED 1.00]

## Communities (29 total, 9 thin omitted)

### Community 0 - "Resume & Skills"
Cohesion: 0.05
Nodes (54): Ad Load Configuration, Additional, AdTech Platform, AG Software, AngularJS, AWS, Banex / Findesa, Bupartech (+46 more)

### Community 1 - "Income, Clients & July Bills"
Cohesion: 0.06
Nodes (33): Bills / Expenses, Cafeteria El Molino VI, Community Security (cash), David - School Tuition (monthly), ECSA Uno Los Robles, Electricity Bill, Fritoni, Home Internet Bill (+25 more)

### Community 2 - "Debts, Loans & Credit Cards"
Cohesion: 0.09
Nodes (34): AVANZ, Links, BAC (Banco de America Central), Links, Ficohsa, Links, Lafise (Lafise Bancentro), Links (+26 more)

### Community 3 - "Marco ERP & SEM Projects"
Cohesion: 0.09
Nodes (32): Aluval, Enhancement Payment System, Command Center (Enterprise Platform), CRM, Links, Vidrieria F. Morales, Architecture, Backend ([[Marco ERP - Backend|marco-backend]]) (+24 more)

### Community 4 - "Pluto TV Org & Contacts"
Cohesion: 0.17
Nodes (10): Contacts, Links, Pluto TV / Paramount, Project, Evan Caldwell, Links, Reports to, Direct reports (+2 more)

### Community 5 - "Obsidian App Config"
Cohesion: 0.26
Nodes (13): Obsidian Core Plugins Configuration, Backlink Plugin, Obsidian Bases Plugin, Obsidian Canvas Plugin, Daily Notes Plugin, Graph View Plugin, Obsidian Sync Plugin, Templates Plugin (+5 more)

### Community 6 - "Work Experience Roles"
Cohesion: 0.22
Nodes (9): AG Software — Technical Lead / Senior Software Engineer, Banex / Findesa — Programmer Analyst, Bupartech — Regional Technology Consultant, [[Enhancement Payment System]] — Senior Software Engineer, Experience, [[In All Media]] — Senior Software Engineer, Quoin Inc / AG Software — Senior Software Engineer / Technical Lead, Seaban S.A — Regional Technology Consultant (+1 more)

### Community 7 - "In All Media Client"
Cohesion: 0.25
Nodes (7): Clients, Engagement History, In All Media (Coderfull SA), Links, Payment Terms, Role, Statement of Work (Current)

### Community 8 - "Repo Documentation (CLAUDE.md)"
Cohesion: 0.52
Nodes (5): Directory Structure, graphify-out, Key Entities, What This Repo Is, Working With This Repo

### Community 9 - "Marco ERP Backend Repo"
Cohesion: 0.40
Nodes (4): Code Knowledge Graph, Links, Marco ERP - Backend, Repo

### Community 10 - "Marco ERP Frontend Repo"
Cohesion: 0.40
Nodes (4): Code Knowledge Graph, Links, Marco ERP - Frontend, Repo

### Community 11 - "Sales Sling Elastic Beanstalk"
Cohesion: 0.40
Nodes (4): Links, Related, Sales Sling (Elastic Beanstalk), Stack

### Community 12 - "Sales Sling Lambda"
Cohesion: 0.40
Nodes (4): Links, Related, Sales Sling (Lambda), Stack

### Community 13 - "Freelance Work Mode"
Cohesion: 0.40
Nodes (4): Active Clients, Freelance, Inactive Clients, Link

### Community 14 - "Queso CRM Project"
Cohesion: 0.50
Nodes (3): Links, Queso CRM, Stack

### Community 15 - "Contractor Work Mode"
Cohesion: 0.50
Nodes (3): Active, Contractor, Link

### Community 19 - "Bill Inbox Template"
Cohesion: 0.33
Nodes (7): Contact, Enhancement Payment System (EPS), Links, Payment Terms, Projects, Andres Cornejo, Links

### Community 20 - "Community 20"
Cohesion: 0.50
Nodes (4): Charges, Credit Cards, Notes, Payments

### Community 21 - "Community 21"
Cohesion: 0.50
Nodes (3): 1. Muro final lateral derecho, Home Improvements, Projects

## Ambiguous Edges - Review These
- `2026-07.md` → `Bill: Nacatamales (2026-07-25)`  [AMBIGUOUS]
  will_personal/Finance/_Inbox/Bill_2026-07-25_Nacatamales.md · relation: conceptually_related_to
- `Credit Cards.md` → `David - School Tuition (monthly)`  [AMBIGUOUS]
  will_personal/Finance/2026/2026-07.md · relation: conceptually_related_to

## Knowledge Gaps
- **122 isolated node(s):** `alwaysUpdateLinks`, `enableCommunityPlugins`, `Bill`, `CRM`, `Links` (+117 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **9 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What is the exact relationship between `2026-07.md` and `Bill: Nacatamales (2026-07-25)`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **What is the exact relationship between `Credit Cards.md` and `David - School Tuition (monthly)`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **Why does `Finance Overview` connect `Debts, Loans & Credit Cards` to `Marco ERP & SEM Projects`, `Income, Clients & July Bills`, `Bill Inbox Template`, `In All Media Client`?**
  _High betweenness centrality (0.309) - this node is a cross-community bridge._
- **Why does `William Donald Martínez Avellan` connect `Resume & Skills` to `Marco ERP & SEM Projects`, `Pluto TV Org & Contacts`, `Work Experience Roles`?**
  _High betweenness centrality (0.250) - this node is a cross-community bridge._
- **Why does `In All Media` connect `Marco ERP & SEM Projects` to `Resume & Skills`, `Debts, Loans & Credit Cards`, `Pluto TV Org & Contacts`?**
  _High betweenness centrality (0.221) - this node is a cross-community bridge._
- **What connects `alwaysUpdateLinks`, `enableCommunityPlugins`, `Bill` to the rest of the system?**
  _122 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Resume & Skills` be split into smaller, more focused modules?**
  _Cohesion score 0.05454545454545454 - nodes in this community are weakly interconnected._