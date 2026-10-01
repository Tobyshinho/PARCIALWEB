# Wireframe — seis zonas

```text
┌────────────────────────────────────────────────────────┐
│ 1. CABECERA / NAVEGACIÓN                               │
│ Marca Portal TI · Servicios · Estados · FAQ · CTA       │
├────────────────────────────────────────────────────────┤
│ 2. PRESENTACIÓN / HERO                                  │
│ Mensaje principal y contexto · CTA directo a #soporte    │
│ Nota clara: práctica; no envía ni guarda tickets        │
├────────────────────────────────────────────────────────┤
│ 3. SERVICIOS                                            │
│ Cuatro tarjetas: Red / Prioritario / Hardware / Software│
│ Una tarjeta destaca; en móvil, una columna               │
├────────────────────────────────────────────────────────┤
│ 4. ESTADOS FICTICIOS                                    │
│ Recibida → En revisión → Orientación lista               │
│ Aviso de que los estados son solo ilustrativos           │
├────────────────────────────────────────────────────────┤
│ 5. SOLICITUD DE SOPORTE                                 │
│ Ayuda/alcance a la izquierda (escritorio)                │
│ Nombre · correo · tipo · prioridad · descripción         │
│ Confirmación accesible sin envío ni persistencia         │
├────────────────────────────────────────────────────────┤
│ 6. FAQ + CONTACTO                                       │
│ Dos categorías y cinco preguntas · correo/horario fict.  │
└────────────────────────────────────────────────────────┘
```

## Comportamiento del layout

En móvil las seis zonas se apilan en una sola columna, la navegación se abre con el botón respaldado por el `ui.js` existente y los controles usan el ancho disponible. Desde 768 px el menú se distribuye horizontalmente, los estados y el formulario pasan a una composición de varias columnas y una tarjeta puede abarcar dos columnas. Desde 1024 px el catálogo alcanza tres columnas y el formulario se divide entre introducción y datos. El contenido conserva el orden semántico en todos los anchos; el CTA principal del hero enlaza al formulario directamente.
