# Requisitos del sistema

## Roles
- **Usuario:** crea tickets y ve solo los suyos.
- **Agente:** atiende tickets, cambia estados y comenta.
- **Admin:** gestiona usuarios, categorías y ve todas las métricas.

## Requisitos funcionales
- RF01: Registro e inicio de sesión con JWT.
- RF02: Control de acceso por rol.
- RF03: CRUD de tickets (título, descripción, categoría, prioridad).
- RF04: Estados: abierto, en progreso, en espera, resuelto, cerrado.
- RF05: Asignación de tickets a agentes.
- RF06: Comentarios por ticket.
- RF07: Historial automático de cambios por ticket.
- RF08: Dashboard con métricas (abiertos, por prioridad, tiempo medio de resolución).
- RF09: Notificaciones por Telegram con botones "Tomar" y "Cerrar".
- RF10: SLA: escalamiento automático de tickets sin atender.
- RF11: Búsqueda y filtros por estado, prioridad y categoría.

## Requisitos no funcionales
- RNF01: Contraseñas con hash (bcrypt); ningún secreto en el repositorio.
- RNF02: API documentada con OpenAPI/Swagger.
- RNF03: Cobertura de pruebas mínima del 70 % en el backend.
- RNF04: Ejecutable con `docker compose up`.
- RNF05: CI automático en cada Pull Request.

## Historias de usuario
- Como usuario, quiero crear un ticket para reportar un problema.
- Como usuario, quiero ver el estado de mis tickets para saber si avanzan.
- Como agente, quiero ver la cola de tickets por prioridad para atender primero lo urgente.
- Como agente, quiero tomar un ticket desde Telegram para responder rápido.
- Como agente, quiero comentar y cambiar el estado para mantener informado al usuario.
- Como admin, quiero ver métricas para medir el desempeño del soporte.
- Como admin, quiero gestionar categorías y usuarios.
- Como admin, quiero que los tickets sin atender escalen solos para cumplir los SLA.