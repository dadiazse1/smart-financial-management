# Smart Financial Management — V1.10

Prototipo bilingüe (ES/EN) para inteligencia financiera y costeo de una agencia. Datos de demostración ficticios, almacenados únicamente en el navegador mediante localStorage.

## Novedades V1.10
- Número de factura único por cliente: evita guardar duplicados.
- Consolidación inicial de registros duplicados de la versión anterior: conserva el mayor valor esperado y el mayor recaudo conocido; no suma recaudos duplicados.
- Edición de facturas existentes.
- Registro de pagos parciales múltiples con fecha e historial.
- Cálculo del saldo pendiente y validación para impedir pagos superiores al saldo.
- Eliminación de facturas de demostración.
- Conserva configuración individual de retenciones por cliente y cálculo porcentual / por mil.

## Publicación en GitHub Pages
Reemplaza `docs/index.html` y `docs/README.md` con estos archivos. Conserva `docs/PROJECT_ROADMAP.md` y la configuración de Pages. Después de confirmar los cambios, abre el sitio y actualiza con Ctrl + Shift + R.

## Limitaciones
- Es un prototipo local; no tiene base de datos, autenticación, conexión con SIIGO o DIAN ni sincronización entre dispositivos.
- La consolidación de duplicados usa número y cliente como clave. Si hay registros antiguos repetidos, conserva el mayor valor esperado y el mayor recaudo registrado, sin sumar valores potencialmente duplicados.
- Los pagos de demostración se registran desde el botón “Registrar pago”.
- Las retenciones son configurables; el usuario debe validar su aplicación y base gravable para cada operación.
- No calcula obligaciones tributarias ni nómina legal.


### Mejora V1.10
- Permite editar individualmente cada movimiento de recaudo desde el historial de la factura.
- Se puede corregir la fecha de pagos migrados que aparecen como “Fecha no registrada”.
- Permite corregir el valor del pago, validando que el total recaudado no supere el neto esperado.
- Los cambios actualizan automáticamente el recaudo acumulado y el saldo pendiente.
