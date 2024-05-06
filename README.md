# Práctica 6. *Indexación y selección de datos*

Supongamos que tenemos el siguiente DataFrame llamado `ventas_df`:

```python
import pandas as pd

# Crear un DataFrame de ejemplo
data = {
    'Producto': ['A', 'B', 'C', 'D', 'E'],
    'Ventas_2022': [100, 200, 150, 300, 180],
    'Ventas_2023': [120, 210, 160, 310, 190]
}

ventas_df = pd.DataFrame(data)
```

### 1. Indexación y selección de filas y columnas en DataFrames

#### Acceso a columnas:
- Para acceder a una columna específica, utilizamos la notación de corchetes `[]` con el nombre de la columna. Por ejemplo:

```python
# Acceder a la columna 'Ventas_2022'
ventas_2022 = ventas_df['Ventas_2022']
print(ventas_2022)
```
[Revisar documentación](docs/docloc.md#acceso-a-columnas)

#### Acceso a filas:
- Para acceder a filas específicas, podemos utilizar los métodos `loc[]` o `iloc[]`. Por ejemplo:

```python
# Acceder a la fila con índice 2 (tercera fila)
fila_2 = ventas_df.loc[2]
print(fila_2)
```

### 2. Uso de etiquetas y posiciones para acceder a datos

#### Acceso por etiqueta:
- Utilizamos `loc[]` para acceder a datos por etiqueta (nombre de fila o columna). Por ejemplo:

```python
# Acceder a la venta de 'Producto B' en 2023
venta_B_2023 = ventas_df.loc[1, 'Ventas_2023']
print(f"Venta de Producto B en 2023: {venta_B_2023}")
```

#### Acceso por posición:
- Utilizamos `iloc[]` para acceder a datos por posición (índice numérico de fila o columna). Por ejemplo:

```python
# Acceder a la venta de 'Producto C' en 2022
venta_C_2022 = ventas_df.iloc[2, 1]
print(f"Venta de Producto C en 2022: {venta_C_2022}")
```
[Revisar documentación](docs/docloc.md#acceso-a-columnas)
### 3. Filtrado de datos basado en condiciones

#### Filtrar filas:
- Podemos filtrar filas basadas en condiciones. Por ejemplo, para obtener las filas donde las ventas en 2023 superan las 200 unidades:

```python
# Filtrar filas con ventas en 2023 > 200
ventas_superiores_200 = ventas_df[ventas_df['Ventas_2023'] > 200]
print(ventas_superiores_200)
```
[Consulta las condiciones mas comunes](docs/condiciones.md)

## Ejercicios

[Descargue el conjunto de datos](https://www.kaggle.com/datasets/anandshaw2001/airlines-booking-csv) y almacene el archivo  como "ventas.csv" en la carpeta data, posteriormente realice las siguientes consignas:


1. **Acceso a columnas y estadísticas básicas**:
   - Imprime las primeras 5 filas del DataFrame.
   - Calcula la media y la desviación estándar de la columna `num_passengers`. (Aplicar método [`mean()` y `std()`](docs/dispersión.md))
   - ¿Cuál es el número máximo de pasajeros registrados? (Aplicar método  [`max()`](docs/docsymin.md)).

2. **Filtrado de datos**:
   - Filtra las filas donde el `trip_type` es "ida y vuelta".
   - Encuentra las reservas realizadas desde el país "España".

3. **Selección de filas y columnas**:
   - Selecciona las columnas `flight_day`, `flight_hour` y `length_of_stay`.
   - Muestra los datos de la fila correspondiente al vuelo con la duración más larga. (filtra con duración mayor al tercer cuartil, puedes utilizar el metodo `describe()`)

4. **Agregación y agrupación**:
   - Agrupa los datos por `ruta` y calcula la suma total de pasajeros para cada ruta. (aplicar  [`groupby()`, `sum()`](docs/groupbysum.md)).
   - ¿Cuál es la ruta más popular en términos de pasajeros?

5. **Creación de nuevas columnas**:
   - Crea una nueva columna llamada `booking_lead_days` que represente la diferencia entre `purchase_lead` y `length_of_stay`.
   - ¿Cuál es el valor medio de `booking_lead_days`?

6. **Visualización de datos**:
   - Crea un gráfico de barras que muestre la cantidad de pasajeros por día de la semana (`flight_day`).

7. **Análisis de completitud de reservas**:
   - Calcula la proporción de reservas completadas (donde `booking_complete` es verdadero) en comparación con todas las reservas.

Recuerda adaptar estos ejercicios según tus necesidades específicas y explorar más funciones de pandas para profundizar en el análisis de datos. ¡Buena suerte! 🚀
