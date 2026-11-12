# APE 4 · Fase 1 · Grupo 4

**Universidad Técnica de Ambato · Estructura de Datos · Tercero B**

El Grupo 4 analizó los requisitos de una red social y definió un modelo de referencia para representar personas, amistades y consultas. Esta entrega reúne la documentación, los datos del caso base, los diagramas, las matrices de comprobación y los resultados esperados de las pruebas. La implementación y la ejecución de las pruebas corresponden a la Fase 2.

## Archivos de la entrega

| Contenido | Archivos |
| --- | --- |
| Requisitos y actividad formativa | [Especificación del modelo](docs/ESPECIFICACION.md) · [Quiz de diez preguntas con respuestas justificadas](docs/QUIZ_FASE1.md) |
| Datos de referencia | [Personas](modelo/personas.csv) · [Amistades](modelo/amistades.csv) · [Vecinos y grados](modelo/vecinos_referencia.csv) |
| Diagramas | [Mermaid](modelo/grafo_fase1.mmd) · [PlantUML](modelo/PLANTUML_grafo.puml) |
| Matrices de comprobación | [Adyacencia](modelo/matriz_adyacencia.csv) · [Incidencia](modelo/matriz_incidencia.csv) |
| Validación prevista | [Banco de 18 casos](pruebas/CASOS_PRUEBA.csv) · [Plan de validación](pruebas/PLAN_DE_VALIDACION.md) |
| Continuidad de la práctica | [Acta de traspaso a la Fase 2](entrega/ACTA_DE_TRASPASO.md) |

## Caso base

La red se representa mediante un grafo **simple, no dirigido y no ponderado**. Cada persona es un vértice y cada amistad mutua es una arista. Los identificadores son únicos, los nombres deben contener texto y las amistades solo se permiten entre personas registradas y distintas. Cada pareja puede tener una sola arista.

| ID | Persona | Vecinos directos | Grado |
| --- | --- | --- | ---: |
| P01 | Ana | Bruno y Carla | 2 |
| P02 | Bruno | Ana y Diego | 2 |
| P03 | Carla | Ana y Diego | 2 |
| P04 | Diego | Bruno y Carla | 2 |
| P05 | Elena | Ninguno | 0 |

El caso tiene **5 personas y 4 amistades**. Elena permanece registrada como vértice aislado. De las 10 parejas posibles, 4 son amistades, por lo que la densidad es del **40 %**. La matriz de adyacencia es simétrica, mide 5 × 5 y tiene ceros en la diagonal. La de incidencia mide 5 × 4 y cada columna contiene dos unos, uno por extremo de la amistad.

## Consultas y validación

| Consulta | Resultado esperado |
| --- | --- |
| `existeRelacion(P01, P02)` | Verdadero, porque Ana y Bruno tienen una amistad directa. |
| `existeRelacion(P01, P04)` | Falso, porque Ana y Diego carecen de una amistad directa. |
| `vecinos(P01)` | Conjunto `{P02, P03}`. |
| `vecinos(P05)` y `grado(P05)` | Conjunto vacío y grado `0`, respectivamente. |
| `vecinos(P99)` | Error de validación por identificador inexistente. |

Los **18 casos de prueba** se agrupan en consultas (CP01–CP07), validación de restricciones (CP08–CP14) e integridad del modelo (CP15–CP18). El banco registra las entradas y las salidas esperadas para la futura ejecución.

## Actividad formativa

La dinámica plantea añadir hipotéticamente la amistad **Ana–Elena**. Con esa arista, el grado de Ana subiría de 2 a 3 y el de Elena de 0 a 1. La densidad pasaría al 50 %. El caso base utilizado para el traspaso conserva sus cuatro amistades originales.

El informe también propone un criterio de recomendación por vecinos en común. En el caso base, Ana y Diego obtendrían dos puntos por compartir a Bruno y Carla. El criterio se analiza de forma conceptual para una fase posterior.

## Traspaso a la Fase 2

El equipo receptor partirá de los mismos identificadores, datos, reglas y contratos de consulta. A partir del acta de traspaso, podrá implementar las operaciones en Java y ejecutar los 18 casos para comparar los resultados obtenidos con los esperados.

## Integrantes

- Josué Caguana
- Cristopher Oto
- Andrés Moyota
- Shirley Yanchatipan
- Lenin Maigua
- Héctor Villacís

El registro de las contribuciones del equipo está disponible en el [historial de commits](https://github.com/shirleymikaela2/APE4-Fase-1-Grupo4/commits/main/) y en las [solicitudes de cambios](https://github.com/shirleymikaela2/APE4-Fase-1-Grupo4/pulls?q=is%3Apr+is%3Aclosed).

