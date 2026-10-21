# Ciclo de Vida del Servicio de Campo

1. Ingesta: Cliente genera ticket (Módulo 2) -> Bloque ROJO (Pendiente).
2. Ponderación: Backend evalúa Zonas (PostGIS), Disponibilidad, Especialidad, Herramientas y Nivel de Cliente.
3. Despacho: Se presenta terna Top 3 al Supervisor/Admin -> Aprobación -> Bloque AZUL (En curso).
4. Ejecución: Técnico recibe la orden en su sesión activa -> Realiza el trabajo.
5. Cierre: Técnico captura formulario de evidencias con firma del cliente -> Bloque VERDE (Completada).