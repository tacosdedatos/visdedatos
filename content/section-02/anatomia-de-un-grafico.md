Anatomía de un Gráfico
======================


Cada gráfico en `altair` es compuesto al describir un mínimo de tres elementos:
* Datos
* Marcadores
* Codificaciones

***

## Datos
`Altair` acepta __datasets__ de 3 maneras:
* un `DataFrame` de `pandas`
* un objeto de clase `Data` de `altair`
* datos en formato `JSON` o `csv` de manera directa

Nosotros trabajaremos con `DataFrames` de `pandas`. 

`Pandas` es una de las mejores opciones para trabajar con estructuras de datos en `python`. El nombre `pandas` proviene de __Python Data Analysis Library__. `pandas` esta basada en `numpy` (de __Numeric Python__) la cual provee estructuras de datos (__arrays__ o _matrices_) las cuales `pandas` utiliza para crear __DataFrames__. Un __DataFrame__ es una estructura de datos en la cual se pueden guardar datos de distintos tipos (cadenas de caractéres (__strings__), __integers__, __floats__, y más) en cada columna. Es similar a una tabla o una planilla de Excel o Google Spreadsheets. 

Como es una estructura de `python` claro que su índice comienza en 0.

## Marcadores

El marcador en un gráfico es la representación visual de tus datos. `Altair` ofrece los siguientes marcadores hasta el momento:

| Marcador  | Método          | Descripción                                      | Ejemplo                                   |
|-----------|-----------------|--------------------------------------------------|-------------------------------------------|
| area      | mark_area()     | Un gráfico de area.                              | [Simple Stacked Area Chart](https://altair-viz.github.io/gallery/simple_stacked_area_chart.html#gallery-simple-stacked-area-chart)|
| barra     | mark_bar()      | Un gráfico de barras.                            | [Simple Bar Chart](https://altair-viz.github.io/gallery/simple_bar_chart.html#gallery-simple-bar-chart)|
| círculo   | mark_circle()   | Un diagrama de dispersión con círculos rellenos. | [One Dot Per Zipcode](https://altair-viz.github.io/gallery/one_dot_per_zipcode.html#gallery-one-dot-per-zipcode)|
|_geofigura_| mark_geoshape() | Una fígura geográfica.                           | [Choropleth Map](https://altair-viz.github.io/gallery/choropleth.html#gallery-choropleth)|
| línea     | mark_line()     | Un gráfico de líneas.                            | [Simple Line Chart](https://altair-viz.github.io/gallery/simple_line_chart.html#gallery-simple-line-chart)|
| punto     | mark_point()    | Un diagrama de dispersión con formas de puntos configurables.   | [Faceted Scatter Plot with Linked Brushing](https://altair-viz.github.io/gallery/scatter_linked_brush.html#gallery-scatter-linked-brush)|
| rectángulo| mark_rect()     | Un rectángulo relleno, usado para mapas de calor (_heatmaps_).  | [Simple Heatmap](https://altair-viz.github.io/gallery/simple_heatmap.html#gallery-simple-heatmap)|
| regla     | mark_rule()     |Una línea vertical u horizontal que abarca el eje.| [Candlestick Chart](https://altair-viz.github.io/gallery/candlestick_chart.html#gallery-candlestick-chart)|
| cuadrado  | mark_square()   | Un diagrama de dispersián con cuadrados.         | N/A                                       |
| texto     | mark_text()     | Un diagrama de dispersián con los puntos representados con texto.  | [Simple Bar Chart with Labels](https://altair-viz.github.io/gallery/bar_chart_with_labels.html#gallery-bar-chart-with-labels)|
| marca     | mark_tick()     | Una marca o línea horizontal o vertical.         | [Strip Plot](https://altair-viz.github.io/gallery/strip_plot.html#gallery-strip-plot)|


## Codificaciones

Un gráfico es una representación visual de tus datos. Es esencial conectar tu información a un elemento visual en el gráfico. En `altair` eso se le conoce como __encode__ o _codificar_ tus datos. Es el proceso de asignar valores (en este caso columnas de tu __DataFrame__) a elementos posicionales (como el eje X o Y) o propiedades de tu marcador (como el color o el tamaño). 
`Altair` es una biblioteca para crear gráficos altamente configurables asi que simplemente enlistar todas las codificaciones posibles sería una manera muy ineficáz de aprender. La mejor manera de aprender es haciendo.

### Tipos de Datos

`altair` hace un buen trabajo deduciendo el tipo de datos con el que estas trabajando al igual que `pandas`. Pero también puedes especificar el tipo de datos en tus gráficos. `Altair` reconoce 4 tipos de datos:

| Tipo de datos | Código |                Descripción                | 
|:-------------:|:------:|:------------------------------------------|
| cuantitativo  |    Q   | una cantidad continua y de números reales | 
| ordinal       |    O   | una cantidad discreta y ordenada          |
| nominal       |    N   | una cantidad discreta y desordenada       |
| temporal      |    T   | un valor de tiempo o fecha                |

En los ejercicios de este cápitulos aprenderás sobre las bastas opciones que tienes para representar tus datos de manera gráfica con `altair`. 

***


![anatomia de un grafico](../images/chapter-02/anatomia-de-un-grafico.png)