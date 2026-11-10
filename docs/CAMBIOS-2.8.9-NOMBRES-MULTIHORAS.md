# Smart Hub 2.8.9

- Las oficinas reservables se muestran con sus nombres originales:
  Oficina A, Oficina B, Oficina C y Oficina D.
- Ya no se usan Ejecutiva Plus / Ejecutiva Compact / Premium Patio View / Ejecutiva Lounge
  como nombres visibles en la app.
- En la pantalla de reservación se pueden seleccionar varias horas consecutivas.
- Al seleccionar una hora inicial y otra posterior, las horas libres intermedias se
  seleccionan automáticamente.
- No se permite formar una reserva con un hueco ocupado en medio.
- El backend recibe un solo rango continuo, por ejemplo `12:00-16:00`, por lo que
  mantiene la validación atómica de disponibilidad y el cálculo correcto por horas.
- La duración y el total se actualizan según el rango seleccionado.
