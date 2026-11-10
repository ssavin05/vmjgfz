# Mapa móvil táctil

- Control táctil nativo con `touchstart/touchmove/touchend` y `passive:false`.
- Un dedo orbita/mueve el mapa.
- Dos dedos hacen pinch zoom hasta 7.5x.
- Toque simple selecciona oficinas A/B/C/D.
- Botones +/- usan el zoom real de la escena.
- `touch-action:none` se fuerza por CSS y por JavaScript.
- Zoom inicial ortográfico adaptado a móvil sin deformar la geometría.
- Mini mapa reducido y oculto en teléfonos muy angostos para no bloquear interacción.
