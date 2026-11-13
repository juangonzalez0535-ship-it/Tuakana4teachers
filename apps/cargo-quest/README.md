# Cargo Quest — Edición Aula V2

Juego 2D de estrategia y precisión para explorar las leyes de Newton y el rozamiento. Se conserva la mecánica de preparar el empuje, lanzar la carga, analizar el resultado y ajustar el siguiente intento.

## Lo nuevo

- **Academia de Física:** módulo desplegable con las leyes de Newton, diagrama de cuerpo libre, fricción estática vs. cinética, vectores y cálculo de distancia, más un miniexperimento interactivo del umbral de arranque.
- **Distancia medible:** regla con marcas en metros, posición inicial de la meta, rango válido y distancia restante a la meta.
- **Predicción voluntaria:** el estudiante puede escribir cuántos metros cree que recorrerá la caja y comparar su estimación con el resultado.
- **Seis misiones:** se conservan cuatro y se agregan *Carga pesada* y *Entrega maestra*.
- **Progreso:** barra e insignias por misión, sin penalización por ensayar.
- **Identidad:** paleta provisional azul petróleo, turquesa y amarillo, pendiente de confirmar códigos oficiales de marca Tukana.

## Cómo jugar

1. Consulta la lección o inicia directamente una misión.
2. Lee la distancia exacta de la meta y analiza masa, coeficientes de fricción y controles disponibles.
3. Estima una distancia (opcional), ajusta fuerza, duración y/o ángulo, y pulsa lanzar.
4. Compara el lugar donde se detuvo la carga con la meta y tu predicción.
5. Explica qué fuerza determinó el resultado; cambia una sola variable y repite.

## Modelo físico y sus límites

Modelo educativo unidimensional de una carga sobre patines que se desliza por un suelo horizontal; g = 9,8 m/s². La fricción estática se ajusta hasta μₛ N y la cinética tiene magnitud μₖ N, contraria al deslizamiento. Al tirar hacia arriba de una cuerda, la normal se calcula como N = mg − F sen θ mientras la carga siga en contacto. No se simulan rodadura, deformaciones, impactos realistas ni vuelo.

Los coeficientes ilustran diferencias entre materiales; **no son mediciones universales**. El simulador usa integración numérica de intervalos pequeños para representar el movimiento. Las soluciones de las seis misiones se comprobaron con un modelo numérico independiente, pero sigue siendo necesario probar usabilidad y comprensión con estudiantes.

## Privacidad y tecnología

HTML + CSS + Canvas 2D + JavaScript. No requiere servidor de datos ni almacena información personal de menores. La fuente remota, cuando está disponible, es opcional.
