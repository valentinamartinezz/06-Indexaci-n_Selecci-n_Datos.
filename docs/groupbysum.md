# Métodos **`groupby()`** y **`sum()`** en **pandas**:

1. **`groupby()`**:
   - **Descripción**: `groupby()` implica una combinación de dividir el objeto, aplicar una función y combinar los resultados. Se utiliza para agrupar grandes cantidades de datos y calcular operaciones en estos grupos.
   - **Sintaxis**: `df.groupby(by=columna).sum()`
   - **Ejemplo**:
     ```python
     # Agrupar por la columna 'ruta' y calcular la suma de pasajeros para cada ruta
     pasajeros_por_ruta = df.groupby('ruta')['num_passengers'].sum()
     print(pasajeros_por_ruta)
     ```

2. **`sum()`**:
   - **Descripción**: `sum()` calcula la suma de los valores en una columna o fila.
   - **Sintaxis**: `df['columna'].sum()`
   - **Ejemplo**:
     ```python
     # Calcular la suma total de pasajeros
     total_pasajeros = df['num_passengers'].sum()
     print(f"Total de pasajeros: {total_pasajeros}")
     ```

Estos métodos son útiles para realizar cálculos agregados en tus datos.

[Regresar a README.md](../README.md)