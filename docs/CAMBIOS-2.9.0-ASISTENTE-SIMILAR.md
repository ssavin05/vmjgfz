# Smart Hub 2.9.0 — Asistente más tolerante

El asistente ya entiende mejor palabras parecidas, errores de escritura y frases coloquiales.

Ejemplos:
- `ofisina` → oficina
- `presio` → precio
- `reserbar` → reservar
- `ocupo una oficina` → buscar/reservar
- `cuánto sale la B` → precio de Oficina B
- `¿y la C?` después de hablar de precios → conserva el contexto de precios

También se mejoró la búsqueda por nombre, código, descripción y amenidades.

La Edge Function `asistente` recibió la misma regla semántica para que el modo con IA
no dependa de coincidencias literales.
