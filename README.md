# ID Pedidos

Página para `flowaiinfo.lat/idpedidos` que verifica si un ID de pedido ya fue despachado el mismo día.

- **Verde**: el ID es nuevo hoy. Presiona Enter (o el botón) para marcarlo como despachado.
- **Rojo**: el ID ya fue despachado hoy (muestra la hora).
- La comparación ignora espacios y mayúsculas/minúsculas.
- La lista se guarda en el navegador (localStorage), separada por día; cada día empieza vacía y se pueden consultar días anteriores, exportar a CSV o borrar.

## Publicar (cPanel · Git Version Control)

El archivo `.cpanel.yml` copia `idpedidos/` a `~/public_html/idpedidos/`, así la página queda en `flowaiinfo.lat/idpedidos`.

1. cPanel → **Git Version Control** → **Create**.
2. Activa **Clone a Repository**. Clone URL: `https://github.com/bryanmoreta71/IdPedidos.git`. Repository Path: `repositories/IdPedidos` (no lo pongas dentro de `public_html`). Nombre: `IdPedidos`.
3. Cuando termine de clonar → **Manage** → pestaña **Pull or Deploy** → **Update from Remote** y luego **Deploy HEAD Commit**.
4. Abre `https://flowaiinfo.lat/idpedidos`.

Para publicar cambios futuros: haz el commit en GitHub y en cPanel repite **Update from Remote** → **Deploy HEAD Commit**.
