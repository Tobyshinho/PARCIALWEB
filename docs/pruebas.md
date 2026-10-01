# Registro de pruebas y evidencias

**Rama:** `feature/parcial-portal` (base `main`).

**Fecha:** 30 de septiembre de 2026, zona UTC−5.

**Preview de desarrollo:** <https://8328-izby3er5v25ar6vx368kb-1a7b854d.us4.manus.computer/>

**`ui.js` SHA-256 antes/después:** `9e572529cacf08658d031aa1274769cb356a1ebf3715a4650324f7682af232ae` (sin cambios).

Las evidencias son capturas reales del Preview o del capturador de layout de Webdev; no son mockups. Se marca como aprobado solo lo observado. La guía `EP_Desarrollo_Web_alumno.docx` no estuvo en los adjuntos, por lo que la tabla de casos 1001/1005/1002 es provisional en `analisis-auditoria.md`.

## Matriz de pruebas

| ID  | Prueba                                        | Resultado observado                                                                                                                                                   | Estado y evidencia                                                                                                                     |
| --- | --------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| R1  | Layout a 320 px                               | Vista móvil completa; menú compacto, contenido en columna y controles dentro de la captura.                                                                           | **PASS visual** — `evidencias/vista-320px.png`                                                                                         |
| R2  | Layout a 768 px                               | Breakpoint tablet; tarjetas y formulario legibles.                                                                                                                    | **PASS visual** — `evidencias/vista-768px.png`                                                                                         |
| R3  | Layout a 1440 px                              | Escritorio centrado, catálogo y formulario legibles.                                                                                                                  | **PASS visual** — `evidencias/vista-1440px.png`                                                                                        |
| R4  | Layout a 1024 px (complementario)             | Composición intermedia visible.                                                                                                                                       | **PASS visual** — `evidencias/vista-1024px-complementaria.png`                                                                         |
| R5  | Reflow equivalente a zoom 200 %               | Captura a `640×360`, mitad del viewport base `1280×720`; refluye el portal y aparece el menú compacto. La herramienta no cambió el zoom de la interfaz del navegador. | **PARCIAL** — `evidencias/zoom-200-equivalente.png`. No se afirma que sea zoom nativo; repetir al 200 % en el navegador de escritorio. |
| A1  | Foco por teclado                              | `Tab` enfoca “Saltar al contenido” y el indicador de foco queda visible.                                                                                              | **PASS** — `evidencias/foco-teclado.png`. `Shift+Tab` no quedó registrado.                                                             |
| A2  | Menú móvil y Escape                           | Selectores requeridos presentes y `ui.js` original intacto; no se ejecutó secuencia dinámica móvil de abrir/cerrar/Escape.                                            | **NO VERIFICADO** — confirmar localmente con ventana ≤767 px.                                                                          |
| F1  | Enviar formulario vacío                       | El navegador detiene el envío en el primer campo `required`; no aparece confirmación.                                                                                 | **PASS** — `evidencias/formulario-vacio-required.png`                                                                                  |
| F2  | Nombre con 2 caracteres                       | Con `Al`, el navegador reportó `tooShort: true`; `checkValidity()` fue `false` y no permitió confirmar.                                                               | **PASS** — `evidencias/nombre-minimo-nativo.png`                                                                                       |
| F3  | Correo inválido                               | `no-es-correo` se rechaza con el control nativo `type=email`.                                                                                                         | **PASS** — `evidencias/formulario-invalido.png`                                                                                        |
| F4  | Tipo/prioridad obligatorios y prioridad única | `tipo` es obligatorio; los tres radios comparten `name="prioridad"`. El envío vacío no confirma; con datos válidos quedó marcada solo `media`.                        | **PASS** — capturas vacía/válida y atributos de `public/index.html`.                                                                   |
| F5  | Descripción 10–500 caracteres                 | Con 9, `tooShort: true` y `checkValidity(): false`; HTML declara `minlength=10`, `maxlength=500`. No se ingresaron 501 caracteres.                                    | **PASS** mínimo/atributo máximo — `evidencias/descripcion-minimo-nativo.png`                                                           |
| F6  | Datos ficticios válidos                       | `checkValidity()` fue `true`, tipo `red`, una prioridad `media`; al confirmar apareció el mensaje simulado.                                                           | **PASS** — `evidencias/formulario-valido.png`                                                                                          |
| N1  | Envío/guardado                                | El manejador original ejecuta `preventDefault()` y solo actualiza el estado accesible. No hay backend, API ni persistencia de tickets.                                | **PASS** — inspección de `ui.js`; suite local rechaza POST.                                                                            |
| P1  | Preview y manifiesto                          | HTTP 200 local y público; `manus-routes.json` devuelve la ruta `/`.                                                                                                   | **PASS** — Preview arriba; manifiesto incluido.                                                                                        |
| Q1  | Formato, sintaxis y pruebas provistas         | `npm run check` y `npm run check:syntax` sin errores; `npm test`: 6 pruebas aprobadas, 0 fallidas.                                                                    | **PASS** — ejecución final en el proyecto.                                                                                             |

## Auditoría estructural

El análisis estático confirmó cuatro tarjetas, cinco FAQ en dos categorías, IDs únicos, etiquetas para los campos, un formulario sin `novalidate`, nombre `required`/`minlength=3`, correo `type=email`, tipo obligatorio, grupo de tres radios, descripción `required`/`minlength=10`/`maxlength=500`, `fieldset`/`legend`, al menos tres variables CSS, Grid/Flexbox, CTA directo a `#soporte` y la ruta fuente declarada. El hash de `ui.js` coincide con el original.

## Correcciones reales antes/después

Se observaron dos problemas reproducibles antes de corregirlos y se conservaron capturas del mismo layout antes y después. La causa, ajuste y archivos están descritos en [`evidencias/README.md`](evidencias/README.md); no se presentan defectos supuestos como correcciones.

## GitHub y límites externos

El destino privado confirmado es [PARCIALWEB](https://github.com/Tobyshinho/PARCIALWEB). Tras el rechazo del permiso `Workflows` de la GitHub App, se preparó una variante que omite `.github/workflows/calidad.yml` de toda la historia, conservando las validaciones locales. El SHA que corresponda al ZIP y la URL del Pull Request se entregan solo después de verificar el estado remoto; este registro no declara un PR inexistente.

No se recibió `EP_Desarrollo_Web_alumno.docx`; por tanto, el contenido completo de la guía y los datos fuente de 1001/1005/1002 quedan pendientes de contrastar. El informe provisional está en `analisis-auditoria.md`.
