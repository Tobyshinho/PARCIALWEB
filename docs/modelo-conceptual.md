# Modelo conceptual (sin persistencia en esta práctica)

El diagrama muestra exactamente cinco entidades conceptuales; no crea tablas ni almacena tickets en la aplicación.

| Entidad            | PK             | FK                                                             | Uso conceptual                                                   |
| ------------------ | -------------- | -------------------------------------------------------------- | ---------------------------------------------------------------- |
| `PERSONA`          | `id_persona`   | —                                                              | Solicitante o actor de auditoría.                                |
| `TIPO_SOLICITUD`   | `id_tipo`      | —                                                              | Catálogo de categorías como red, hardware o software.            |
| `PRIORIDAD`        | `id_prioridad` | —                                                              | Catálogo de niveles de prioridad.                                |
| `SOLICITUD`        | `id_solicitud` | `id_persona`, `id_tipo`, `id_prioridad`                        | Descripción, estado y fecha de creación.                         |
| `EVENTO_AUDITORIA` | `id_evento`    | `id_solicitud`, `id_actor` (referencia a `PERSONA.id_persona`) | Acción, valores anterior/nuevo, motivo, autorización y hora UTC. |

## Cardinalidades

- `PERSONA 1 — N SOLICITUD`: una persona puede crear varias solicitudes; cada solicitud se atribuye a una persona.
- `TIPO_SOLICITUD 1 — N SOLICITUD`: cada solicitud tiene un tipo; cada tipo clasifica muchas solicitudes.
- `PRIORIDAD 1 — N SOLICITUD`: cada solicitud tiene una prioridad a la vez; un nivel puede asignarse a varias solicitudes.
- `SOLICITUD 1 — N EVENTO_AUDITORIA`: una solicitud acumula eventos; cada evento refiere a una solicitud.
- `PERSONA 1 — N EVENTO_AUDITORIA`: una persona puede actuar en muchos eventos; cada evento registra un actor identificable.

## Reglas de auditoría

Los eventos son append-only: no se sobrescriben ni eliminan. Cada cambio registra actor, solicitud, acción, instante UTC, valor anterior/nuevo, motivo y referencia de autorización; los eventos de creación y de cambio de prioridad se conservan. Una posible relación duplicada entre 1001 y 1005 requiere comparación de campos y revisión humana; nunca se fusiona solo por similitud. La prioridad de 1002 se examina cronológicamente y cualquier cambio reportado como no autorizado se investiga conservando su traza original; no se corrige ni borra de forma silenciosa.

La fuente `.mmd` es el diagrama editable; el PNG se incluye como render para lectura rápida. Consulte también [`analisis-auditoria.md`](analisis-auditoria.md) para límites y datos fuente pendientes.
