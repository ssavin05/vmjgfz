# Smart Hub 2.9.14 — No reservar horas ya iniciadas

Nueva regla:
- 11:23 → 11:00-12:00 ya no se puede reservar.
- 11:23 → 12:00-13:00 sí puede reservarse si está libre.
- La franja se cierra en cuanto llega su hora de inicio.

La regla existe tanto en frontend como en Supabase:
- rejilla de horarios;
- botón Continuar;
- checkout mediante URL;
- disponibilidad diaria;
- semáforo del mapa;
- `esta_disponible`;
- `validar_ventana_reserva`.

Para una base existente hay que ejecutar:
`supabase/migracion-19-no-reservar-hora-iniciada.sql`.
