# 07 · Integraciones y dependencias
**Todas pendientes de selección y acceso.** Una pantalla no acredita integración.

| Integración | Inicio | Prueba requerida | Información por obtener |
|---|---|---|---|
| Cartera carrier | CSV validado | Dos importaciones sin duplicar; conflictos visibles | Archivos sintéticos, claves, estados y frecuencia |
| Comisiones carrier | CSV con staging | Positivos, negativos, reimportación y cierre | Reglas y formatos por carrier |
| Cotización ACA | Socio autorizado/sandbox | Año/mercado correcto; error y expiración | API, derechos, costo y cobertura |
| Inscripción ACA | Ruta EDE aprobada | Flujo de revisión y confirmación externa | Contrato, alcance upstream/downstream y auditoría |
| Mercados estatales | Matriz por estado | Ruta disponible verificada | Proveedores/rutas por mercado |
| Licencias/NPN | Registro verificado inicialmente | Vencido/desconocido bloquea acción aplicable | Fuente autorizada y cadencia |
| Email/SMS/WhatsApp | Sandbox y destinatarios de prueba | Entrega, fallo, exclusión y reintento | Cuentas, plantillas, registro y tarifas |
| Telefonía/voz | Proveedor evaluado | Transferencia, grabación y acceso | Consentimiento aplicable, costo, retención |
| Firma/documentos | Flujo de evidencia revisado | Recuperar versión y prueba de acción | Identidad, plantilla y proveedor |
| IA | Adaptador de prueba sintético | Recuperación permitida y aprobación | Privacidad, región, retención y costo |
| Anuncios/marketing | Posterior | Exclusiones y aprobación de campaña | Cuentas y reglas por plataforma |

## EDE
CMS describe opciones de entidad primaria, upstream y agente/broker downstream; recomienda usar la lista de entidades aprobadas para posibles socios. La elegibilidad oficial la determina el Exchange. Recomendación del proyecto: evaluar socio antes de infraestructura EDE propia.
[Fuente oficial CMS](https://www.cms.gov/marketplace-private-insurance/agents-brokers/direct-enrollment-partners).

## Por estado
Construir inventario: estado, mercado/plataforma, producto, carrier, socio, año, agente habilitado y fecha de comprobación. Operar en 50 estados no demuestra que una API cubra los 50.

## Contrato de adaptador
Autenticación, scopes, sandbox, versión de esquema, clave idempotente, firma de webhook, límites, errores, timeout, reintentos, reconcilación y exportabilidad.
Pedir derechos de acceso/uso, condiciones de automatización, soporte, privacidad y salida. No utilizar credenciales prestadas ni scraping como sustituto de autorización.

## Fallos esperables
Proveedor caído: conservar caso pendiente y aviso; datos antiguos: marcar antigüedad; webhook duplicado: ignorar efecto repetido conservando trazabilidad; fila desconocida: excepción; timeout de inscripción: consultar estado remoto antes de repetir.
