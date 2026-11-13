# Smart Financial Management — V1.13

## Novedades
- Conciliación de gastos generales para la rentabilidad total de la agencia.
- La participación interna se muestra por separado y se incluye en el costo total de operación.
- Los gastos generales no distribuidos (por ejemplo, porcentajes manuales pendientes) se muestran por separado y también se incluyen en el costo total.
- La utilidad real de la agencia resta costos directos y el 100% de los gastos generales registrados, sin excluir la parte interna.
- La rentabilidad individual de cada cliente conserva únicamente los gastos generales que se le asignaron.
- Se conservan los registros locales existentes de la versión 1.12.

## Criterio contable del tablero
Los ingresos se toman de la base gravable facturada, sin IVA. El IVA no es ingreso propio. Las retenciones afectan el recaudo esperado, pero no reducen el ingreso facturado usado para calcular la rentabilidad.

Los gastos generales se registran una sola vez. La suma de: asignado a clientes + parte interna + no distribuido debe coincidir con el gasto general total. La parte interna y los importes no distribuidos se incluyen en la utilidad consolidada de la agencia para evitar subestimar sus costos.

## Privacidad y almacenamiento
- Datos de demostración ficticios.
- Los datos se guardan únicamente en el almacenamiento local del navegador. No hay servidor, autenticación, respaldo central ni integración con SIIGO/DIAN.
- Antes de activar costos automáticos de personal, verifica las asignaciones en Team & Capacity y evita ingresarlos nuevamente en los campos manuales.

## Publicación en GitHub Pages
Reemplaza `docs/index.html` y `docs/README.md`. Conserva `docs/PROJECT_ROADMAP.md` y la configuración de GitHub Pages. Después de publicar, actualiza con `Ctrl + Shift + R`.
