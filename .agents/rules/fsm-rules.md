# Reglas Arquitectónicas del Sistema FSM de Telecomunicaciones

1. Stack Tecnológico:
   - Frontend: Angular (señales reactivas, standalone components, offline-ready).
   - Backend: NestJS (arquitectura modular, TypeScript, TypeORM, BullMQ).
   - Base de Datos: PostgreSQL + PostGIS (geocálculo con ST_Contains).
   - Infraestructura: Docker Compose.

2. Seguridad y Credenciales:
   - NUNCA exponer credenciales o modificar el archivo .env en commits.
   - Validar roles con Guards en NestJS (RBAC).

3. Reglas de Negocio Estrictas:
   - Roles: Administrador, Supervisor (alcance zonal), Técnico (aislamiento propio), Cliente (Estándar vs Empresarial).
   - Prioridades de Servicio:
     1. Mantenimiento Correctivo
     2. Instalación
     3. Mantenimiento Preventivo
     4. Actualización
   - Motor de Asignación:
     - No asigna automáticamente a ciegas; genera una recomendación TOP 3 de técnicos idóneos.
     - La confirmación final la realiza el Supervisor o Administrador (Human-in-the-loop).
   - Estados de Solicitud:
     - ROJO: Pendiente
     - AZUL: En curso
     - VERDE: Completada (requiere fotos, material consumido, observaciones y firma del cliente).