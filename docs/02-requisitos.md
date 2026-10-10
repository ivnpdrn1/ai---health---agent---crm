# 02 · Requisitos y criterios de aceptación
**Todos los requisitos están pendientes de implementación.** P0: núcleo/piloto; P1: operación ampliada; P2: capacidades posteriores. Prioridad no sustituye fase ni autorización de proveedores.

| ID | Capacidad | Prioridad | Criterio de aceptación | Dependencia |
|---|---|---|---|---|
| R01 | Acceso y MFA | P0 | Usuario invitado entra; usuario revocado pierde sesiones y acceso | Proveedor de identidad |
| R02 | Agencia, roles y alcance | P0 | Agente A no obtiene cartera B por API, búsqueda, documento o exportación | D02 |
| R03 | Cliente y hogar | P0 | Un hogar con varios miembros conserva roles y cambios por año sin duplicar personas | Modelo |
| R04 | Prospectos | P0 | Capturar fuente, dueño y próxima acción; convertir preserva historial | R03 |
| R05 | Pólizas | P0 | Vigencia, pago y solicitud se muestran como hechos independientes, con fuente | R03 |
| R06 | Importación | P0 | Vista previa, errores por fila y reimportación idempotente; sin publicación silenciosa | Mapeo carrier |
| R07 | Documentos | P0 | Subir archivo sintético; URL privada expira; acceso fuera de alcance denegado | Almacenamiento |
| R08 | Evidencia ACA | P0 | Consentimiento y revisión de solicitud separados, versionados y exportables | Revisión de cumplimiento |
| R09 | Tareas y renovaciones | P0 | Tarea con responsable, vencimiento y cierre; renovación crea período nuevo | R05 |
| R10 | Licencias y habilitación | P0 | Bloqueo de acción comercial si habilitación aplicable vencida o desconocida | Fuente autorizada |
| R11 | Auditoría | P0 | Reconstruir cambio con actor, fecha, objeto y motivo; registros protegidos | Diseño de auditoría |
| R12 | Exportación y reportes | P0 | Totales y filas coinciden; se respeta alcance y se audita exportación | R02 |
| R13 | Comisiones importadas | P1 | Lote sintético con positivos, negativos y duplicados se concilia sin doble conteo | R06 |
| R14 | Reparto y liquidación | P1 | Reglas con vigencia; redondeo reproducible; cierre inmutable y ajuste posterior | R13 |
| R15 | Diferencias de cartera | P1 | Diferencia queda como excepción con evidencia y resolución humana | R05/R13 |
| R16 | Correo y SMS | P1 | Consentimiento, supresión, aprobación y entrega/fallo trazables | Proveedor |
| R17 | WhatsApp y bandeja | P1 | Hilo ligado a persona correcta, exclusión activa y relevo a humano | Canal autorizado |
| R18 | Cotización ACA | P1 | Respuesta de sandbox con año, ubicación, fuente y fecha; no simular elegibilidad oficial | Socio |
| R19 | Inscripción ACA | P1 | Ruta autorizada, revisión del consumidor y confirmación externa; error no activa póliza | R08/R10/EDE |
| R20 | Sincronización carrier | P1 | Reintento no duplica; dato atrasado marcado; corrección no destruye historial | Acuerdo carrier |
| R21 | Marketing y campañas | P2 | Segmento, fuente, autorización, presupuesto y exclusiones verificables antes del envío | R16/R17 |
| R22 | Copiloto IA | P2 | Resumen cita registros permitidos; sin evidencia declara desconocimiento | R02/R11 |
| R23 | Acciones IA | P2 | Aprobación ligada al contenido; cambio exige nueva aprobación; ejecución auditable | R22 |
| R24 | Call center y voz IA | P2 | Transferencia humana, consentimiento aplicable y trazabilidad de grabación | Telefonía/revisión |
| R25 | Móvil/PWA | P1 | Flujos clave usables en móvil; salir elimina acceso; sin caché sensible por defecto | R01/R02 |
| R26 | Subagencias y marca | P2 | Herencia explícita de alcance y aislamiento entre organizaciones | R02 |
| R27 | Reclutamiento/contratos | P2 | Candidato, contrato, estado y fecha de habilitación separados | Fuente NPN/contratos |
| R28 | Otras líneas | P2 | Cada producto añade campos/reglas y casos propios sin mezclar ACA/Medicare | Especificación por línea |
| R29 | Recuperación | P0 | Restauración probada en entorno aislado con resultado documentado | Hosting |
| R30 | Calidad y costo operativo | P0 | Métricas de errores, tareas y gasto con alertas; sin datos personales en logs | Observabilidad |

## Cobertura de la referencia
Estas son familias funcionales, no una certificación de paridad. La evaluación de demo debe añadir subfunciones y variantes que no sean visibles públicamente. Registrar por capacidad: anunciado → observado → requisito detallado → implementado → probado → aceptado.
