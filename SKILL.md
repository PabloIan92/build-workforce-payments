---
name: build-workforce-payments
description: Diseña, implementa, audita o mejora sistemas de personal, asistencia y liquidación de pagos. Úsalo para legajos, asignaciones, jornadas, geolocalización consentida, adelantos, gastos, pagos, presupuestos, reportes y controles antifraude, sin incorporar datos personales, marcas ni credenciales reales.
---

# Build Workforce Payments

Construye sistemas de personal y pagos con trazabilidad y privacidad desde el diseño.

## Flujo de trabajo

1. Aclara jurisdicción, período, roles, monedas, conceptos y fuentes de verdad.
2. Define entidades y cálculos con [data-model.md](references/data-model.md).
3. Diseña altas, asistencia y liquidación con [workflows.md](references/workflows.md).
4. Separa información personal, registros laborales y movimientos financieros.
5. Implementa cálculos deterministas con reglas versionadas.
6. Aplica los controles de [security.md](references/security.md).
7. Prueba redondeos, períodos, duplicados, reversas, permisos y cierres.
8. Entrega migraciones, pruebas, configuración sintética y guía de operación.

## Principios

- Identifica reglas que requieren validación laboral, fiscal o contable local.
- Conserva movimientos financieros como libro inmutable y corrige con reversas.
- Versiona tarifas y reglas con vigencia temporal.
- Obtén consentimiento y minimiza geolocalización.
- Exige revisión humana de alertas antifraude.
- Mantén secretos fuera del código y usa datos sintéticos.

## Alcance

Incluye personal, proyectos o centros de costo, asistencia, jornadas, adelantos, gastos, pagos, saldos, presupuestos, fotografías autorizadas, exportaciones y auditoría. Para agenda de servicios y cuadrillas usa `$build-turn-management`.

## Entregables mínimos

- Matriz de roles y segregación de funciones.
- Modelo de datos y libro de movimientos.
- Especificación versionada de cálculos.
- Controles de privacidad y retención.
- Pruebas de precisión, permisos e idempotencia.
- Variables de entorno documentadas sin valores.
- Plan de conciliación, migración y reversión.
