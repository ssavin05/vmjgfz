# Smart Hub 2.9.15 — Migración 19 corregida

La migración anterior fallaba en algunas bases con ERROR 42883 porque
intentaba llamar una función de horario que no estaba instalada.

La nueva migración 19 ya no depende de ninguna función externa de horarios.

Agrega un trigger autónomo sobre `public.reservas`:
- INSERT con `inicio <= now()` → rechazado.
- UPDATE que cambie `inicio` o `fin` hacia una hora ya iniciada → rechazado.
- Cambios normales de estado/pago/cancelación siguen funcionando.
