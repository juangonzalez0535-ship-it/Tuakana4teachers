# Cargo Quest — Physics Arena V3

**Tukana Lab · Juego de precisión y estrategia sobre Newton y fricción**

## Cómo jugar

1. Selecciona un nivel y configura masa, material y fuerza. El método de tracción, duración y ángulo se desbloquean según el nivel.
2. Consulta los coeficientes de fricción estática (μs) y cinética (μk) del par de superficies seleccionado.
3. Completa cuatro predicciones: normal, fricción estática máxima, fricción cinética y distancia final.
4. Lanza; observa el desplazamiento y compara tus cálculos con los resultados.
5. En **modo competitivo**, dos equipos bloquean sus estrategias antes de ver los lanzamientos, con dos rondas y una puntuación de cercanía a la zona.

## Los cuatro niveles

| Nivel | Escenario | Meta |
|---|---|---|
| 1 | Almacén | Cruzar 2 m superando la fricción estática |
| 2 | Puerto | Detenerse entre 4,80 y 6,00 m |
| 3 | Estación de montaña | Detenerse entre 4,00 y 5,20 m mediante cuerda |
| 4 | Physics Arena | Detenerse entre 5,80 y 6,60 m usando todos los controles |

El archivo `matriz-matematica-v3.md` incluye las **ecuaciones, supuestos, coeficientes y una solución verificada por nivel**. La copia `v2-edicion-aula.html` preserva la edición anterior.

## Alcance y límites

HTML, CSS y Canvas JavaScript sin dependencias de ejecución. Modelo 1D didáctico, horizontal, carga sobre patines deslizantes, g=9,8 m/s². Los coeficientes son **valores ilustrativos**, no datos de laboratorio. No se modela rodadura, colisión ni levantamiento. Los resultados de física son deterministas. No hay almacenamiento de información personal.

## Estado de pruebas

✅ Sintaxis de JavaScript validada con Node. ✅ Cuatro niveles tienen configuraciones ganadoras comprobadas mediante ejecución aislada del motor. ⚠️ Revisión completa de navegador (Chrome/Safari) y pruebas con estudiantes pendientes: el entorno de pruebas actual restringe Chromium.

## Identidad

Paleta provisional azul petróleo, turquesa y acentos amarillos. Pendiente de contrastar con la guía oficial de marca de Tukana.
