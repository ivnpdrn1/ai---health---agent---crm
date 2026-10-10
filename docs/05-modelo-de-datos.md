# 05 · Modelo de datos conceptual
No es todavía un esquema migrable. Cada tabla operativa incluye ID, organización, creación/actualización, actor y versión cuando corresponda.

| Entidad | Contenido y relación |
|---|---|
| Organization | Sunshine y futuras agencias; límites, configuración y estado |
| AgencyUnit | Unidad/subagencia con padre; evitar ciclos |
| User / Membership | Identidad externa, organización, rol y alcance vigente |
| Agent | Persona operativa, NPN y unidades; NPN no equivale a licencia vigente |
| License / Appointment / MarketplaceRegistration | Estado, producto/carrier, vigencia, fuente y verificación separadas |
| Person | Persona única; contacto mínimo; identificadores sensibles separados |
| Household / HouseholdMembership | Miembros, relación y vigencia; no asumir que todos solicitan cobertura |
| CoverageYearSnapshot | Datos del hogar para un año; historial de cambios |
| Lead | Origen/campaña, responsable, estado y conversión |
| Plan / PlanVersion | Carrier, mercado, estado, año, código, fuente y vigencia |
| Quote / QuoteOption | Entradas versionadas, opciones y fecha; respuesta externa |
| Application / ApplicationRevision | Solicitud, revisión confirmada, responsable e identificador remoto |
| Policy / CoveragePeriod / PolicyMember | Póliza, período y personas cubiertas; vínculo a solicitud |
| CoverageObservation / PremiumObservation | Hechos fechados del carrier; estado original y normalizado |
| Document / Evidence / Consent / ApplicationConfirmation | Objeto privado, huella, versión, propósito, actor y evidencia |
| Task / ServiceCase | Responsable, plazo, motivo, enlaces y resolución |
| ImportBatch / ImportRow / MappingVersion | Archivo, staging, validación y publicación |
| CommissionTransaction / CommissionMatch | Ingreso/ajuste con ID fuente y asociación revisada |
| CommissionRule / Allocation | Regla vigente y reparto explicable |
| Settlement / SettlementLine / PaymentRecord | Cierre, líneas y constancia de pago externa |
| ChannelPermission / Suppression | Propósito, canal, alcance, fuente y revocación |
| Conversation / Message / Call | Participantes, canal, entrega y acceso |
| IntegrationConnection / ExternalIdentifier | Proveedor, referencia de secreto y claves externas |
| Approval / ToolExecution | Actor, acción/contenido aprobado, caducidad y resultado |
| AuditEvent / OutboxEvent | Cambio protegible y evento de entrega |

## Invariantes
- Llaves compuestas y relaciones impiden referencias cruzadas entre organizaciones.
- Un miembro puede existir sin póliza; un hogar puede cambiar sin reescribir años cerrados.
- Comisiones no se almacenan como una suma mutable dentro de Policy.
- Liquidación cerrada no se edita: nuevo ajuste vinculado y autorizado.
- Clave única de transacción externa + carrier + organización; duplicados dudosos a revisión.
- Asignación de cartera tiene vigencia, motivo y actor.
- Evidencia de revisión corresponde a una revisión específica de solicitud; cambios relevantes exigen nueva revisión.
- Eventos externos fuera de orden se conservan y reconcilian; no reemplazar el último estado solo por hora de llegada.
- Revocar consentimiento no elimina evidencia histórica cuya conservación sea aplicable.

## Minimización
SSN y documentos completos no son necesarios para el primer prototipo. Si una integración posterior los exige: campos restringidos, cifrado, masking y auditoría específica; nunca ejemplos reales en el repositorio.
