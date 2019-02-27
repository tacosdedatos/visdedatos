---
title: 'Creación de Gráficos'
prev_page:
  url: /section-02/6/conclusion
  title: 'Conclusión'
next_page:
  url: /section-03/1/equis-y-que
  title: 'Equis y ¿Qué?'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---
Creación de Gráficos
====================

En el módulo anterior aprendiste sobre la anatomía básica de un gráfico y como `altair` construye gráficos basado en la _gramática de gráficos_. Ya aprendimos sobre los objetos `Chart`, sobre los marcadores `.mark_****()` y como asignamos nuestros datos a elementos del gráfico con `.encode()`.  En este módulo aprenderemos más a fondo los elementos que componen un gráfico en `altair`. 

En la sección 5 del capítulo 2 aprendemos a crear mapas en `altair` y utilizamos un nuevo objeto para representar nuestros datos: `alt.Data()`. Hasta el momento, habiamos estado utilizando __DataFrames__ de `pandas` y en general es a lo que nos mantendremos. Así como existe el objeto `Data` de `altair`, existen otros objetos que representan elementos de un gráfico. Por ejemplo, tenemos:

* `alt.X()` y `alt.Y()`: Que representa el valor de X y Y, respectivamente, en tu gráfico.
* `alt.Scale()`: Que representa una _escala_. Las escalas en `altair` son utlizadas de varias formas pero en general su función es _traducir_ una serie de valores a otra. 
* `alt.Legend()`: Que representa el la leyenda de tu gráfico.

Y muchos más que estaremos descubriendo conforme vamos explorando `altair`. Cada uno de estos objetos acepta argumentos que te dan un sinfín de opciones para personalizar tus gráficos. En las siguientes secciones practicaremos varias formas de personalizar nuestros gráficos e introduciremos estos nuevos objetos.