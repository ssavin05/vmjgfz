# Smart Hub 2.9.12

La corrección de tamaño de la foto ya no depende únicamente de una hoja CSS externa.

En escritorio:
- ancho fijo máximo: 640 px
- alto: 360 px
- centrada
- fotografía completa con `object-fit: contain`

La restricción está en tres niveles:
1. estilo inline en `espacio.js`
2. CSS crítico embebido directamente en `index.html`
3. `css/ficha-desktop.css`

Esto evita que una hoja CSS vieja en caché vuelva a mostrar una fotografía gigante.

Sala de Juntas conserva sus tres fotografías. La foto IMG-20260824-WA0008.jpg
corresponde exactamente a `assets/fotos/sala-juntas/02.jpg`.
