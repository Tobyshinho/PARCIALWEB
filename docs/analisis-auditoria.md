# Análisis de auditoría — 1001/1005 y 1002

## Límite de evidencia

La guía `EP_Desarrollo_Web_alumno.docx` no llegó en el ZIP ni entre los adjuntos examinados. Tampoco se recibió una exportación de las solicitudes ni del historial. El único hecho de origen disponible sobre los identificadores es lo que afirma el enunciado del usuario: 1001 y 1005 son posibles duplicados; la prioridad de 1002 tuvo un cambio no autorizado indicado por la guía. Por tanto, este informe separa hipótesis de hechos y no inventa valores, personas, fechas, razones ni campos comparativos.

## Posibles duplicados 1001 y 1005

**Conclusión provisional:** candidatos de revisión duplicada, no duplicado confirmado. Un mismo solicitante, tipo o texto parecido puede ser evidencia de similitud, pero no demuestra que ambos registros refieran al mismo incidente.

**Comparación necesaria cuando llegue la fuente:** cotejar solicitante, tipo/categoría, descripción normalizada, equipo o recurso afectado, marcas temporales, estado y referencias a una misma causa. Registrar qué campos coinciden, cuáles difieren y qué valores faltan. Evaluar proximidad temporal y evidencia contextual; no deduplicar solo por texto o persona.

**Tratamiento seguro:** conservar ambos IDs y sus auditorías; pedir revisión humana; si la evidencia confirma relación, marcar uno como relacionado/duplicado por un evento nuevo que contenga actor, instante, motivo y registro sobreviviente. No fusionar ni borrar datos automáticamente en esta práctica. Aquí el procedimiento es conceptual; la interfaz no crea ni modifica solicitudes.

| Elemento               | 1001                                | 1005                                | Evidencia recibida                  |
| ---------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| Campos del registro    | No disponible                       | No disponible                       | Pendiente del DOCX/exportación      |
| Comparación            | No verificable                      | No verificable                      | No concluir hasta revisar la fuente |
| Estado de la hipótesis | Candidato mencionado por el usuario | Candidato mencionado por el usuario | Sin confirmación independiente      |

## Cambio de prioridad de 1002

El usuario describe el cambio como no autorizado y remite a la guía. A efectos del enunciado se registra como **cambio no autorizado reportado**, no como hallazgo reconstruido independientemente: faltan la prioridad anterior y posterior, actor, instante, autorización esperada/otorgada, motivo y evento fuente.

**Comprobación al recibir registros:** reconstruir la secuencia temporal de eventos; comprobar que el actor tuviera rol/autorización a la hora del cambio; comparar valores anterior/nuevo; revisar justificación y referencia de autorización; confirmar si existe reversión válida. Conservar el cambio original en la bitácora, anotar el resultado de revisión como evento separado y no reemplazar el dato histórico. Una corrección propuesta debe identificar actor autorizado, razón y valor restaurado, nunca borrar la traza.

## Reglas de auditoría para el modelo conceptual

1. Toda creación o cambio se agrega como evento inmutable con PK, FK de solicitud y FK del actor.
2. Cada evento registra acción, hora UTC, valor anterior/nuevo cuando corresponda, motivo y referencia de autorización.
3. Los datos de identificación del actor usados en la revisión se conservan conforme a la fuente disponible; no se inventan valores.
4. La asociación 1001/1005 solo se confirma con evidencia suficiente y revisión humana; la mera semejanza no autoriza fusión.
5. La prioridad de 1002 se rastrea cronológicamente; cambios sin permiso comprobable se marcan para investigación, sin suprimir el evento original.

## Pendiente para completar

Adjuntar la guía completa o los extractos de registros 1001, 1005 y la bitácora de 1002. Luego completar la tabla comparativa y citar las páginas/campos fuente. La entrega no debe presentar las hipótesis como un resultado definitivo mientras falten esos insumos.
