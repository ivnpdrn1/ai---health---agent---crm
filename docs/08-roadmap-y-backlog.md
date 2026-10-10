# 08 · Roadmap y backlog
## Etapas por evidencia
| Fase | Entrega | Puerta para avanzar |
|---|---|---|
| F0 Definición | Alcance, datos sintéticos, demo, decisiones y backlog | Sunshine valida flujo mínimo; stack y permisos decididos |
| F1 Núcleo | Acceso, hogar, póliza, importación, evidencia, tareas y exportación | Recorrido sintético completo; aislamiento y restauración probados |
| F2 Finanzas/servicio | Comisiones, reglas, liquidaciones y renovación | Período sintético conciliado; revisión de caso operativo |
| F3 Ventas conectadas | Cotización, inscripción y canales | Acuerdos vigentes y casos sandbox; piloto autorizado |
| F4 IA/call center | Copiloto, aprobaciones y voz | Calidad, permisos, transferencia y costo medidos |
| F5 Expansión | Nuevas líneas, subagencias y comercialización | Casos propios, aislamiento y soporte aceptados |

Sin duración prometida. Estimar después de datos, proveedores y criterios aprobados.

## Backlog ordenado
Todos pendientes salvo B01, completado documentalmente. Dependencias no resueltas bloquean tarea.
| ID | Trabajo | Requisitos | Depende de | Resultado verificable |
|---|---|---|---|---|
| B01 | Base documental | Todos | — | Índice, matriz, arquitectura y seguimiento publicados |
| B02 | Descubrimiento Sunshine | R03–R20 | B01 | Volumen, productos, carriers, roles y muestra sintética |
| B03 | Demo/prueba referencia | Todos | Acceso proveedor | Casos observados y diferencias registradas |
| B04 | ADR stack/hosting | R01/R29/R30 | B02 | Decisión con costos, acuerdos y alternativa |
| B05 | ADR permisos/identidad | R01/R02 | B02 | Matriz por acción y plan de pruebas |
| B06 | Esquema y migraciones | R03/R05/R11 | B04/B05 | Restricciones y entidades de F1 migrables |
| B07 | Login/alcance/auditoría | R01/R02/R11 | B06 | Pruebas negativas y revocación |
| B08 | Hogar y cartera | R03/R04/R05 | B07 | Recorrido ficticio y cambios por año |
| B09 | Importación cartera | R06 | B08/B02 | Preview, idempotencia y excepciones |
| B10 | Evidencia y archivos | R07/R08 | B07/revisión | Recuperación segura y versión |
| B11 | Habilitación/tareas/renovación | R09/R10 | B08 | Bloqueos y responsable por caso |
| B12 | Reportes/exportación/recuperación | R12/R29/R30 | B09–B11 | Totales correctos y restauración |
| B13 | Reglas financieras y comisiones | R13/R14/R15 | B02/B09 | Conciliación, reparto, cierre y ajuste |
| B14 | Socios y matriz de mercados | R18/R19/R20 | B02 | Derechos, cobertura, sandbox y contrato |
| B15 | Canales y móvil | R16/R17/R25 | B10/B14 | Prueba de envío y exclusión |
| B16 | Cotización/inscripción | R18/R19 | B10/B11/B14 | Caso autorizado y recuperación de error |
| B17 | Copiloto y acciones | R22/R23 | F3/R02/R11 | Evaluación sintética y aprobación |
| B18 | Telefonía/marketing | R21/R24 | B15/B17/revisión | Transferencia, exclusión y topes |
| B19 | Expansión | R26/R27/R28 | F4 | Especificación y pruebas por línea |

## Listo para empezar / terminado
Listo: problema concreto, dependencia resuelta, datos sintéticos, aceptación y límites.
Terminado: implementación o documento entregado, aceptación comprobada, evidencia, enlaces y estado actualizados. Una tarea bloqueada registra causa y siguiente acción.

## Cadencia
Al cerrar cada sesión: actualizar registro y estado. Revisar semanalmente backlog, bloqueos y riesgos. No existe una actualización automática diaria configurada.
