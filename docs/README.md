# Smart Financial Management

**AI-powered financial intelligence for digital marketing agencies.**

Version 1.0 is a bilingual (English/Spanish) Glass Dashboard front-end prototype.

## Core product model
- Profitability by client, service, and project.
- Dual labor costing: tracked delivery hours and monthly payroll allocation.
- Advertising spend can be shown separately as client-funded pass-through or included in the service cost view.
- Agency service revenue is distinguished from client media budgets.
- Currency display supports COP and USD.

## Run
Open `index.html` in a modern browser. The prototype is self-contained and does not require a build process, external libraries, or network access.

## Privacy
All names and financial figures are fictional synthetic demo data. Do not commit confidential client, employee, banking, invoice, credential, or company information to this public repository.

## Current limitations
This is a front-end prototype. Detailed allocation calculations, database persistence, authentication, multi-tenant security, accounting integrations, advertising platform integrations, and AI services are not implemented yet.

See `docs/PROJECT_ROADMAP.md` for the development plan.


## Shared digital tools costing
The prototype includes a centralized inventory of company-wide subscriptions and an illustrative client allocation table. Shared tools are recorded once and allocated using documented drivers such as usage, seats, hours, or agreed percentages. The demo reserves 10% for internal agency operations; client allocations should total 90% in this example. This is a UI demonstration, not yet a persistent accounting engine.


## V1.2 – Digital Tools module
The Digital Tools module now supports adding and deleting subscriptions, monthly cost totals,
billing frequency, subscription and renewal dates, status, and allocation method (percentage,
users/licenses, or consumption). Client allocation percentages and the internal agency share
are editable; the module flags when the allocation does not total 100%.

Demo changes are saved in the current browser using localStorage. They are not synchronized
between users or devices and are not stored in a server database. All seeded data is fictional.


## V1.3 – Independent allocation engine
Each active subscription now calculates its allocation independently using its configured method:
- Percentage: client percentage weights plus internal agency percentage.
- Users/licenses: assigned seats for each client and internal agency seats.
- Consumption/usage: measured usage units for each client and internal agency usage units.

Select a tool to edit its own driver values and see each client's calculated share and allocated
cost. Inventory totals, client allocation and internal agency share recalculate from individual
tool allocations. This remains a browser-only prototype using localStorage, not a server database
or synchronized multi-user system. Existing V1.2 tools are retained in the same browser.
All sample names and values are fictional.


## V1.3.1 – Usage allocation default correction
Corrected the sample internal usage driver so usage-based tools start with 90 client units
and 10 internal agency units, consistent with the sample allocation. Existing browser demo
records created by V1.3 are migrated once when this version loads. This is a demo-only
calculation and should be replaced with measured usage data in a production system.


## V1.4 – Client profitability engine
Adds a bilingual client profitability module with fictional editable monthly revenue,
personnel, freelancer and other direct cost assumptions. Allocated shared tool costs are
pulled from the Digital Tools allocation engine, then total delivery cost, gross profit and
gross margin are recalculated by client. A selected-client service contribution view provides
an illustrative split across paid media management, content/creative, and analytics/strategy.
Values are synthetic and stored in browser localStorage only. The service split is illustrative;
project-level time tracking, auditable cost allocation, backend persistence and multi-user
synchronization are not yet implemented.


## V1.5 – Team & Capacity engine
Adds an editable synthetic team roster with monthly salary and productive hours.
Supports two personnel costing methods: tracked hours (salary allocated by client hours
over productive capacity) and monthly salary allocation (editable client percentages).
Shows payroll, client-allocated personnel cost, internal/unallocated cost, capacity utilization,
and personnel cost by client. Data is stored in browser localStorage only. It is a prototype:
no employee records, payroll integrations, time-clock validation, leave calendar, or backend
synchronization are implemented. Use synthetic data only.


## V1.6 – Team, remuneration, accounts & functions
Extends the synthetic team module to distinguish employees and contractors and model
monthly remuneration components: base/salary, account X and Y fees, fixed fee, variable
bonus/fee, and (for contractors) hourly rate multiplied by paid hours. Adds editable
client/platform/account/function assignments with both monthly hours and dedication
percentages. Supports Meta Ads, Google Ads, TikTok Ads and other/internal functions.
The team cost engine uses the selected allocation basis (hours or percentages) for the
client-level personnel cost summary. Assignment hours and percentages are stored together
for operational analysis; they are not added together. Data is stored in browser localStorage.
No statutory payroll, benefits, tax, legal classification or backend synchronization is included.


## V1.7 – Multiple roles per person
Adds employee and contractor role catalogs and permits selecting multiple roles/functions
for one team member. Employee roles: Gerente, Líder de Marketing Digital and Auxiliar
Contable. Contractor roles: Trafficker, Diseñador, Community Manager, Project Manager,
Administrativo, Estratega and Auditoría Comercial. Role selection is stored with the
synthetic team record in browser localStorage. This is an editable prototype, not an HR
master-data or legal classification system.
