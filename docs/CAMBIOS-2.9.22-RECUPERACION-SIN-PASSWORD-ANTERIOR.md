# 2.9.22

Se agregó `/restablecer-password` como ruta pública exclusiva para recuperación.
El enlace de correo entra ahí, valida el código de Supabase y pide únicamente la contraseña nueva y su confirmación. No pide la contraseña anterior.

El `redirectTo` usado por `resetPasswordForEmail` ahora es:
`https://ibarra.one/baja-smart-hub/restablecer-password`

Después de desplegar, solicitar un correo NUEVO.
