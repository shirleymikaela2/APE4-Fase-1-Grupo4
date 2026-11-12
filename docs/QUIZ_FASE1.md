# Quiz de Fase 1 (Cris) · 10 preguntas con respuesta

1. **¿Qué representa una persona?** Un vértice. Cada persona registrada ocupa un vértice del grafo, incluso si no tiene amistades.

2. **¿Qué representa una amistad?** Una arista no dirigida y no ponderada. La relación es mutua y no tiene un peso asignado.

3. **¿Cuántos vértices tiene el caso?** Cinco. Son Ana, Bruno, Carla, Diego y Elena.

4. **¿Cuántas aristas tiene inicialmente?** Cuatro. Las amistades son Ana–Bruno, Ana–Carla, Bruno–Diego y Carla–Diego.

5. **¿Cuál es el grado de Elena?** Cero. Elena está registrada, pero ninguna de las cuatro amistades la incluye.

6. **¿Ana y Diego tienen amistad directa?** No. Existe el camino Ana–Bruno–Diego, pero no hay una arista que una directamente a Ana con Diego.

7. **¿Ana y Bruno tienen amistad directa?** Sí. La arista `e1` los conecta y representa una sola amistad mutua.

8. **¿Se permite Ana–Ana?** No. Esa relación sería un lazo, y la regla R2 prohíbe las amistades de una persona consigo misma.

9. **¿Cuál es el orden de la matriz de adyacencia?** 5 × 5, con una fila y una columna por persona. Es simétrica porque las amistades son mutuas y su diagonal tiene ceros porque no se permiten lazos.

10. **¿Qué pasa con la densidad al añadir Ana–Elena?** Pasa de 40 % a 50 %. Entre cinco personas hay diez parejas posibles. El caso inicial tiene cuatro amistades (`4/10`) y el escenario propuesto tendría cinco (`5/10`).
