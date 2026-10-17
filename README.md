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

## Anclar a la barra de tareas de Windows

La página se puede instalar como app (ventana propia con su icono):

1. Abre `https://flowaiinfo.lat/idpedidos` en **Chrome** o **Edge**.
2. Chrome: icono de instalar en la barra de direcciones (o menú ⋮ → **Transmitir, guardar y compartir** → **Instalar página como app**). Edge: menú … → **Aplicaciones** → **Instalar este sitio como una aplicación**.
3. Con la app abierta, clic derecho en su icono de la barra de tareas → **Anclar a la barra de tareas**.

## Ventana siempre visible

El botón **📌 Siempre visible** abre el cuadro de verificación en una ventana pequeña que se queda encima de las demás aplicaciones (Chrome/Edge 116+). Al cerrarla, el cuadro vuelve a la página. La página principal debe seguir abierta (puede estar minimizada).

## Formato del pedido e impresión

- Se pega el texto del pedido tal cual, por ejemplo `ID: 48213 Rappi`. La página separa el número (`48213`) y la plataforma (`Rappi`).
- Es **repetido** si el mismo número ya salió hoy por la misma plataforma (o si una de las dos no tiene plataforma). Si el número ya salió por otra plataforma, se marca nuevo con un aviso.
- **🖨 Imprimir tirilla** imprime todos los pedidos del día seleccionado (número, ID, plataforma y hora), con totales por plataforma. Para impresora de recibos, en el cuadro de impresión de Chrome elige esa impresora y en *Más opciones* pon márgenes en *Ninguno*.
