![Marcha de Napoleón](images/napoleon.gif)
<br>**Figura 1**: _Charles Joseph Minard: “Carte Figurative des pertes succesives en hommes de l’Armée Française dans la campagne de Russie 1812-1813”, Paris, 1869._
# Introducción

>_Los gráficos de datos visualizan visualmente las cantidades medidas mediante el uso combinado de puntos, líneas, un sistema de coordenadas, números, símbolos, palabras, sombreado y color._<br>...<br>
_Los gráficos de datos modernos pueden hacer mucho más que simplemente sustituir tablas estadísticas pequeñas. En el mejor de los casos, los gráficos son instrumentos para razonar sobre información cuantitativa. A menudo, la forma más efectiva de describir, explorar y resumir un conjunto de números, incluso un conjunto muy grande, es mirar las imágenes de esos números. Además, de todos los métodos para analizar y comunicar información estadística, los gráficos de datos bien diseñados son los más simples y, al mismo tiempo, los más potentes._ <br>
> ###### Edward R. Tufte, *The Visual Display of Quantitative Information*, 2da Edición


La visualización de datos efectiva es una habilidad técnica cada día más codiciada. No es sólo una herramienta útil para presentar resultados sino también para la exploración eficáz de datos. 
Los gráficos bien diseñados son capaces de transferir una gran cantidad de información en poco tiempo. Toma por ejemplo la figura 1. La figura 1, de Charles Joseph Minard, es una visualización de la marcha de Napoleón a Rusia. De izquierda a derecha puedes ver como la cantidad de soldados va disminuyendo (en dorado) conforme pasa el tiempo y se acercan a Rusia. En el panel inferior Minard también esta visualizando la temperatura del día. Minard esta representando 6 dimensiones de sus datos:
* **cambio en la cantidad** de soldados
* la **dirección** de el ejercito
* locación en un plano bidimensional - (X, Y), o en este caso de locación geografica, **longitud** y **latitud**.
* **temperatura**
* tiempo / **fecha**

Esta transferencia de información es casi instantánea algo que sería imposible leyendo una tabla de 6 columnas con la misma información en forma de números.

![paris](images/paris.jpeg)
<br>**Figura 2**: _Étienne-Jules Marey. Visualización del horarios de los trenes entre Lyon y París en 1885_

La figura 2 muestra el horario de trenes entre las ciudades de París y Lyon en Francia en 1885. Es una visualización intuitiva, uno la lée casi sin pensar y puede darse cuenta que existe una distancia mayor de Dijon a Macon que de París a Monterre, claro si uno fuera a tomar ese tren. No sólo eso, uno se da cuenta que si toma el tren de las 11 en París, va a tener una parada de 30 minutos en Dijon ya que se llega a las 5:30PM pero se sale a las 6PM. Esto es claro en el abruto salto en la línea representando nuestro tren. Este calculo no es díficil de notar en un boleto, tal vez veríamos los horarios de llegada y salida de cada parada en nuestro recorrido pero la representación gráfica nos entrega esa información de una manera todavía más rápida y eficáz.

*** 

Este libro es un documento vivo sobre la visualización de datos en `python` y específicamente utilizando la biblioteca `altair`. Aprenderás un poco sobre _la grámatica de gráficos_ y sobre `pandas`, la biblioteca de análisis de datos más popular de `python`. También aprenderás a como visualizar tus datos utilizando `altair` y como compartirlos en la red, ya sea en tu blog, en el sitio de tu empresa, o en tus redes sociales. 

En algunos capítulos observarás el botón __Interactuar__<br>
<img src="images/interactuar.png" alt="Interactuar" height="120">
<br> al hacerle clic a ese botón activarás un __JupyterHub__ en [mybinder.org](https://mybinder.org) en el cual podrás practicar los ejercicios sin necesidad de instalar nada. 

¡La guía seguirá creciendo con el tiempo con más material y más ejercicios así que asegurate de regresar de vez en cuando a ver que hay de nuevo!

Si encuentras un error o tienes sugerencias o comentarios te invito a que abrás un __issue__ en el [repo de GitHub](https://github.com/cimarron-io/guia-altair/issues).
