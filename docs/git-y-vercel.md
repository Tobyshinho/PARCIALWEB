# Git, rama de trabajo y Preview

## Rama base

La entrega sigue la instrucción explícita del proyecto: `feature/parcial-portal` parte de `main`. Esta decisión reemplaza las referencias antiguas a `develop`/`feature/landing-responsive` de la base. Los cambios se registran con commits descriptivos, por ejemplo `feat: completa portal de soporte TI`, `fix: corrige navegación móvil` y `docs: agrega evidencias y auditoría`.

## Estado del repositorio externo

El ZIP de inicio no incluye `.git` ni un remoto GitHub. El proyecto gestionado contiene su propio `main`. La URL del repositorio externo no se recibió, por lo que no se inventa un `origin`, URL, owner ni PR.

La conexión de un proyecto Manus-managed a GitHub debe seguir el flujo canónico de Webdev y su tarjeta de confirmación. Ese flujo puede preparar un repositorio privado nuevo, pero no permite importar/adoptar automáticamente un repo existente. Resolver el destino y comprobar acceso precede a transferir refs o abrir el Pull Request. No usar tokens en archivos/chat, `gh` o un conector genérico para saltarse ese flujo; no fusionar el PR ni publicar sin instrucción.

## Preview de desarrollo

El Preview Manus sirve el proceso de desarrollo en el puerto runtime confirmado (3000), no es una versión pública permanente. El servidor local incluido en la base es para VS Code y escucha en `127.0.0.1:5500`; no confundir esa dirección con el Preview gestionado. No ejecutar Publish ni activar publicación automática para esta entrega.

## Checklist para el PR cuando el destino esté autorizado

- Compare: `feature/parcial-portal`; base: `main`.
- Resumen de HTML/CSS, ausencia de backend, y preservación byte por byte de `ui.js`.
- SHA completo igual al commit cuyo árbol se empaqueta en el ZIP.
- Enlaces a Preview y evidencias verificadas; resultados del workflow de calidad si el repositorio los ejecuta.
