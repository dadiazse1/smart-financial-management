# Smart Financial Management — V1.17

Demo bilingüe de inteligencia financiera y costeo para agencias. Todos los datos incluidos son ficticios.

## Mejoras V1.16
- Corrección de comas visibles entre filas de asignaciones.
- Porcentaje de dedicación calculado automáticamente al cambiar las horas (horas / capacidad productiva mensual). El porcentaje sigue siendo editable manualmente.
- Resumen por integrante con horas asignadas, capacidad, horas disponibles y dedicación total.
- Alerta cuando las horas superan la capacidad mensual o la dedicación supera el 100%.
- La validación distingue capacidad excedida de diferencias entre horas y porcentaje; muestra el porcentaje equivalente calculado a partir de las horas. Se admite una tolerancia de 0,5 puntos porcentuales.
- El costo asignado por horas se limita al costo mensual total de cada integrante, evitando que una sobreasignación genere costos superiores a su remuneración.
- Datos locales migrados desde V1.15; no se conectan servicios externos ni bases de datos.

## Publicación en GitHub Pages
Reemplaza `docs/index.html` y `docs/README.md`. Conserva `docs/PROJECT_ROADMAP.md` y la configuración actual de GitHub Pages.

## Privacidad y alcance
Usa únicamente datos sintéticos. Los cambios se guardan en el almacenamiento local del navegador. Esta demostración no calcula nómina legal, prestaciones, aportes, impuestos ni sustituye un sistema contable.


## V1.10 — Dynamic client allocation correction
- Removed the dependency on fixed client A/client B or account X/account Y allocation positions.
- Personnel allocation is now derived directly from each person's named client assignments (client, platform/account, function, hours and dedication percentage).
- New client names entered in Platform Accounts & Functions are included automatically in personnel cost by client and profitability calculations.
- The team allocation view is now a calculated summary from named assignments, avoiding a second manual allocation source.
- When total assigned hours exceed monthly capacity, hours-based allocation is proportionally capped to prevent allocating more than 100% of a person's cost. Percentage-based allocation is similarly capped at 100%.
- Demo data remains fictional. Data is stored only in this browser; no backend or accounting/payroll integration is included.


## V1.10 — Automatic hours / percentage consistency
- In tracked-hours mode, dedication percentages are recalculated automatically from each assignment's hours and the person's productive monthly capacity.
- In monthly-salary allocation mode, equivalent hours are recalculated from each assignment's percentage.
- Existing saved demo assignments are normalized on render according to the selected costing method, correcting mismatches such as 100 assigned hours / 90% when capacity is 120 hours.
- Capacity validation continues to warn when assigned hours exceed productive capacity or assigned percentages exceed 100%.
- The selected method determines the source of truth; the derived measure is not independently editable in that mode.
- All demo records remain fictional and browser-local.


## V1.10 — Internal personnel cost in agency profitability
- Added an explicit “Internal / unassigned cost” row to the Team & Capacity personnel-cost-by-client summary. It shows remaining productive capacity and the corresponding personnel cost not assigned to client work.
- Added a separate “Internal / unassigned personnel” KPI to the financial bridge.
- When “Include Team & Capacity allocation” is enabled, internal/unassigned personnel cost is included once in total agency operating cost and deducted from actual agency profit.
- Client-level personnel costs remain allocated to their named clients; the internal row is not charged to any client.
- Service contribution calculations use total agency costs including internal personnel.
- When automatic Team & Capacity allocation is disabled, internal personnel is not added to the financial bridge, avoiding an unexpected charge when users enter personnel costs manually.
- Synthetic demo data only; local browser storage; no accounting or payroll integration.
