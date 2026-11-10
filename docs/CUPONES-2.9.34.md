# Cupones y promociones — Smart Hub 2.9.34

## Qué se agregó

- Campo **¿Tienes un código de descuento?** en la reserva.
- Panel **Administración → Cupones**.
- Cupones generales o limitados a una o varias oficinas / Sala de Juntas.
- Descuento porcentual, monto fijo u horas de cortesía.
- Fecha de inicio y vencimiento.
- Límite total de usos y límite por cliente.
- Activar/desactivar sin borrar el historial.
- Validación del descuento en servidor.

## Paso obligatorio en Supabase

Después de subir el ZIP, abre **Supabase → SQL Editor**, pega el contenido de:

`supabase/migracion-20-cupones-descuento.sql`

y ejecútalo una sola vez.

## Ejemplo

En **Administración → Cupones → Nuevo cupón**:

- Código: `SMART10`
- Tipo: Porcentaje de descuento
- Valor: `10`
- Dónde aplica: Todos los espacios (o selecciona oficinas concretas)
- Máximo por cliente: `1`
- Vencimiento: opcional

El cliente escribe `SMART10` al reservar. El resumen mostrará el descuento antes de continuar al checkout. El total definitivo se vuelve a calcular en la función `crear_reserva` del servidor.
