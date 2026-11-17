# Cargo Quest — Physics Arena V3
## Matriz matemática y criterios de prueba

**Fecha:** 17 de noviembre de 2026  
**Estado:** cuatro niveles calibrados con soluciones encontradas mediante el motor numérico del juego.  
**Nota:** los coeficientes son supuestos didácticos de pares de superficies; no son tablas experimentales universales.

## Modelo físico

En una superficie horizontal, con masa `m` y fuerza de tracción `F` aplicada con ángulo `θ`:

- Peso: `mg`; `g = 9,8 m/s²`.
- Componente horizontal: `Fx = F cos(θ)`; componente vertical al jalar: `Fy = F sen(θ)`.
- Normal mientras hay contacto: `N = mg − Fy`; se rechaza el intento si `Fy >= mg`.
- Fricción estática: hasta `fs,max = μs N`. Si está en reposo y `Fx <= fs,max`, no arranca.
- Una vez desliza: `fk = μk N`, opuesta a la velocidad; aceleración inicial: `a = (Fx − fk)/m`.
- Fuerza aplicada solo durante `duración` y luego retirada; el cuerpo sigue deslizándose hasta que se frena.
- Integración determinista por pasos de `1/240 s`. Se detiene al llegar a `v=0`, cruzar la marca en nivel 1 o alcanzar el límite de pista.

## Contactos disponibles

| Par de superficies | μs | μk |
|---|---:|---:|
| Madera / madera | 0,50 | 0,30 |
| Madera / hielo | 0,10 | 0,05 |
| Caucho / concreto | 0,80 | 0,60 |
| Metal / metal | 0,40 | 0,25 |
| Plástico / baldosa | 0,30 | 0,20 |

## Niveles calibrados

Las siguientes configuraciones son **ejemplos verificables**, no soluciones únicas ni valores que deba mostrar el juego antes del intento.

| Nivel | Objetivo | m | Superficie | Método, F y θ | Duración | N inicial | fs máxima | fk inicial | Fx inicial | Posición simulada |
|---|---|---:|---|---|---:|---:|---:|---:|---:|---:|
| 1. El almacén | Cruzar 2,00 m | 10 kg | Madera/madera | Empuje, 90 N, 0° | 1,2 s fija | 98,00 N | 49,00 N | 29,40 N | 90,00 N | 2,0003 m al cruzar |
| 2. El puerto | Detener entre 4,80 y 6,00 m | 20 kg | Madera/madera | Cuerda, 210 N, 20° | 0,6 s | 124,18 N | 62,09 N | 37,25 N | 197,34 N | 5,4379 m |
| 3. La estación de montaña | Detener entre 4,00 y 5,20 m | 25 kg | Plástico/baldosa | Cuerda, 90 N, 40° | 2,1 s | 187,15 N | 56,14 N | 37,43 N | 68,94 N | 4,5854 m |
| 4. Physics Arena | Detener entre 5,80 y 6,60 m | 20 kg | Madera/madera | Cuerda, 90 N, 20° | 2,1 s | 165,22 N | 82,61 N | 49,57 N | 84,57 N | 6,1818 m |

**Advertencia sobre nivel 1:** la simulación finaliza al **cruzar la marca**, por lo que 2,0003 m no es la distancia final de frenado. Los niveles 2–4 sí evalúan el lugar en que se detiene la carga.

## Reglas competitivas

- Los equipos A y B reciben la misma misión. Cada uno guarda su estrategia y su ficha de predicción sin ver la del rival.
- Se ejecutan ambos lanzamientos una vez bloqueadas las dos estrategias.
- Máximo dos rondas; se conserva el mejor intento de cada equipo.
- En niveles 2–4, primero se compara la distancia a la zona válida y, si ambos están dentro, la distancia al centro de la zona.
- En nivel 1, quien cruza la marca supera a quien no la cruza; entre los que cruzan, gana el menor impulso `F × duración`. Entre quienes no cruzan, gana el que se acercó más.
- El cálculo no tiene una puntuación adicional que modifique el resultado físico, pero es obligatorio predecir normal, fricción estática máxima, fricción cinética y distancia antes de jugar.

## Validaciones realizadas

- Sintaxis JavaScript verificada con Node.
- Motor probado en ejecución aislada JavaScript (VM) con cuatro configuraciones ganadoras.
- Inicio y carga de lógica de cuatro niveles sin errores en el entorno de pruebas aislado.
- La comprobación visual completa en navegador automatizado no se pudo concluir porque el entorno restringió la navegación de Chromium. **Pendiente:** revisión manual en Chrome/Safari y prueba real con mentores y estudiantes.

## Riesgos a vigilar

1. Los valores de contacto son pedagógicos y no deben citarse como datos de laboratorio.
2. El resultado numérico procede de una integración temporal discreta, con pequeña tolerancia de redondeo.
3. Para evitar sobrecarga cognitiva, el mentor puede permitir calculadora y usar el modo individual como ensayo previo a la competencia.
4. El motor es 1D y supone fuerza aplicada hacia la derecha; no resuelve rodadura, choques ni levantamiento.
5. La identidad visual usa paleta azul/verde/amarillo provisional hasta confirmar manual de marca de Tukana.