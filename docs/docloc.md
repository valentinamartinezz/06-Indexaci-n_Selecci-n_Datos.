## Documentación para los métodos **`loc`** e **`iloc`** en **pandas**:

1. **`loc`** (etiquetas):
   - **Descripción**: `loc` es un método de selección de datos basado en etiquetas, lo que significa que utilizamos nombres de filas o columnas para acceder a los datos.
   - **Sintaxis**: `df.loc[etiqueta_fila, etiqueta_columna]`
   - **Ejemplo**:
     ```python
     # Acceder a la venta del 'Producto B' en 2023
     venta_B_2023 = ventas_df.loc[1, 'Ventas_2023']
     print(f"Venta del Producto B en 2023: {venta_B_2023}")
     ```

2. **`iloc`** (posiciones):
   - **Descripción**: `iloc` es un método utilizado para seleccionar filas y columnas de un DataFrame mediante indexación basada en números enteros.
   - **Sintaxis**: `df.iloc[posición_fila, posición_columna]`
   - **Ejemplo**:
     ```python
     # Acceder a la venta del 'Producto C' en 2022
     venta_C_2022 = ventas_df.iloc[2, 1]
     print(f"Venta del Producto C en 2022: {venta_C_2022}")
     ```

3. **Diferencias clave entre `loc` e `iloc`**:
   - `loc` utiliza etiquetas (nombres) para acceder a datos, mientras que `iloc` utiliza posiciones numéricas.
   - `loc` incluye el último elemento del rango pasado, mientras que `iloc` no lo incluye.
   - `iloc` puede aceptar datos booleanos, a diferencia de `loc`.

[Regresar a Readme](../README.md)