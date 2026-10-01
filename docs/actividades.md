# Actividades y plan de trabajo de la entrega

## Completadas

- Se importó la base del ZIP al proyecto Manus-managed y se creó `feature/parcial-portal` desde `main`.
- Se completaron estructura y contenido semántico del portal con navegación, presentación y CTA al formulario en un clic, cuatro servicios, estados ficticios, formulario, cinco FAQ en dos categorías y contacto/horario ficticios.
- Se conservaron las reglas de `public/assets/js/ui.js` sin modificar; se verificó su hash SHA-256 antes/después.
- Se implementaron estilos propios mobile first con variables CSS, Grid/Flexbox, estados de foco y validación visual sin ocultar overflow.
- Se redactaron brief de cinco dimensiones, cinco historias con criterios medibles, prioridades MoSCoW, wireframe de seis zonas y diagrama conceptual de cinco entidades con PK/FK, cardinalidades y reglas de auditoría.
- Se documentó el análisis provisional de 1001/1005 y 1002; la fuente DOCX no se recibió y el informe conserva explícitamente esa limitación.
- Se capturaron evidencias a 320/768/1440 px, foco, formularios vacío/inválido/válido y dos correcciones reales antes/después. Se añadió 1024 px como comprobación complementaria.
- Se verificó el reflow en un viewport de 640×360, equivalente al espacio de contenido de 200 % sobre 1280×720; no se afirma que el control de zoom nativo haya sido activado.

## Pendiente por insumos externos

- Adjuntar `EP_Desarrollo_Web_alumno.docx` para verificar requisitos y contrastar los datos fuente de 1001, 1005 y 1002.
- Confirmar/proporcionar el repositorio GitHub existente y acceso compatible con el flujo Manus-managed para abrir el Pull Request de `feature/parcial-portal` hacia `main`.
- Repetir la prueba del 200 % usando el control nativo del navegador de escritorio.

El detalle del estado de pruebas se mantiene en [`pruebas.md`](pruebas.md); el procedimiento final está en [`plan-implementacion.md`](plan-implementacion.md).
