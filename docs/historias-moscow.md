# Historias de usuario y prioridades MoSCoW

## Historias y criterios de aceptación

### H1 — Encontrar y abrir el formulario

Como persona usuaria, quiero identificar el portal y llegar a soporte sin buscar en toda la página.

**Criterios medibles:** el hero muestra un CTA enlazado a `#soporte`; desde el hero se llega al formulario en 1 clic (≤2); el enlace “Saltar al contenido” apunta al único `main`; la navegación conserva `.navbar`, `.navbar__toggle` y `#nav-menu` para que opere `ui.js` sin cambios.

### H2 — Reconocer el tipo de ayuda disponible

Como persona usuaria, quiero comparar las áreas de soporte antes de describir mi necesidad.

**Criterios medibles:** se presentan exactamente cuatro `article` en `.services__grid`: Red, Prioritario, Hardware y Software; usan CSS Grid; la tarjeta destacada solo abarca dos columnas desde 768 px; a 320 px no provoca desplazamiento horizontal.

### H3 — Probar una solicitud sin crear un ticket

Como estudiante, quiero probar las restricciones del formulario y ver una confirmación simulada sin enviar datos.

**Criterios medibles:** nombre `required` y `minlength=3`; correo `type=email` y `required`; tipo `required`; tres radios de prioridad con el mismo `name` y selección única; descripción `required`, `minlength=10` y `maxlength=500`; existe `label` para cada control y `fieldset`/`legend` para prioridad; no existe `novalidate`; `#submit-demo` comienza `disabled`; con `ui.js` intacto, un caso nativo inválido no confirma y un caso válido muestra “Validación completada. No se envió ni guardó ningún ticket.” sin solicitud de red ni persistencia.

### H4 — Consultar ejemplos de seguimiento y orientación

Como persona usuaria, quiero entender el flujo de soporte y resolver dudas frecuentes.

**Criterios medibles:** se muestran ≥3 estados expresamente identificados como ilustrativos, exactamente cinco preguntas frecuentes agrupadas bajo exactamente dos categorías, un correo `.test` ficticio y horario ficticio claramente rotulado.

### H5 — Usar el portal en varios tamaños y con teclado

Como persona usuaria, quiero leer y operar el portal en móvil, escritorio y con teclado.

**Criterios medibles:** se comprueba el render a 320, 768 y 1440 px; se prueba zoom al 200 %; Tab/Shift+Tab permite recorrer controles y `:focus-visible` dibuja un indicador discernible; botones y enlaces principales tienen al menos 44 px de altura; no hay scroll horizontal en los anchos requeridos.

## Priorización MoSCoW

| Prioridad  | Alcance                                                                                                                                                                                                                                                                                                                     |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Must**   | Estructura de portal, navegación y CTA ≤2 clics, cuatro servicios, formulario con todas las restricciones y confirmación simulada, estados ficticios, cinco FAQ/dos categorías, contacto/horario ficticios, CSS mobile first, accesibilidad básica, `ui.js` inalterado, documentación, modelo y ZIP/evidencias solicitados. |
| **Should** | Evidencia del análisis de 1001/1005 y 1002 basada en el DOCX/registros fuente; Preview y PR asociados a un repositorio confirmado.                                                                                                                                                                                          |
| **Could**  | Añadir comprobación visual a 1024 px como extensión de la guía del ZIP; pequeñas mejoras decorativas coherentes que no afecten legibilidad ni alcance.                                                                                                                                                                      |
| **Won’t**  | Backend, base de datos, almacenamiento, envío de solicitudes, tickets reales, autenticación, frameworks, JavaScript de cliente nuevo o publicación pública no solicitada.                                                                                                                                                   |

## Supuestos de prueba

Los nombres, correos y descripciones utilizados en evidencia serán ficticios. Los criterios H4 y las descripciones del caso de auditoría no se consideran verificados si falta la guía o el registro fuente.
