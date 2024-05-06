## Lista de condiciones comunes

1. **Igualdad (`==`)**:
   - Filtra filas donde el valor de una columna es igual a un valor específico.
   - Ejemplo: `ventas_df[ventas_df['Ventas_2023'] == 200]` selecciona las filas donde las ventas en 2023 son exactamente 200.

2. **Desigualdad (`!=`)**:
   - Filtra filas donde el valor de una columna no es igual a un valor específico.
   - Ejemplo: `ventas_df[ventas_df['Ventas_2022'] != 150]` selecciona las filas donde las ventas en 2022 no son 150.

3. **Mayor que (`>`), Mayor o igual que (`>=`)**:
   - Filtra filas donde el valor de una columna es mayor que (o igual a) un valor específico.
   - Ejemplo: `ventas_df[ventas_df['Ventas_2022'] > 200]` selecciona las filas donde las ventas en 2022 son mayores que 200.

4. **Menor que (`<`), Menor o igual que (`<=`)**:
   - Filtra filas donde el valor de una columna es menor que (o igual a) un valor específico.
   - Ejemplo: `ventas_df[ventas_df['Ventas_2023'] <= 210]` selecciona las filas donde las ventas en 2023 son menores o iguales a 210.

5. **Operadores lógicos (`&`, `|`)**:
   - Combina múltiples condiciones utilizando los operadores lógicos "y" (`&`) y "o" (`|`).
   - Ejemplo: `ventas_df[(ventas_df['Ventas_2022'] > 200) & (ventas_df['Ventas_2023'] < 210)]` selecciona las filas donde las ventas en 2022 son mayores que 200 y las ventas en 2023 son menores que 210.

6. **Filtrado basado en texto (`.str.contains()`)**:
   - Filtra filas donde una columna de texto contiene una cadena específica.
   - Ejemplo: `ventas_df[ventas_df['Producto'].str.contains('A')]` selecciona las filas donde el nombre del producto contiene la letra 'A'.

7. **Filtrado basado en listas (`.isin()`)**:
   - Filtra filas donde el valor de una columna está en una lista específica.
   - Ejemplo: `ventas_df[ventas_df['Producto'].isin(['A', 'B', 'C'])]` selecciona las filas donde el producto es 'A', 'B' o 'C'.

8. **Filtrado basado en valores nulos (`.isnull()`, `.notnull()`)**:
   - Filtra filas donde los valores en una columna son nulos o no nulos.
   - Ejemplo: `ventas_df[ventas_df['Ventas_2023'].isnull()]` selecciona las filas donde las ventas en 2023 son nulas.

Recuerda que puedes combinar estas condiciones para crear filtros más complejos según tus necesidades. ¡Espero que esta lista te ayude a comprender mejor las opciones de filtrado en pandas! 😊

[Regresar a Readme](../README.md)