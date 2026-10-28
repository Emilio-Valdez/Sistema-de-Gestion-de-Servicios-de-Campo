# Angular Best Practices & Component Guidelines

## Estándares de Componentes
- Utilizar componentes Standalone (`standalone: true`).
- Emplear **Signals** para la gestión de estado reactivo local (`signal()`, `computed()`, `effect()`).
- Estructurar el layout en capas: Componentes contenedores (Smart) y componentes de presentación (Dumb).

## Manejo de Datos y Formularios
- Utilizar `ReactiveFormsModule` para formularios de captura de datos en campo.
- Implementar Guards de enrutamiento para proteger las vistas por rol (Administrador / Técnico).