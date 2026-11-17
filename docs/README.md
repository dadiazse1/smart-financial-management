# Smart Financial Management — V1.20

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


## V1.9 — Dynamic client allocation correction
- Removed the dependency on fixed client A/client B or account X/account Y allocation positions.
- Personnel allocation is now derived directly from each person's named client assignments (client, platform/account, function, hours and dedication percentage).
- New client names entered in Platform Accounts & Functions are included automatically in personnel cost by client and profitability calculations.
- The team allocation view is now a calculated summary from named assignments, avoiding a second manual allocation source.
- When total assigned hours exceed monthly capacity, hours-based allocation is proportionally capped to prevent allocating more than 100% of a person's cost. Percentage-based allocation is similarly capped at 100%.
- Demo data remains fictional. Data is stored only in this browser; no backend or accounting/payroll integration is included.


## V1.9 — Automatic hours / percentage consistency
- In tracked-hours mode, dedication percentages are recalculated automatically from each assignment's hours and the person's productive monthly capacity.
- In monthly-salary allocation mode, equivalent hours are recalculated from each assignment's percentage.
- Existing saved demo assignments are normalized on render according to the selected costing method, correcting mismatches such as 100 assigned hours / 90% when capacity is 120 hours.
- Capacity validation continues to warn when assigned hours exceed productive capacity or assigned percentages exceed 100%.
- The selected method determines the source of truth; the derived measure is not independently editable in that mode.
- All demo records remain fictional and browser-local.


## Correcciones V1.20
- Se filtran nombres de clientes vacíos, nulos o guardados literalmente como `undefined` para evitar columnas incorrectas en la distribución de personal.
- Se agregaron las etiquetas de validación en español para capacidad excedida y asignación correcta.
- Se añadieron valores de respaldo para que la validación no muestre `undefined` si falta una traducción.
- Se conserva la asignación dinámica por nombre real de cliente y el costo interno/no asignado separado.

## Publicación
Reemplaza únicamente `docs/index.html` y `docs/README.md` con los archivos de este paquete. Conserva `docs/PROJECT_ROADMAP.md` y la configuración de GitHub Pages. Después de publicar, abre el sitio y presiona `Ctrl + Shift + R`.


## V1.21 – Bilingual costing snapshot correction
The costing engine and unit economics snapshot now explicitly apply Spanish and English labels when the language selector changes, including after page re-rendering.


## Version 1.23 correction
The Team & Capacity client-cost table now includes an explicit Internal / unassigned cost row. This reconciles client-allocated personnel cost plus internal/unassigned personnel cost to the total monthly payroll, and shows the corresponding unassigned hours and payroll share. All sample data remains fictional.


## Version 1.24 — Service Costing module

- Replaces the Service Costing placeholder with an editable service/project register.
- Tracks client, service, project/account, service revenue, other direct costs and client-funded media spend.
- Imports personnel allocations from Team & Capacity and shared software allocations from Digital Tools. Imported shared costs are allocated across each client’s service records in proportion to service revenue, avoiding duplicate manual entry.
- Separates client-funded media investment by default, with an explicit option to include it in service cost.
- Shows service-level contribution, contribution margin and client-level summaries.
- Uses fictional sample data and browser-local storage only. No backend, database, authentication or live accounting integrations.

To publish: replace `docs/index.html` and `docs/README.md` with the files in this package. Preserve `docs/PROJECT_ROADMAP.md` and the GitHub Pages settings.


## V1.25 — Cash Flow
- Cash Flow module with editable opening cash balance.
- Weekly 8-week forecast based on invoice outstanding balances and due dates.
- Actual collections are taken from payment records and therefore reduce outstanding invoice balances.
- Scheduled obligations (payroll, contractors, software, taxes, rent and other) can be added, edited only by deleting/re-entering, and removed.
- Invoice due date field added to Invoices & Collections and connected to the cash forecast.
- Invoices without due dates remain visible as unscheduled; no payment date is invented from historical behavior.
- All records are synthetic/local browser data; no backend or multi-user synchronization.
