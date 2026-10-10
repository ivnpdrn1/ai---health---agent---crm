# 06 · Seguridad, permisos y cumplimiento
## Matriz inicial
A = autorizado dentro de alcance; L = lectura limitada; — = denegado. Detallar por acción en D02 antes de implementar.

| Rol | CRM/cartera | Evidencia | Liquidaciones | Equipo/configuración | Auditoría |
|---|---|---|---|---|---|
| Admin | A agencia | A | A con rol financiero | A | L |
| Supervisor | A unidad autorizada | A unidad | L si se concede | L unidad | L unidad |
| Agente | A asignados | A asignados | L propias publicadas | — | — |
| Servicio | A alcance asignado | A alcance asignado | — | — | — |
| Finanzas | L mínimo necesario | L justificado | A | — | L financiera |
| Auditor | L alcance de revisión | L | L | — | L |

A no autoriza automáticamente inscripción, envío externo o cierre financiero. Evaluar rol + alcance + finalidad + habilitación + estado del caso. Superadmin técnico tampoco implica acceso ilimitado a datos.

## Controles de piloto
MFA; revocación de sesiones; secreto administrado; TLS; cifrado; URLs de documento con expiración; eventos de acceso/exportación; copias privadas; restauración probada; logs sin contenido sensible; separación de entornos.
Probar autorización en detalle, listados, búsqueda, archivos, exportación, worker e IA. Habilitar detección de accesos indebidos, respuesta a incidentes y responsable operativo.

## Evidencia ACA
CMS documenta consentimiento del consumidor y revisión/confirmación de la solicitud antes del envío. La presentación oficial consultada establece conservación mínima de **10 años** para ambas evidencias. Diseñar propósito, nombres, fecha, agente, versión y recuperación. Validar plantilla y procedimiento para el mercado y año antes del piloto.
Fuente: [CMS, Marketplace Compliance, pp. 10–11](https://www.cms.gov/files/document/marketplace-compliance-agents-and-brokers.pdf).

Los permisos comerciales por canal, grabación, firma y supresión requieren evaluación propia; un consentimiento ACA no autoriza por sí solo marketing o llamadas automatizadas. Configurar por finalidad, canal, jurisdicción y vigencia.

## Aplicabilidad por confirmar
Responsable de cumplimiento determina obligaciones federales/estatales, contratos de privacidad, proveedores y posible aplicabilidad HIPAA/BAA según roles y datos. No declarar certificación o cumplimiento global desde esta documentación. Revisión también para Medicare y nuevas líneas.
Retención por categoría: evidencia ACA; documentos; comunicaciones; finanzas; logs. Registrar plazo, base, restricción de borrado, excepción legal y método de eliminación. No establecer un plazo universal.

## IA
No entrenar con datos de clientes por defecto. Evaluar condiciones del proveedor y minimización. Filtrar recuperación por permisos; defender contra instrucciones maliciosas en documentos. Aprobar contenido concreto antes de acciones externas; revalidar permisos y consentimiento al ejecutar. Incluir límites de costo, parada y transferencia humana.
