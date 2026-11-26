# 🛡️ SafeMap BCN

Mapa colaborativo y anónimo para que las mujeres puedan planificar por dónde moverse en Barcelona.

- **Mapa de calor** 🟢 seguro · 🟡 precaución · 🔴 inseguro, calculado a partir de los reportes de la comunidad.
- **Día / Noche**: la sensación de seguridad cambia con la hora; por defecto se muestra la del momento actual.
- **Ruta segura**: compara rutas a pie y marca la más segura, coloreando cada tramo.
- **Reportes anónimos**: sin registro, posición redondeada a ~10 m.
- **Moderación comunitaria**: un reporte necesita 2 confirmaciones para contar del todo y se oculta si la comunidad lo marca como falso.
- Botón directo al **112**.

Toda la app está en un único archivo: [`index.html`](index.html) (HTML + CSS + JS).

## Usarla

Abre `index.html` en el navegador, o la versión publicada en GitHub Pages.

## Tecnología

- [Leaflet](https://leafletjs.com/) 1.9.4, **incluido dentro del propio index.html** (no depende de ningún CDN).
- Mapa de calles con proveedores de respaldo: si uno falla o tarda más de 7 s se pasa al siguiente
  (Esri World Street Map → OpenStreetMap DE → OSM France → OpenStreetMap). El modo noche oscurece el mismo mapa con un filtro CSS.
- Búsqueda: [Nominatim](https://nominatim.org/) · Rutas a pie: [OSRM](https://routing.openstreetmap.de/)

Enlaces directos: `?mapa` (salta la bienvenida) y `?modo=noche`, `?modo=dia` o `?modo=todo`.

## ⚠️ Prototipo

Los reportes de ejemplo son **datos simulados** y no reflejan estadísticas reales.
Los reportes y votos nuevos se guardan solo en el navegador (localStorage). Para compartirlos entre usuarias hará falta un backend.
