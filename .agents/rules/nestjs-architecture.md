# NestJS Architecture & Best Practices

## Principios de Arquitectura
- Separación estricta de responsabilidades: Controladores (HTTP/Rutas), Servicios (Lógica de Negocio) y Módulos.
- Utilizar DTOs (Data Transfer Objects) con `class-validator` y `class-transformer` para validar la entrada de datos en cada endpoint.
- Mantener la lógica de negocio fuera de los controladores.

## Estructura de Módulos FSM
- Organizar el código por módulos de dominio: `users`, `technicians`, `service-orders`, `auth`.
- Usar inyección de dependencias para mantener los servicios desacoplados y facilitar pruebas unitarias con Vitest.
- Retornar siempre respuestas estructuradas y manejar excepciones usando `HttpException` o filtros globales.