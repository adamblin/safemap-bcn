<p align="center"><img src="app%20logo.png" alt="SafeHer logo" width="180"></p>

# SafeHer

A collaborative, anonymous map that helps women plan how to get around Barcelona.

- **Heat map**: 🟢 safe · 🟡 caution · 🔴 unsafe, calculated from community reports.
- **Day / Night**: how safe a place feels changes with the time; by default the map shows the current one.
- **Safe route**: compares walking routes, highlights the safest one and colours each section.
- **Anonymous reports**: no sign-up, location rounded to ~10 m.
- **Community moderation**: a report needs 2 confirmations to count fully and is hidden if the community flags it as fake.
- **Trusted circle**: save up to 5 trusted contacts and send your location or your trip (route + arrival time) via WhatsApp, SMS or the share menu. A check-in reminder asks if you are OK if you have not arrived on time.
- **Walk together**: see verified women heading the same way and ask to walk together, meeting at a busy public spot (simulated profiles in this prototype).
- One-tap **112** emergency button.

The whole app is a single file: [`index.html`](index.html) (HTML + CSS + JS).

## Use it

Open `index.html` in a browser, or use the GitHub Pages version: https://adamblin.github.io/safemap-bcn/

Direct links: `?map` (skips the welcome screen) and `?mode=night`, `?mode=day` or `?mode=all`.

## Tech

- [Leaflet](https://leafletjs.com/) 1.9.4, **embedded in index.html** (no CDN dependency).
- Street map with fallback providers: if one fails or takes longer than 7 s, the next one is used
  (Esri World Street Map → OpenStreetMap DE → OSM France → OpenStreetMap). Night mode darkens the same map with a CSS filter.
- Search: [Nominatim](https://nominatim.org/) · Walking routes: [OSRM](https://routing.openstreetmap.de/)

## ⚠️ Prototype

The sample reports are **simulated data** and do not reflect real statistics.
New reports and votes are stored only in the browser (localStorage). Sharing them between users will need a backend.
