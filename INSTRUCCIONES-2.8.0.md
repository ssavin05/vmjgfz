# Smart Hub 2.8.0

## Entrar al modo administrador

1. Inicia sesión con tu cuenta.
2. Abre **Perfil**.
3. Pulsa **Entrar al panel administrativo**.

También puedes abrir directamente `#/admin` al final de la dirección del sitio.

Si aparece **Verificar acceso**, tu sesión funciona pero Supabase todavía está
reportando el rol `usuario`. Abre el **SQL Editor** del proyecto y ejecuta:

```sql
update public.usuarios
set rol = 'admin'
where lower(email) = lower('TU-CORREO@EJEMPLO.COM');
```

Después vuelve a Perfil y pulsa **Verificar acceso**. No hace falta cerrar sesión.
La explicación ampliada está en `docs/ACCESO-ADMIN.md`.

## Antes de publicar

- Conserva los valores reales de Supabase en la configuración actual.
- No pongas secretos de Clip en archivos del navegador.
- Si la base aún no tiene los nombres comerciales, aplica las migraciones en el
  orden documentado en `README.md` y `OWNER_ACTIONS.md`.
- Publica todos los archivos del ZIP, incluido `sw.js`, para que la caché cambie
  a la versión 2.8.0.

El mapa 3D, login, reservas, cancelaciones, Supabase y Clip se conservaron.
