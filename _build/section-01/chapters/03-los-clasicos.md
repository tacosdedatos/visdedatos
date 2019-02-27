---
interact_link: content/section-01/chapters/03-los-clasicos.ipynb
kernel_name: python3
title: 'Los Clásicos'
prev_page:
  url: /section-01/chapters/02-desventajas
  title: 'Desventajas'
next_page:
  url: /section-02/anatomia-de-un-grafico
  title: 'Anatomía de un Gráfico'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---

# Los Clásicos

Aquí tenemos unos ejemplos de gráficos comunes y el código correspondiente en `altair`

#### _Gráfico de dispersión_ (aka _scatterplot_)



{:.input_area}
```python
import altair as alt
from vega_datasets import data

iris = data.iris()

alt.Chart(iris).mark_point().encode(
    x='petalWidth',
    y='petalLength',
    color='species',
    tooltip='species'
)
```





{:.output .output_png}
![png](../../images/section-01/chapters/03-los-clasicos_2_0.png)




#### _Gráfico de barras_ (aka _bar chart_)



{:.input_area}
```python
import altair as alt
import pandas as pd

data = pd.DataFrame({
    'a': ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I'],
    'b': [28, 55, 43, 91, 81, 53, 19, 87, 52]
})

alt.Chart(data).mark_bar().encode(
    x='a',
    y='b'
).properties(
    height = 400,
    width = 500,
)
```





{:.output .output_png}
![png](../../images/section-01/chapters/03-los-clasicos_4_0.png)




#### _Mapa de calor_ (aka _heatmap_)



{:.input_area}
```python
import altair as alt
import numpy as np
import pandas as pd

# Compute x^2 + y^2 across a 2D grid
x, y = np.meshgrid(range(-5, 5), range(-5, 5))
z = x ** 2 + y ** 2

# Convert this grid to columnar data expected by Altair
data = pd.DataFrame({'x': x.ravel(),
                     'y': y.ravel(),
                     'z': z.ravel()})

alt.Chart(data).mark_rect().encode(
    x='x:O',
    y='y:O',
    color='z:Q'
).properties(
    height = 500,
    width = 500
)
```





{:.output .output_png}
![png](../../images/section-01/chapters/03-los-clasicos_6_0.png)




#### _Histograma_



{:.input_area}
```python
import altair as alt
from vega_datasets import data

movies = data.movies.url

alt.Chart(movies).mark_bar().encode(
    alt.X("IMDB_Rating:Q", bin=True),
    y='count()',
).properties(
    width = 500,
    height = 300,
)
```





{:.output .output_png}
![png](../../images/section-01/chapters/03-los-clasicos_8_0.png)




#### _Mapa_



{:.input_area}
```python
import altair as alt
from vega_datasets import data

counties = alt.topo_feature(data.us_10m.url, 'counties')
unemp_data = data.unemployment.url


alt.Chart(counties).mark_geoshape().encode(
    color='rate:Q'
).transform_lookup(
    lookup='id',
    from_=alt.LookupData(unemp_data, 'id', ['rate'])
).project(
    type='albersUsa'
).properties(
    width=500,
    height=300
)
```





{:.output .output_png}
![png](../../images/section-01/chapters/03-los-clasicos_10_0.png)



