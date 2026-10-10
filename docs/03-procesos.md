# 03 · Procesos operativos
## Recorrido ACA
1. **Prospecto:** capturar origen, asignación, idioma y preferencias de contacto.
2. **Autorizaciones:** verificar consentimiento para asistencia; permisos de contacto por canal se gestionan por separado.
3. **Hogar:** identificar solicitante, integrantes y personas que buscan cobertura; revisión por agente autorizado.
4. **Evaluación:** determinar mercado, año, necesidades y documentación; no inferir elegibilidad con IA.
5. **Cotización:** recuperar opciones autorizadas y registrar preferencias, fuente y vigencia.
6. **Solicitud:** consumidor revisa/confirma información; agente habilitado utiliza ruta autorizada. Guardar identificador y resultado externo.
7. **Activación:** confirmar cobertura y primer pago con fuente externa. La solicitud enviada no prueba activación.
8. **Servicio:** tareas por documentos, cambios, pagos o dudas; resolución con evidencia.
9. **Renovación:** crear nuevo período; actualizar hogar, autorización y revisión según requisitos aplicables; conservar historia.

## Estados independientes
| Objeto | Estados iniciales de diseño | Regla |
|---|---|---|
| Prospecto | Nuevo, contactado, calificado, cita, convertido, perdido | Conversión conserva fuente |
| Solicitud | Borrador, revisión, lista, enviada, recibida, error | Recibida no equivale a cubierta |
| Cobertura | Desconocida, pendiente, activa, terminada | Transición requiere evidencia |
| Pago de prima | Desconocido, pendiente, confirmado, atraso informado | No inferir desde comisión |
| Comisión | Esperada, recibida, conciliada, liquidada, ajustada | Cada ajuste es registro nuevo |
| Evidencia | Borrador, enviada, completada, revocada/sustituida | Conservar versión aplicable |

Estados finales y códigos de gracia/cancelación se adaptan al carrier: conservar código original y mapeo interno; no generalizar reglas de gracia.

## Importación de cartera
Carga privada → huella del archivo → mapeo versionado → staging → validación y vista previa → resolución de conflictos → confirmación → publicación → reporte. Rechazar o retener filas incompletas. No fusionar personas solo por nombre. Conservar lote, fila, claves externas y operador. Repetir el mismo lote no duplica registros.

## Comisiones
Importar extracto → normalizar moneda/periodo/carrier → asociar póliza → resolver no asociados → comparar con expectativa y contrato → aplicar regla vigente → revisar → cerrar liquidación → registrar pago si se ejecuta externamente.
Ejemplo sintético: ingreso 100 USD; agente 70; override 10; agencia 20. Un chargeback posterior de -100 genera reversos trazables. Confirmar cómo Sunshine distribuye ajustes y centavos residuales.

## Atención y renovación
Priorizar por estado verificable, fecha y responsable; indicadores de riesgo son ayudas, no hechos del carrier. Cerrar alerta exige evidencia o motivo. Cambiar de agente requiere flujo autorizado, historial y revisión correspondiente; no automatizar cambios de NPN.
