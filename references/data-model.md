# Modelo de datos

## Entidades

- `Worker`: identificador interno, alias, estado y referencias protegidas.
- `Assignment`: persona, proyecto o centro de costo, rol y vigencia.
- `Attendance`: fecha, entrada, salida, descansos, fuente y versión.
- `RateRule`: concepto, importe o fórmula, moneda, vigencia y versión.
- `Advance`: persona, importe, fecha, autorización y estado.
- `Expense`: centro de costo, concepto, importe, comprobante privado y estado.
- `Payment`: persona, período, moneda, total, estado y referencia de conciliación.
- `LedgerEntry`: cuenta, dirección, importe, moneda, origen, fecha y reversa opcional.
- `Budget`: referencia protegida, partidas, revisiones y estado.
- `AuditEvent`: actor, acción, entidad, fecha y correlación.

Separa datos fiscales, domicilios, contactos, datos bancarios, imágenes y geolocalización en almacenamiento protegido.

## Invariantes

- Usa decimal o unidades monetarias menores; nunca coma flotante binaria.
- Un pago contabilizado no se edita: se revierte y reemplaza.
- Cada tarifa aplicada corresponde a una versión vigente.
- Entrada y salida forman una jornada válida.
- Cada comando admite una clave de idempotencia.
- Los totales coinciden con los movimientos conciliados.
