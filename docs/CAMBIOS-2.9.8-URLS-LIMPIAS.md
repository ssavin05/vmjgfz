# Smart Hub 2.9.8 — URLs limpias

La app deja de usar hash routing.

Antes:
- https://ibarra.one/baja-smart-hub/#/
- https://ibarra.one/baja-smart-hub/#/mapa

Ahora:
- https://ibarra.one/baja-smart-hub/
- https://ibarra.one/baja-smart-hub/mapa
- https://ibarra.one/baja-smart-hub/reservas
- https://ibarra.one/baja-smart-hub/espacios/...

Se agrega `.htaccess` para Apache/cPanel y `<base href="/baja-smart-hub/">`
para que las rutas profundas sigan cargando CSS, JS y assets.

Los enlaces antiguos con # siguen funcionando y se convierten automáticamente
a la URL limpia.

También se corrige el nombre público de SJ-01 a “Sala de Juntas”.
Su precio se mantiene en $416.67 MXN/h + IVA.
