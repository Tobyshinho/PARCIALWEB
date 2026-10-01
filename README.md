# Portal de Soporte TI — práctica académica

Portal estático de soporte hecho con HTML y CSS propios. La página presenta servicios, estados y contacto ficticios; la solicitud usa validación HTML nativa y solo muestra una confirmación simulada. **No envía ni guarda tickets.** El archivo `public/assets/js/ui.js` es el apoyo de la guía 2 y debe permanecer sin cambios.

## Abrir en Visual Studio Code

1. Descomprime la entrega y abre en VS Code la carpeta raíz que contiene `package.json`.
2. Usa **Terminal → New Terminal** y confirma que la terminal está en esa carpeta.
3. Requiere Node.js 22 o superior. Ejecuta `npm ci` una vez y `npm run dev`; el servidor local de la guía anuncia `http://127.0.0.1:5500`.
4. Guarda `public/index.html` o `public/assets/css/styles.css` y recarga el navegador. Detén el servidor local con `Ctrl+C`.

El Preview del proyecto gestionado es una vista de desarrollo separada del servidor local. El sitio no está publicado en producción ni se configuró backend.

## Estructura

- `public/index.html`: navegación, presentación, cuatro servicios, estados de ejemplo, formulario, FAQ y contacto.
- `public/assets/css/styles.css`: tokens visuales, responsive mobile first, Grid/Flexbox y estados de foco.
- `public/assets/js/ui.js`: archivo de apoyo original; conserva menú móvil y confirmación simulada.
- `public/assets/brand/portal-ti-icon.svg`: símbolo/favicon del proyecto.
- `public/manus-routes.json`: declaración de la ruta fuente `/`.
- `docs/`: plan de trabajo, brief, historias y MoSCoW, wireframe, diagrama, auditoría, pruebas y evidencias.
- `scripts/` y `tests/`: servidor local y pruebas ya incluidos en la base.

## Formulario de práctica

Nombre: obligatorio, mínimo 3 caracteres. Correo: obligatorio y con formato de correo. Tipo: obligatorio. Prioridad: se selecciona una opción. Descripción: obligatoria, mínimo 10 y máximo 500 caracteres. Se usan `label`, `fieldset`/`legend` y validación nativa; no hay `novalidate`. No completar con datos personales: usa exclusivamente datos ficticios. La confirmación no conserva los campos.

## Comprobaciones

```bash
npm ci
npm run check
npm run check:syntax
npm test
```

Consulta [`docs/pruebas.md`](docs/pruebas.md) para los resultados reales y la evidencia. Una prueba solo se marca como aprobada después de ejecutarla.

## Entrega y Git

La rama solicitada es `feature/parcial-portal`, creada desde `main`. El SHA final, URL de Preview, URL de repositorio y PR se completarán solo con valores verificados. La URL del repositorio GitHub no estaba incluida entre los insumos recibidos; la entrega no inventa el remoto ni el PR.

Tampoco se recibió `EP_Desarrollo_Web_alumno.docx`; el análisis de 1001/1005 y 1002 es provisional y distingue hechos reportados de hipótesis pendientes de contrastar.

El ZIP excluye `.git`, secretos, `.env`, `node_modules` y carpetas de despliegue. El modelo conceptual es documentación: no crea tablas ni persistencia real. La captura llamada `zoom-200-equivalente.png` usa 640×360 como espacio de contenido equivalente; no sustituye una prueba con el zoom nativo del navegador.
