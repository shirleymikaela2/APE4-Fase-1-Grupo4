# Plan de validación (sin ejecutar)

Hay **18 casos de prueba propuestos**, almacenados en `CASOS_PRUEBA.csv`. Son expectativas derivadas del contrato de requisitos. No existe una columna de «aprobado» ni capturas de salida, porque aún no se ha implementado el sistema de la fase siguiente.

## Procedimiento propuesto
1. Implementar el comportamiento en la fase correspondiente.
2. Preparar una nueva instancia con los cinco usuarios y cuatro aristas del caso base.
3. Ejecutar cada escenario de manera independiente, restaurando el estado inicial cuando corresponda.
4. Registrar resultado real, versión del código, fecha y evidencia.
5. Comparar contra el resultado esperado e identificar discrepancias.

## Precauciones
- El orden de vecinos no se exige: se comparan conjuntos.
- Para una amistad recíproca AB, el modelo tiene una arista, no dos.
- Un ID inexistente nunca debe confundirse con una persona válida que no tiene amigos.
- Los CP08–CP12 son propuestas de altas o relaciones para verificar **reglas futuras**. No implican que estas operaciones estén programadas.
