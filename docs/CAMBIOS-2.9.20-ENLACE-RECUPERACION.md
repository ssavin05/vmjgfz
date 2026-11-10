# Smart Hub 2.9.20 — Enlace de recuperación corregido

Problema:
El correo sí llegaba, pero al abrir el enlace terminaba dentro de la app
en vez de mostrar la pantalla para crear una contraseña nueva.

Causa:
La app limpiaba `?code=...` de la URL ANTES de que Supabase Auth pudiera
intercambiar ese código PKCE por una sesión temporal de recuperación.
Además, `resetPasswordForEmail` regresaba a la raíz de la app.

Corrección:
- `resetPasswordForEmail` ahora usa:
  `https://ibarra.one/baja-smart-hub/nueva-password`
- `revisarEnlaceDeCorreo()` ya no borra `?code=...` antes de Supabase.
- La URL se limpia solamente después de que Auth tuvo oportunidad de
  procesar el callback.
- `/nueva-password` se reconoce como destino de recuperación incluso en
  callbacks PKCE donde sólo llega `?code=...`.

En Supabase debe seguir permitida:
`https://ibarra.one/baja-smart-hub/**`

Los enlaces de recuperación enviados ANTES de desplegar 2.9.20 pueden
seguir apuntando a la ruta anterior. Solicita un correo nuevo después de
subir esta versión.
