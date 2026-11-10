# Smart Hub 2.9.1 — Mapa mobile-first

La vista móvil se considera ahora la vista principal del mapa.

## Cambios de interacción
- 1 dedo desplaza el plano, como un mapa.
- 2 dedos hacen zoom y también permiten desplazar durante el pellizco.
- El botón de giro conserva la rotación 3D.
- El botón de cubo restablece de verdad posición, zoom y orientación.
- Cambiar entre vertical/horizontal vuelve a encuadrar automáticamente.

## Cambios de encuadre
- La cámara móvil es más cenital para facilitar lectura y selección.
- El cálculo de cámara reserva espacio real para buscador, días y controles.
- El edificio no queda escondido debajo de la interfaz.
- No se deforma la geometría.

## Rendimiento móvil
- El minimapa no se crea en teléfonos; se ahorra un canvas y actualizaciones por frame.
- La calidad del render principal se mantiene adaptativa.

## Interfaz
- Buscador y días son más compactos.
- Los controles pasan a una barra horizontal inferior.
- El panel de oficina ocupa menos pantalla.
- Se muestra una ayuda de gestos sólo la primera vez.
- Las etiquetas de espacios pequeños reducen tamaño en móvil para evitar superposición.
