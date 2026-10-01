# Plan de trabajo y estado de la entrega

## 1. Insumos y alcance

- Revisar el ZIP de la base y los archivos `index.html`, `styles.css` y `ui.js` entregados por la persona usuaria.
- Respetar HTML/CSS propios, diseño mobile first, `ui.js` intacto, sin JavaScript cliente nuevo, backend, envío ni persistencia.
- **Bloqueo de fuente:** `EP_Desarrollo_Web_alumno.docx` no venía en los adjuntos revisados ni dentro de `Portal_TI_Proyecto_Base_Semana_2.zip`. El brief y el análisis de auditoría se construyeron a partir del enunciado y del ZIP; no se atribuyen al DOCX requisitos no disponibles.

## 2. Rama y estructura de trabajo

- Crear `feature/parcial-portal` desde el `main` del proyecto gestionado.
- Usar commits descriptivos; la rama queda como trabajo no fusionado.
- La variante para GitHub omite `.github/workflows/calidad.yml` de toda la historia porque la GitHub App no pudo escribir workflows. La comprobación de formato, sintaxis y tests continúa disponible localmente.
- El ZIP y el SHA completo que lo identifica se calculan desde el mismo commit final.

## 3. Implementación del portal

- Completar presentación, navegación, CTA directo al formulario, cuatro servicios, estados ficticios, formulario nativo, FAQ en dos grupos, contacto y horario ficticios.
- Mantener el `ui.js` original byte por byte; usar solo su menú y su confirmación simulada existentes.
- Documentar brief de cinco dimensiones, cinco historias con criterios medibles, MoSCoW, wireframe de seis zonas, modelo conceptual de cinco entidades y análisis provisional 1001/1005/1002.
- Mantener el proyecto estático, sin endpoints de ticket, credenciales, persistencia ni publicación.

## 4. Validación y correcciones

- Ejecutar verificaciones de formato, sintaxis y pruebas que ya trae el proyecto; hacer inspección estructural del HTML y comparar el hash de `ui.js`.
- Capturar evidencia a 320, 768 y 1440 px, además de prueba de foco, validación inválida/válida y dos correcciones observadas antes/después.
- Se capturó reflow en `640×360` —el viewport de contenido equivalente a 200 % de `1280×720`— porque la herramienta no cambia el zoom de la interfaz del navegador. La verificación de zoom nativo al 200 % queda pendiente de repetirse localmente.

## 5. Entrega verificable

- Incluir fuente, README, pruebas, diagrama y evidencias en el ZIP.
- Excluir `.git`, secretos, `.env`, `node_modules` y carpetas generadas de despliegue.
- Entregar el enlace del Preview, el repositorio privado [PARCIALWEB](https://github.com/Tobyshinho/PARCIALWEB), el SHA completo de la ZIP y la URL del PR solo después de verificarlos.
- Abrir el PR de `feature/parcial-portal` hacia `main` después de aprobar el SHA exacto; no fusionarlo ni publicar.

## Dependencias y límites externos

1. **DOCX:** falta `EP_Desarrollo_Web_alumno.docx`; la clasificación de 1001/1005 y la reconstrucción del cambio 1002 no puede confirmarse contra la fuente.
2. **GitHub:** el repositorio privado se confirmó mediante el flujo del propietario. La variante sin workflow se prepara para respetar el permiso de GitHub App; no transferirla hasta aprobar su SHA completo y no declarar PR antes de verificar su URL.
3. **Zoom nativo:** falta repetir la comprobación con el control de zoom real del navegador; se adjunta la captura equivalente para documentar reflow, identificada expresamente como tal.
