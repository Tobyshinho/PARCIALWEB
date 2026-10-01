# Dirección visual — Portal de Soporte TI

## Fuente y dirección elegida

Se conserva la dirección visual heredada de la hoja base aportada: fondo claro `#f5f7fa`, tinta azul marino `#0d1b2a`, azul de acción/foco `#2563eb`, blanco y tipografía `Inter, system-ui, sans-serif`. No se introduce una estética competidora ni se sustituye el punto de partida del alumno.

## Dimensiones de diseño

- **Movimiento:** diseño editorial de servicios digitales, sobrio y funcional; énfasis en claridad antes que decoración.
- **Principios:** orientación inmediata, contenido escaneable, etiquetas persistentes, contraste visible, estados inequívocos y controles táctiles cómodos.
- **Filosofía de color:** marino para estructura y texto principal; blanco y gris azulado para superficies; azul accesible como acento y foco; usar verde/ámbar/rojo solo en etiquetas semánticas de estado, sin depender únicamente del color.
- **Paradigma de layout:** mobile first; ancho centrado máximo de 1200 px; Flexbox para marca/navegación y agrupaciones simples; Grid para servicios/estado; una columna en móvil y columnas graduales en anchos mayores. No ocultar desbordamientos.
- **Elementos distintivos:** hero con CTA primario de al menos 44 px, tarjetas de servicios con una destacada en pantallas aptas, badges de estados ficticios, bloques de FAQ con encabezados claros, ayudas de formulario y un enlace de salto visible al recibir foco.
- **Filosofía de interacción:** HTML nativo primero; navegación por teclado y foco visible; se conserva `assets/js/ui.js` exactamente como fue entregado para menú móvil y confirmación simulada. No agregar scripts, llamadas de red, almacenamiento ni persistencia.
- **Animación:** sin movimiento ornamental; cualquier transición breve debe respetar `prefers-reduced-motion`.
- **Tipografía:** mantener `Inter, system-ui, sans-serif`, texto base de 1 rem y line-height cercano a 1.5; jerarquía por escala, peso y espacio, no por texto diminuto.
- **Esencia de marca:** asistencia confiable, comprensible y humana.
- **Voz de marca:** español neutro, directo, amable y transparente sobre la ficción de tickets/estados.
- **Wordmark/logo:** mostrar “Portal TI” como texto HTML legible, no incrustar letras en un logo rasterizado. Símbolo de proyecto simple de soporte técnico —un escudo geométrico con marca de verificación/soporte— en navy y azul; mantener la silueta reconocible como favicon e icono pequeño.
- **Color de marca distintivo:** azul `#2563eb`, coherente con el `:focus-visible` de la base.

## Reglas de consistencia

1. Conservar reglas base útiles de `styles.css`; definir los colores como custom properties CSS y no dispersar valores duplicados.
2. No usar imágenes de stock ni ilustraciones decorativas que compitan con tareas de soporte; el símbolo del proyecto cumple solo la función de marca.
3. Mantener contenido, iconografía, estados y estilos secundarios legibles con zoom de 200 % y en 320 px.
