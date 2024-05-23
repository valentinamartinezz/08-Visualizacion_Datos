# Practica 8. Visualización de Datos con Pandas

## Introducción.
La visualización de datos es crucial porque transforma cifras complejas en gráficos comprensibles, facilitando la detección de tendencias, patrones y anomalías. Los gráficos permiten comunicar información de manera rápida y clara, mejorando la toma de decisiones. Al presentar datos visualmente, se fomenta un análisis más profundo y se captura la atención de manera efectiva, lo que es esencial en un mundo donde la capacidad de procesar rápidamente grandes volúmenes de información es cada vez más importante. En resumen, los gráficos son herramientas poderosas para sintetizar datos y revelar insights que podrían pasar desapercibidos en formatos numéricos crudos.

## **Uso de la función plot para crear gráficos directamente desde DataFrames:**
Pandas hace que sea muy fácil visualizar los datos directamente desde un DataFrame. La función `plot` es una herramienta versátil que puede generar varios tipos de gráficos con solo una línea de código. Por ejemplo, si tienes un DataFrame llamado `df`, simplemente puedes escribir `df.plot()` y Pandas creará un gráfico de líneas por defecto, mostrando todas las columnas numéricas en el eje Y y el índice del DataFrame en el eje X.

## **Creación de gráficos de líneas, barras, histogramas y más:**
Con la función `plot`, puedes especificar el tipo de gráfico que deseas crear con el argumento `kind`. Aquí hay algunos ejemplos:
- **Gráficos de líneas:** `df.plot(kind='line')` es útil para mostrar tendencias a lo largo del tiempo.
- **Gráficos de barras:** `df.plot(kind='bar')` es ideal para comparar valores entre diferentes grupos.
- **Histogramas:** `df.plot(kind='hist')` ayuda a entender la distribución de una variable numérica.

## **Personalización de la apariencia de los gráficos:**
Pandas permite personalizar tus gráficos para hacerlos más informativos y atractivos. Puedes cambiar colores, añadir etiquetas, títulos y mucho más. Por ejemplo:
- **Cambiar colores:** `df.plot(color='red')` cambiará el color de las líneas o barras a rojo.
- **Añadir títulos y etiquetas:** `plt.title('Mi Gráfico')` añadirá un título, y `plt.xlabel('Eje X')` y `plt.ylabel('Eje Y')` añadirán etiquetas a los ejes.

Aquí tienes un ejemplo simple de cómo podrías usar Pandas para crear y personalizar un gráfico de barras:

```python
import pandas as pd
import matplotlib.pyplot as plt

# Supongamos que tenemos el siguiente DataFrame
df = pd.DataFrame({
    'Productos': ['Manzanas', 'Naranjas', 'Plátanos'],
    'Ventas': [23, 38, 12]
})

# Creamos un gráfico de barras
df.plot(kind='bar', x='Productos', y='Ventas', color='skyblue')

# Personalizamos el gráfico
plt.title('Ventas de Frutas')
plt.xlabel('Frutas')
plt.ylabel('Cantidad Vendida')
plt.xticks(rotation=0)  # Rotamos las etiquetas del eje X para que se muestren horizontalmente
plt.show()
```
## Ejercicios:
1. Crea un DataFrame con el archivo de la carpeta `Data/loan.csv`, puedes encontrar más información de la data dando click [aqui](https://www.kaggle.com/datasets/sujithmandala/simple-loan-classification-dataset).
2. Crea un grafico de barras en donde se muestren la cantidad de personas registradas por `occupation`.
3. Crea un gráfico de barras en donde se muestre el total de personar registradas por `education_level`
4. Crea un grafico circular en donde se muestre la proporcion de Hombres y mujeres de acuerdo a la columna `gender`
5. Crea un histograma con la columna `age`. 