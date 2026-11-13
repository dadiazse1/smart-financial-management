# Smart Financial Management — V1.11

Prototipo bilingüe (ES/EN) de inteligencia financiera y costeo para una agencia. Usa exclusivamente datos ficticios y almacenamiento local del navegador.

## Novedades V1.11 — Rentabilidad financiera conectada
- Nuevo panel de rentabilidad que toma como ingreso de servicios la base gravable de las facturas registradas, sin sumar IVA.
- Las retenciones se mantienen como descuentos del recaudo esperado y no reducen el ingreso propio usado para estimar rentabilidad.
- Consolida por cliente la base facturada, costos de mano de obra, contratistas, otros costos directos y herramientas compartidas.
- Permite ingresar/ajustar costos por cliente y conserva esos supuestos en el navegador.
- Calcula costo total, utilidad estimada y margen por cliente.
- Añade una vista de contribución por servicio con una distribución ilustrativa inicial de 55% pauta digital, 30% contenido/diseño y 15% estrategia/gestión.

## Lógica financiera importante
- **Ingreso para rentabilidad:** base gravable de facturas, sin IVA.
- **Recaudo esperado:** base + IVA − retenciones aplicables.
- **Caja recibida:** suma de pagos registrados.
- **Saldo pendiente:** recaudo esperado − pagos registrados.
- El IVA se muestra separado y no se trata como ingreso propio.
- Las retenciones reducen el efectivo recibido, pero no son costos operativos ni reducen por sí mismas el ingreso por servicios.

## Publicación en GitHub Pages
Reemplaza `docs/index.html` y `docs/README.md` con estos archivos. Conserva `docs/PROJECT_ROADMAP.md` y la configuración de Pages. Después del commit, abre el sitio y actualiza con `Ctrl + Shift + R`.

## Limitaciones
- Es un prototipo local; no tiene base de datos, autenticación, sincronización entre dispositivos ni integración con SIIGO o DIAN.
- Los costos de mano de obra, contratistas y otros costos del nuevo panel se ingresan manualmente por cliente; aún no se calculan automáticamente desde cada asignación de persona/rol/horas.
- La distribución por servicio 55/30/15 es una hipótesis demostrativa editable en el diseño futuro, no una atribución real de horas ni costos por servicio.
- Los costos de herramientas se leen de la distribución existente del módulo Digital Tools.
- Los clientes sin costos asignados pueden mostrar utilidad sobreestimada; completa los costos antes de usar el resultado para tomar decisiones.
- No calcula impuestos, retenciones legalmente aplicables ni nómina legal. Verifica las bases y tarifas con el responsable contable.
- Todos los datos de ejemplo son ficticios. No ingreses información confidencial o datos reales de clientes, trabajadores o bancos.
