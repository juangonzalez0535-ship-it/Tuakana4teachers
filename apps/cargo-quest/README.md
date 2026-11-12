# Cargo Quest — El Almacén (MVP)

Videojuego 2D de precisión y estrategia para aprender las leyes de Newton, especialmente fricción estática y cinética.

## Cómo jugar

1. Selecciona una de las cuatro misiones.
2. Predice qué ocurrirá con la fuerza y duración propuestas.
3. Ajusta los controles y pulsa **Lanzar intento**.
4. Observa el resultado; modifica una sola variable por intento.
5. Al acertar, explica por qué funcionó y avanza.

## Misiones

- **¡Haz que se mueva!** Superar el umbral de fricción estática.
- **La entrega perfecta.** Conseguir que la carga se detenga dentro de la zona de entrega.
- **El piso traicionero.** Elegir la superficie central del recorrido y controlar la distancia de frenado.
- **La cuerda inteligente.** Ajustar fuerza, duración y ángulo de tracción para equilibrar las componentes horizontal/vertical y la fricción.

## Para el mentor

Activar **Modo mentor** para ver fuerza horizontal, normal, fricción, aceleración, velocidad y una pregunta de reflexión. La puntuación y los intentos no se guardan después de cerrar la página.

## Modelo físico

- Caja sobre patines deslizantes en una superficie horizontal; se desprecia la rodadura.
- Gravedad constante: `g=9.8 m/s²`.
- Fricción estática con umbral `μs · N`; fricción cinética `μk · N` opuesta al movimiento.
- Fuerza durante un tiempo elegido; su componente vertical modifica `N` al jalar hacia arriba.
- Modelo educativo unidimensional, sin deformaciones, golpes, pendiente del suelo ni levantamiento de la caja.
- Coeficientes de fricción de cada material elegidos para el juego: son ilustrativos, no mediciones universales.

## Tecnología

HTML, CSS, Canvas 2D y JavaScript sin dependencias funcionales ni backend. Google Fonts es opcional y el sistema usa fuentes locales cuando no hay internet.

## Estado

MVP jugable para pruebas con mentores; pendiente de validar usabilidad y resultados pedagógicos con estudiantes.
