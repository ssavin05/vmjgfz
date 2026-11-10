# Smart Hub 2.9.3 — Pagos y Clientes

## Error corregido
Las filas de las tablas de Pagos y Clientes se construían como HTML seguro,
pero después se convertían a texto con `.join("")` y la plantilla principal
las volvía a escapar. Por eso aparecían etiquetas `<tr><td>...` impresas en
pantalla.

Ahora cada fila se mantiene como objeto `html` seguro hasta insertarse en el DOM.

## Móvil
- Pagos se muestra como tarjetas legibles, sin tabla horizontal gigante.
- Clientes se muestra como tarjetas con correo, teléfono, empresa, reservas y rol.
- Los filtros de Pagos pueden desplazarse horizontalmente.
- Los canales Clip se compactan en móvil.
- Escritorio conserva tablas normales.
