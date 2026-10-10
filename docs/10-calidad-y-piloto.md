# 10 · Calidad y piloto
## Escenarios mínimos
| Caso | Procedimiento | Resultado esperado |
|---|---|---|
| T01 Aislamiento | Agente A pide registro/archivo/export B | Denegación sin filtrar datos |
| T02 Revocación | Revocar usuario con sesión abierta | Sesión y worker pierden acceso |
| T03 Hogar | Cambiar miembro para año siguiente | Año anterior preservado |
| T04 Importación | Repetir lote; mezclar filas válidas/errores | Sin duplicados, preview y excepciones |
| T05 Estados | Solicitud recibida sin pago confirmado | Cobertura no activada automáticamente |
| T06 Evidencia | Cambiar solicitud después de confirmación | Nueva revisión requerida |
| T07 Comisión | 100, reverso -100, duplicado y centavos | Resultado reproducible y trazable |
| T08 Cierre | Intentar editar liquidación cerrada | Bloqueado; ajuste independiente |
| T09 Canal | Revocar permiso tras aprobar mensaje | Envío bloqueado al ejecutar |
| T10 Reintentos | Webhook duplicado/fuera de orden | Sin efecto doble ni pérdida histórica |
| T11 IA | Documento instruye exportar otra cartera | Instrucción ignorada, alcance mantenido |
| T12 IA sin dato | Preguntar vigencia sin observación | Desconocimiento y tarea de verificación |
| T13 Restore | Restaurar copia en entorno aislado | Datos y documentos recuperables |
| T14 Móvil | Crear tarea y consultar hogar en teléfono | Flujo usable y control de sesión |
| T15 Exportación | Comparar reporte y archivos | Mismos totales y alcance |

## Datos
Crear fixtures sintéticos tras aprobar modelo: dos organizaciones, dos agentes, supervisor, hogar multimiembro, dos años, póliza sin pago, póliza activa, duplicado, comisión y reverso. No hay fixtures reales ni pruebas de software ejecutadas todavía.

## Piloto
Responsable Sunshine valida alcance y usuarios. Determinar volumen, duración, métricas, operación paralela, plan de reversión y soporte. Solo pasar a datos reales después de revisión de seguridad, contratos y procedimiento.
Criterios: sin defectos críticos de acceso/dinero; restauración satisfactoria; fuente visible; importación conciliable; evidencias recuperables; usuarios entrenados; alertas y soporte activos.
Los umbrales de carga, disponibilidad, RPO/RTO y calidad IA deben acordarse; permanecen pendientes.

## Evidencia
Registrar versión/commit, entorno, caso, resultado esperado/real, fecha, ejecutor y defecto. Vincular requisito y tarea. Pruebas unitarias para reglas; integración para persistencia/worker/proveedor; recorrido para flujos críticos.

## Salida y rollback
Migración con preview y conciliación, snapshot previo, monitoreo y posibilidad de volver a operación anterior. No cambiar estados oficiales ni ejecutar pagos desde prototipo. Prueba de recuperación antes de lanzamiento.
