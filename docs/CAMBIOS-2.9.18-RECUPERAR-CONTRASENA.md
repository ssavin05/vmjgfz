# Smart Hub 2.9.18 — Recuperar contraseña

El login ahora muestra claramente:

**¿Olvidaste tu contraseña?**

Flujo:
1. El usuario escribe su correo.
2. Smart Hub solicita a Supabase Auth un enlace de recuperación.
3. El usuario abre el enlace recibido por correo.
4. La app detecta el token y abre `/nueva-password`.
5. El usuario crea y confirma una contraseña nueva.
6. Supabase actualiza la contraseña.

Si el enlace caducó, la misma pantalla permite pedir otro.

Configuración necesaria en Supabase:
Authentication → URL Configuration

Site URL:
https://ibarra.one/baja-smart-hub/

Redirect URLs:
https://ibarra.one/baja-smart-hub/**

La recuperación de contraseña se controla con `passwordRecoveryEnabled` y
es independiente de los demás correos opcionales (`emailDeliveryEnabled`).
