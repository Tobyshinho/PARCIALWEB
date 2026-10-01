# Índice de evidencias

Las imágenes son capturas del portal real durante esta práctica. `antes-*` corresponde al mismo sitio antes de las correcciones; `vista-*` es la captura posterior. El detalle de pruebas y límites está en [`../pruebas.md`](../pruebas.md).

## Dos correcciones reales

### 1. No marcar como error todos los controles requeridos al abrir

- **Antes:** `antes-01-mobile-320.png` muestra bordes rojos en los campos obligatorios vacíos incluso antes de intentar completar o enviar el formulario.
- **Corrección:** ajustar los estados visuales para que el énfasis de error no aparezca anticipadamente en controles aún no interactuados; conservar el mensaje de ayuda y la validación HTML nativa.
- **Después:** `vista-320px.png`; los campos iniciales se presentan neutrales y la advertencia nativa aparece al enviar un formulario vacío en `formulario-vacio-required.png`.

### 2. Retirar el adorno que competía con el enlace del hero

- **Antes:** `antes-02-desktop-1440.png` muestra un anillo decorativo superpuesto/competitivo en la tarjeta de presentación, cerca de su enlace de estados.
- **Corrección:** retirar ese ornamento para despejar el área interactiva y mantener el texto y el enlace legibles.
- **Después:** `vista-1440px.png` muestra el enlace sin esa interferencia visual.

Estas dos diferencias se basan en las capturas guardadas y no son ejemplos fabricados. El código de ambas correcciones queda en la rama `feature/parcial-portal`; el SHA del commit final se entrega junto con el ZIP.

## Capturas finales solicitadas

| Evidencia                  | Archivo                           | Descripción                                                                                                                                       |
| -------------------------- | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Móvil                      | `vista-320px.png`                 | Página completa a 320 px.                                                                                                                         |
| Tablet                     | `vista-768px.png`                 | Página completa a 768 px.                                                                                                                         |
| Escritorio                 | `vista-1440px.png`                | Página completa a 1440 px.                                                                                                                        |
| Complementaria             | `vista-1024px-complementaria.png` | Página completa a 1024 px.                                                                                                                        |
| Teclado                    | `foco-teclado.png`                | `Tab` sobre el enlace “Saltar al contenido”, con foco visible.                                                                                    |
| Formulario vacío           | `formulario-vacio-required.png`   | Validación nativa del primer campo obligatorio.                                                                                                   |
| Nombre corto               | `nombre-minimo-nativo.png`        | El navegador rechaza “Al” con `minlength=3`.                                                                                                      |
| Correo inválido            | `formulario-invalido.png`         | El navegador rechaza texto que no cumple `type=email`.                                                                                            |
| Descripción corta          | `descripcion-minimo-nativo.png`   | El navegador rechaza 9 caracteres frente al mínimo de 10.                                                                                         |
| Confirmación válida        | `formulario-valido.png`           | Mensaje simulado con datos ficticios; no se crea un ticket.                                                                                       |
| Reflow equivalente a 200 % | `zoom-200-equivalente.png`        | Viewport `640×360`, equivalente en ancho/alto útil a ampliar 200 % desde `1280×720`; no es una captura con el control de zoom nativo del browser. |

## Alcance de estas imágenes

El Preview es un entorno de desarrollo, no un sitio publicado. En las capturas del formulario se usaron únicamente datos ficticios (`Ana Demo`, `ana@example.test`, tipo Red, prioridad Media). Las notificaciones de validación las genera el navegador y su idioma puede diferir del idioma del portal.
