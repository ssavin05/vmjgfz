# Smart Hub 2.9.26 — despliegue sin caché

Esta versión ataca específicamente el problema donde el hosting ya tenía
archivos nuevos pero el navegador seguía mostrando una versión anterior.

Cambios:
- Service Worker desactivado temporalmente.
- Workers anteriores se desregistran al abrir la app.
- Se borran cachés `co-*`.
- HTML, JS y CSS se sirven con `no-store` desde `.htaccess`.
- El bootstrap de limpieza corre en cada carga.
- Se conservan los botones Mostrar/Ocultar contraseña.
- Se conserva la validación: 8 caracteres + minúscula + mayúscula + número.

Comprobación:
abre
https://ibarra.one/baja-smart-hub/?v=2926

La pantalla debe mostrar Smart Hub v2.9.26.
