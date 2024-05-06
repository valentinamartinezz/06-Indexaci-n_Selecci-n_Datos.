## Métodos para el calculo de medidas de dispersión  **`mean()`** y **`std()`**:

1. **`mean()`** (media):
   - **Descripción**: `mean()` calcula la media (promedio) de los valores en una columna o fila.
   - **Sintaxis**: `df.mean(axis=0)` para calcular la media por columnas (eje 0) o `df.mean(axis=1)` para calcular la media por filas (eje 1).
   - **Ejemplo**:
     ```python
     # Calcular la media de las ventas en 2022
     media_ventas_2022 = ventas_df['Ventas_2022'].mean()
     print(f"Media de ventas en 2022: {media_ventas_2022}")
     ```

2. **`std()`** (desviación estándar):
   - **Descripción**: `std()` calcula la desviación estándar de los valores en una columna o fila.
   - **Sintaxis**: `df.std(axis=0)` para calcular la desviación estándar por columnas (eje 0) o `df.std(axis=1)` para calcular la desviación estándar por filas (eje 1).
   - **Ejemplo**:
     ```python
     # Calcular la desviación estándar de las ventas en 2023
     desviacion_ventas_2023 = ventas_df['Ventas_2023'].std()
     print(f"Desviación estándar de ventas en 2023: {desviacion_ventas_2023}")
     ```

Recuerda que la media representa el valor central de un conjunto de datos, mientras que la desviación estándar mide la dispersión o variabilidad de los datos con respecto a la media.

[Regresar a README.md](../README.md)