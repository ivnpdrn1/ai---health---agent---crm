# 11 · Estado y decisiones
Actualizado: 2026-10-10.

## Estado
| Área | Estado verificable |
|---|---|
| Repositorio | Conectado; público; rama main inicializada |
| Documentación | Base inicial con requisitos, procesos y backlog |
| App/código/infraestructura | No implementados |
| Demo/prueba Insurance360CRM | No realizadas |
| Datos y reglas Sunshine | Pendientes de levantamiento |
| Proveedores y acuerdos | No seleccionados/confirmados |
| Pruebas de software | No ejecutadas |
| Automatización de seguimiento | No configurada |

## Preguntas que desbloquean B02
1. Agentes activos, supervisores, asistentes y unidades; acceso esperado.
2. Cantidad de hogares/pólizas y máximos durante Open Enrollment.
3. Productos, carriers y estados usados primero.
4. CRM/hojas actuales y exportaciones disponibles; ejemplos sanitizados o sintéticos.
5. Reglas de comisiones: contratos, overrides, chargebacks, vigencia y cierre.
6. Socios actuales de cotización/inscripción y derechos API.
7. Canales/cuentas existentes; proceso de consentimiento y exclusión.
8. Quién acepta el piloto, quién opera soporte y rango de inversión.
No bloquear redacción por estas preguntas; sí bloquear decisiones que requieren sus respuestas.

## Decisiones
| ID | Tema | Estado | Criterio |
|---|---|---|---|
| D01 | Stack/hosting | Propuesto | Costo, operación, seguridad y acuerdos |
| D02 | Roles y aislamiento | Pendiente | Validación Sunshine y pruebas negativas |
| D03 | Identidad/MFA | Pendiente | Revocación, soporte y costo |
| D04 | Socio inscripción | Pendiente | Aprobación/ruta y mercados cubiertos |
| D05 | Modelo comisiones | Pendiente | Contratos y conciliación |
| D06 | Documentos/retención | Pendiente | Reglas por categoría y recuperación |

Confirmado por instrucción del usuario: usar este repositorio para organizar y desarrollar el proyecto sistemáticamente. Propuesta: especialización ACA inicial y expansión por fases. El documento no constituye aprobación de presupuesto o producción.

## Riesgos concretos
Acceso a proveedores sin confirmar; calidad de datos desconocida; reglas financieras por levantar; alcance multestado; cambios regulatorios por año; exposición accidental en repo público; paridad de referencia aún no observada.
Mitigaciones y responsables deben asignarse en descubrimiento; no presentar riesgos como resueltos.

## Siguiente paso
B02 + B03: levantar operación Sunshine y evaluar demo. B04/B05: decidir base técnica. Después, B06–B12 construyen primer incremento. Entregar cada tarea con plantilla y evidencia.

## Bitácora
2026-10-10: repositorio vacío confirmado; lectura pública de referencia y fuentes CMS; base documental inicial. Ningún módulo declarado implementado.
