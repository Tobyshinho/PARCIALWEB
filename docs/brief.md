# Brief del proyecto — Portal de Soporte TI

## 1. Audiencia y actores

Personas que buscan ayuda técnica básica para conectividad, atención prioritaria, hardware o software; quienes usan teclado o ampliación de pantalla; y quien evalúa la práctica. En esta entrega no existe agente de soporte real ni cuenta autenticada.

## 2. Necesidad y objetivo

Presentar en una página clara qué áreas de soporte existen, cómo se describiría una incidencia y qué información requiere un formulario accesible. La persona puede validar datos ficticios y ver una confirmación simulada sin enviar ni guardar tickets.

## 3. Alcance funcional

Encabezado/navegación, presentación con CTA al formulario en máximo dos clics, cuatro tarjetas de servicio, estados explícitamente ficticios, formulario nativo, cinco preguntas frecuentes agrupadas en dos categorías y datos/horario de contacto ficticios. La página es de una sola ruta y el modelo de datos es conceptual, no implementado.

## 4. Restricciones y decisiones

HTML y CSS propios, sin frameworks; conservar `assets/js/ui.js` de la guía 2 byte por byte; no añadir JavaScript cliente, backend, API, base de datos ni persistencia de solicitudes. Diseño mobile first; al menos tres variables CSS y uso de Grid o Flexbox; foco visible y zoom utilizable al 200 %. La rama de trabajo solicitada es `feature/parcial-portal` desde `main`. La publicación pública no forma parte del alcance.

## 5. Éxito y medición

- CTA de la presentación alcanza `#soporte` en un clic y el menú conserva sus selectores/función de teclado.
- Se presentan exactamente cuatro tarjetas de servicios, cinco FAQ en dos categorías y estados/contacto identificados como ficticios.
- El formulario aplica validación nativa a nombre (3+ caracteres), correo, tipo, prioridad única y descripción (10–500); válido confirma sin una petición de ticket ni persistencia.
- El layout se prueba a 320, 768 y 1440 px; también se registran zoom 200 %, foco y formularios inválido/válido.
- La entrega contiene documentación, diagrama, evidencias y ZIP reproducible desde el SHA completo declarado.

## Insumos pendientes

No se encontró `EP_Desarrollo_Web_alumno.docx` ni el remoto GitHub dentro de los archivos enviados. La valoración factual de 1001/1005 y 1002 queda limitada a lo afirmado en el enunciado hasta recibir esa fuente.
