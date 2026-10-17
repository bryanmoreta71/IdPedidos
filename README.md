# ID Pedidos

Página para `flowaiinfo.lat/idpedidos` que verifica si un ID de pedido ya fue despachado el mismo día.

- **Verde**: el ID es nuevo hoy. Presiona Enter (o el botón) para marcarlo como despachado.
- **Rojo**: el ID ya fue despachado hoy (muestra la hora).
- La comparación ignora espacios y mayúsculas/minúsculas.
- La lista se guarda en el navegador (localStorage), separada por día; cada día empieza vacía y se pueden consultar días anteriores, exportar a CSV o borrar.

## Publicar

Copia la carpeta `idpedidos/` a la raíz del sitio `flowaiinfo.lat`, de modo que quede `flowaiinfo.lat/idpedidos/index.html`. Es un único archivo HTML estático, sin dependencias.
