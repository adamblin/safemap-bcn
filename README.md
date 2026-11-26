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

- [Leaflet](https://leafletjs.com/) + teselas de [CARTO](https://carto.com/) / [OpenStreetMap](https://www.openstreetmap.org/)
- Búsqueda: [Nominatim](https://nominatim.org/)
- Rutas a pie: [OSRM](https://routing.openstreetmap.de/)

## ⚠️ Prototipo

Los reportes de ejemplo son **datos simulados** y no reflejan estadísticas reales.
Los reportes y votos nuevos se guardan solo en el navegador (localStorage). Para compartirlos entre usuarias hará falta un backend.
