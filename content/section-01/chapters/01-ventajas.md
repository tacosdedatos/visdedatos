Ventajas
========

La ventaja más obvia de `altair` es la facilidad con la que se puede crear un gráfico interactivo. 

> _La idea clave es que está declarando enlaces entre columnas de datos y canales de codificación visual, como el eje x, el eje y, el color, etc. El resto de los detalles del gráfico se manejan automáticamente. Sobre esta idea base de un trazado de gráficos declarativo, se puede crear una sorprendente gama de gráficos y visualizaciones, de simples a sofisticados, utilizando una gramática relativamente concisa._

En realidad `altair` traduce `python` a `Vega-lite` el cual utiliza JSON para especificar los elementos de un gráfico. Esto significa que con un poco de código en `python` puedes crear gráficos que puedes compartir fácilmente en HTML o JavaScript lo cual los hace mucho más faciles de compartir en la red. 

Por ejemplo, supongamos que escribes el siguiente código:

```python
import altair as alt
from vega_datasets import data

grafico = alt.Chart(data.cars.url).mark_point().encode(
    x='Horsepower:Q',
    y='Miles_per_Gallon:Q',
    color='Origin:N'
)
```

con el simple método
```python
grafico.save("grafico.json")
```
ya puedes tener tu gráfico en formato JSON.
```json
{
  "$schema": "https://vega.github.io/schema/vega-lite/v2.json",
  "config": {
    "view": {
      "height": 300,
      "width": 400
    }
  },
  "data": {
    "url": "https://vega.github.io/vega-datasets/data/cars.json"
  },
  "encoding": {
    "color": {
      "field": "Origin",
      "type": "nominal"
    },
    "x": {
      "field": "Horsepower",
      "type": "quantitative"
    },
    "y": {
      "field": "Miles_per_Gallon",
      "type": "quantitative"
    }
  },
  "mark": "point"
}
```

Si lo quieres en HTML para publicarlo en tu sitio web

```python
grafico.save("grafico.html")
```

y tienes el archivo `grafico.html` que se ve así
```html
<!DOCTYPE html>
<html>
<head>
  <script src="https://cdn.jsdelivr.net/npm/vega@3"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@2"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@3"></script>
</head>
<body>
  <div id="vis"></div>
  <script type="text/javascript">
    var spec = {
      "$schema": "https://vega.github.io/schema/vega-lite/v2.json",
      "config": {
        "view": {
          "height": 300,
          "width": 400
        }
      },
      "data": {
        "url": "https://vega.github.io/vega-datasets/data/cars.json"
      },
      "encoding": {
        "color": {
          "field": "Origin",
          "type": "nominal"
        },
        "x": {
          "field": "Horsepower",
          "type": "quantitative"
        },
        "y": {
          "field": "Miles_per_Gallon",
          "type": "quantitative"
        }
      },
      "mark": "point"
    };
    var opt = {"renderer": "canvas", "actions": false};
    vegaEmbed("#vis", spec, opt);
  </script>
</body>
</html>
```
