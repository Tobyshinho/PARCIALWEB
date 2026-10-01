# Git, rama de trabajo y Preview

## Rama base

La rama de entrega solicitada es `feature/parcial-portal`, creada desde `main`. Los commits se describen por separado para implementación y documentación. El SHA que identifique la ZIP debe ser exactamente el HEAD incluido en ella.

## Repositorio GitHub y PR

El destino privado confirmado por el propietario es [PARCIALWEB](https://github.com/Tobyshinho/PARCIALWEB). La transferencia sigue el flujo canónico de Webdev; el `main` del proyecto se conserva como base y `feature/parcial-portal` como rama de trabajo.

La variante de entrega omite `.github/workflows/calidad.yml` de toda su historia, según la decisión del usuario tras el rechazo de permisos de GitHub. Se mantienen las comprobaciones locales `npm run check`, `npm run check:syntax` y `npm test`; no se afirma que exista un workflow de GitHub Actions.

El SHA remoto y la URL del Pull Request solo se declaran después de verificar la transferencia y la creación del PR. El PR debe usar `feature/parcial-portal` como head y `main` como base; no fusionar ni publicar.

## Preview de desarrollo

El Preview Manus sirve el proceso de desarrollo en el puerto runtime confirmado (3000), no es una versión pública permanente. El servidor local incluido en la base es para VS Code y escucha en `127.0.0.1:5500`; no confundir esa dirección con el Preview gestionado. No ejecutar Publish ni activar publicación automática para esta entrega.

## Checklist de entrega

- Rama `feature/parcial-portal` con base `main`.
- `public/assets/js/ui.js` byte por byte igual al archivo recibido.
- HTML/CSS propios, formulario simulado, sin backend, envío ni persistencia.
- SHA completo igual al commit cuyo árbol se empaqueta en la ZIP.
- Enlaces de Preview y PR, solo después de verificar sus URL reales.
- Evidencias y limitaciones en `docs/pruebas.md`.
