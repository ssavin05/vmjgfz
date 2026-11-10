# Smart Hub 2.8.5 — mapa 3D exacto

La vista `#/mapa` usa ahora `js/three/escena-exacta.js`.

La geometría visual ya no se recompone con rectángulos de `espacios`.
Se usa el mismo trazado por polígonos que el HTML standalone aprobado,
manteniendo los datos reales de Supabase para selección y reservas.

Cambios visibles:
- cámara ortográfica isométrica;
- fondo azul claro;
- paredes negras continuas;
- nombres grandes flotantes;
- sin precios impresos sobre el edificio;
- una sola puerta decorativa exterior por Recepción;
- A/B/C/D: D izquierda, C arriba derecha, B centro derecha y A abajo derecha;
- contorno azul en A/B/C/D;
- selección con relleno azul oscuro sólido;
- auto en cochera y cuatro autos en estacionamiento frontal.
