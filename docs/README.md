# Smart Financial Management

## Publicación en GitHub Pages

Este proyecto se publica desde la rama `main`, carpeta `/docs`.

### Archivos
- `index.html`: aplicación web y módulos.
- `README.md`: estas instrucciones.

### Actualizar el sitio
1. En GitHub, abre el repositorio `smart-financial-management`.
2. Abre la carpeta `docs`.
3. Reemplaza `index.html` por el archivo de esta carpeta.
4. Conserva los demás archivos existentes, incluido `PROJECT_ROADMAP.md`.
5. Confirma el cambio con **Commit changes**.
6. Espera a que el flujo **pages build and deployment** finalice correctamente.
7. Recarga el sitio con `Ctrl + Shift + R`.

## Nota de diagnóstico
La función auxiliar `byId` está declarada al inicio del bloque JavaScript, antes de que los módulos puedan invocarla. Si el navegador sigue mostrando el error anterior, comprueba que el archivo publicado sea este y que la consola no esté mostrando una versión almacenada en caché.

## Datos
La aplicación utiliza datos demostrativos ficticios. No cargues información confidencial, bancaria, de clientes ni de empleados.
