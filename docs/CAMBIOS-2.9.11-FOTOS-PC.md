# Smart Hub 2.9.11 — Fotos de oficinas en PC

Corrección basada en la captura real del sitio.

- La foto principal ya no ocupa casi todo el ancho del panel de escritorio.
- Máximo normal: 760 × 405 px.
- En monitores grandes: 720 × 405 px.
- Se usa un CSS dedicado cargado al final con reglas `!important`.
- `index.html` usa `?v=2.9.11` en CSS y JS críticos para romper caché.
- El service worker pide CSS/JS nuevos a la red antes de usar caché vieja.
- Sala de Juntas conserva sus 3 fotos reales.
- Móvil no cambia.
