## Métodos **`max()`** y **`min()`**:

1. **`max()`**:
   - **Descripción**: `max()` devuelve el valor máximo de los datos en una columna o fila.
   - **Sintaxis**: `df.max(axis=0)` para calcular el máximo por columnas (eje 0) o `df.max(axis=1)` para calcular el máximo por filas (eje 1).
   - **Ejemplo**:
     ```python
     # Calcular el máximo de las ventas en 2022
     max_ventas_2022 = ventas_df['Ventas_2022'].max()
     print(f"Máximo de ventas en 2022: {max_ventas_2022}")
     ```

2. **`min()`**:
   - **Descripción**: `min()` devuelve el valor mínimo de los datos en una columna o fila.
   - **Sintaxis**: `df.min(axis=0)` para calcular el mínimo por columnas (eje 0) o `df.min(axis=1)` para calcular el mínimo por filas (eje 1).
   - **Ejemplo**:
     ```python
     # Calcular el mínimo de las ventas en 2023
     min_ventas_2023 = ventas_df['Ventas_2023'].min()
     print(f"Mínimo de ventas en 2023: {min_ventas_2023}")
     ```

Estos métodos son útiles para obtener los valores extremos en tus datos.

[Regresar a README.md](../README.md)