# Tukana Lab · Tukana4Teachers

Biblioteca de herramientas web de Tukana para mentorías y experiencias de aprendizaje.

## Estructura

- `apps/`: cada herramienta es una aplicación autónoma con su propio `index.html` y `README.md`.
- `shared/assets/`: recursos comunes de marca.
- `docs/`: guías generales de uso y criterios pedagógicos.
- `index.html`: catálogo de herramientas.

## Convenciones

1. Una carpeta por aplicación, usando minúsculas y guiones (por ejemplo: `apps/historias-al-cubo/`).
2. Priorizar HTML, CSS y JavaScript sin dependencias para herramientas pequeñas.
3. No integrar datos identificables de estudiantes ni claves privadas en el código público.
4. Documentar el objetivo pedagógico, el modo de uso y el estado de cada aplicación.
5. Probar los cambios antes de publicarlos.

## Publicación

El repositorio puede desplegarse como sitio estático. Para rutas `/apps/nombre/`, basta con que cada carpeta tenga `index.html`. La elección del hosting y del dominio está pendiente.

## Primeras herramientas

- **Historias al Cubo:** juego de dados para narración oral (V4 publicada en `apps/historias-al-cubo/`).
- **Simulador de Planeador:** Glider Lab, sesión 2, incorporado en `apps/simulador-planeador/`.
