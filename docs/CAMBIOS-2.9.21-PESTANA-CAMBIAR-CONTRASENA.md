# Smart Hub 2.9.21 — Pestaña Cambiar contraseña

Se agregó una página dedicada:

`/baja-smart-hub/cambiar-password`

Disponible desde:
- Perfil → Cambiar contraseña.
- Configuración → Seguridad → Cambiar contraseña.
- Enlaces nuevos de recuperación de contraseña.

Uso normal:
- pide contraseña actual;
- pide contraseña nueva;
- confirma contraseña nueva;
- permite cerrar las demás sesiones.

Uso desde recuperación:
- el enlace de correo apunta a
  `/cambiar-password?recuperacion=1`;
- la sesión de recuperación queda marcada;
- NO pide la contraseña anterior;
- sólo pide la nueva contraseña y su confirmación.

Después de desplegar esta versión, solicita un correo NUEVO de recuperación.
