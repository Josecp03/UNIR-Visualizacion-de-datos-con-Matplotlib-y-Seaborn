# Trabajo 4: Visualización de datos con Matplotlib y Seaborn

Análisis completo del dataset de ventas de Superstore 2012 mediante diferentes técnicas de visualización de datos utilizando las bibliotecas Matplotlib y Seaborn.

## Descripción del proyecto

Este proyecto consiste en crear visualizaciones con Matplotlib y Seaborn para analizar un conjunto de datos de ventas minoristas. Se implementan diferentes tipos de gráficos (univariantes, bivariantes y multivariantes) para extraer insights relevantes del negocio.

## Dataset

El análisis se realiza sobre el archivo `superstore_dataset2012.csv`, que contiene información de ventas de una tienda minorista durante el año 2012. El dataset incluye:

- 4,246 registros de transacciones
- 24 columnas con información sobre productos, clientes, ventas y beneficios
- Categorías: Technology, Furniture, Office Supplies
- Segmentos de clientes: Consumer, Corporate, Home Office

## Requisitos implementados

El proyecto cumple con todos los requisitos solicitados:

- Gráfico univariante con Matplotlib (histograma de distribución de ventas)
- Gráfico univariante con Seaborn (boxplot de beneficios por categoría)
- Gráfico bivariante con Matplotlib (dispersión de ventas vs beneficio)
- Gráfico bivariante con Seaborn (barras agrupadas por categoría y segmento)
- Visualización multivariante con Seaborn (heatmap de correlación y pairplot)
- Personalización de gráficos (títulos, etiquetas, paletas de colores)
- Organización de visualizaciones en subplots (dashboard con 4 gráficos)
- Guardado de figuras como archivos de imagen
- Comentarios explicativos sobre las conclusiones de cada visualización

## Estructura del proyecto

```
.
├── visualizacion_datos.ipynb    # Notebook principal con todo el análisis
├── superstore_dataset2012.csv   # Dataset utilizado
├── histograma_ventas.png        # Visualización guardada
├── dashboard_completo.png       # Dashboard con múltiples gráficos
└── README.md                    # Este archivo
```

## Tecnologías utilizadas

- **Python 3.x**
- **Pandas**: Manipulación y análisis de datos
- **NumPy**: Operaciones numéricas
- **Matplotlib**: Creación de gráficos estáticos
- **Seaborn**: Visualizaciones estadísticas avanzadas

## Principales hallazgos

### Distribución de ventas
- La mayoría de las ventas se concentran en montos bajos (por debajo de $500)
- La diferencia entre media ($237) y mediana ($82.53) indica presencia de valores atípicos altos
- Distribución asimétrica hacia la derecha

### Beneficios por categoría
- Technology tiene mayor variabilidad en beneficios
- Se observan outliers negativos en todas las categorías (ventas no rentables)
- Office Supplies muestra beneficios más consistentes aunque más bajos

### Relación ventas-beneficio
- Correlación positiva entre ventas y beneficio, pero no perfecta
- Algunas ventas altas generan pérdidas
- Los tres segmentos de clientes muestran patrones similares

### Correlaciones importantes
- El descuento tiene correlación negativa con el beneficio (-0.22)
- Las ventas y los costos de envío están fuertemente correlacionados (0.76)
- Curiosamente, el descuento no aumenta significativamente la cantidad vendida

### Temporalidad
- Pico de ventas en septiembre (posiblemente temporada de vuelta al cole/oficina)
- Phones y Chairs son las subcategorías más vendidas

## Cómo ejecutar el proyecto

### Opción 1: Google Colab (recomendado)
1. Sube el archivo `superstore_dataset2012.csv` a Colab
2. Abre el notebook `visualizacion_datos.ipynb`
3. Ejecuta todas las celdas secuencialmente

### Opción 2: Entorno local
1. Clona este repositorio
2. Instala las dependencias:
```bash
pip install pandas numpy matplotlib seaborn
```
3. Abre el notebook con Jupyter:
```bash
jupyter notebook visualizacion_datos.ipynb
```
4. Ejecuta todas las celdas

## Visualizaciones generadas

El proyecto genera las siguientes visualizaciones:

1. **Histograma de ventas** - Distribución de los montos de ventas
2. **Boxplot de beneficios** - Comparación de beneficios por categoría
3. **Gráfico de dispersión** - Relación entre ventas y beneficio por segmento
4. **Barras agrupadas** - Ventas promedio por categoría y segmento
5. **Heatmap de correlación** - Matriz de correlaciones entre variables numéricas
6. **Pairplot** - Relaciones múltiples entre variables
7. **Dashboard completo** - 4 visualizaciones organizadas en subplots

## Criterios de evaluación cumplidos

- **Implementación de visualizaciones con Matplotlib (40%)**: Completo
  - Histograma, dispersión y múltiples gráficos en subplots
  
- **Implementación de visualizaciones con Seaborn (40%)**: Completo
  - Boxplot, barras agrupadas, heatmap y pairplot
  
- **Preparación y manejo de datos con Pandas (20%)**: Completo
  - Carga, exploración, conversión de fechas y transformaciones necesarias
