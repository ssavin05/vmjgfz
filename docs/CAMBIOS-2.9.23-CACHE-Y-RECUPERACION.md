# Smart Hub 2.9.23

Corrección principal:
- El navegador podía seguir ejecutando módulos de la 2.9.21 desde el Service Worker aunque se borraran los archivos del hosting.
- Se agregó `js/bootstrap-update.js`, que al detectar este despliegue:
  - desregistra workers viejos del scope `/baja-smart-hub/`;
  - borra cachés `co-*`;
  - fuerza una carga limpia una sola vez;
  - después `main.js` registra nuevamente el Service Worker 2.9.23.

Recuperación:
- Se conserva la página pública `/restablecer-password`.
- No pide la contraseña anterior.
- El email solicita `redirectTo: /restablecer-password`.

Después de desplegar:
1. Abre `https://ibarra.one/baja-smart-hub/?_shv=2.9.23`.
2. Debe mostrar `Smart Hub · v2.9.23`.
3. Solicita un correo NUEVO de recuperación.
