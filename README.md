# Introduccion al analisis y representacion de datos para Quimica General e Inorgánica

## La importancia del analisis de datos

Simplificando bastante la cuestion podemos decir que la labor cientifica tiene como partes escenciales las siguientes etapas:

1. Formulacion de Hipotesis.
2. Diseno de experimentos.
3. Recoleccion de datos crudos.
4. Analisis y representacion de datos.
5. Contrastacion de las hipotesis iniciales

Nos centraremos aqui en el punto 4: "Analisis y representacion de datos". En la mayoria de los casos, de los experimentos que se realizan en el laboratorio no se obtienen directamente las respuestas a las preguntas de partida. Aun cuando los experimentos estan bien disenados es necesario tratar los datos crudos obtenidos de manera que puedan ser interpretados y utilizados para la contrastacion de hipotesis.

El tratamiendo de datos por lo general incluye la organización, filtrado y limpieza de los datos crudos; el analisis estadistico de la mismas (obtencion de promedios, desviaciones estandar, exclusion de puntos anomalos, etc); el modelado de los mismos, es decir el tratamiento matematico de los datos aplicando teorias previamente establecidas para la obtencion de distintos parametros; y la representacion gráfica de uno o mas de los pasos anteriores para facilitar la visualizacion y de los resultados obtenidos y la toma de decicion sobre que hacer respecto de nuestras hipotesis de partida.

## Informatica

Existen diversos softwares que poden asistir el tratamiento y la representacion de datos. Es importante destacar que las herramientas informaticas son solo eso, herramientas, y que nunca suplantaran un correcto entedimiento de las teorias necesarias para interpretar los datos obtenidos y sacar conclusiones de los mismos. Sin embargo habiendo dicho esto, es altamente recomendable aprender a usar estas herramientas porque pueden ahorrarnos mucho tiempo y esfuerzo en nuestros projectos. Con ayuda de estos programas pueden hacerse análisis  que serian imposibles de hacer sin el uso de computadoras. La ciencia de datos es una disciplina en auge que aborda todos estos temas, nosotros aca vamos simplemente a dar algunos lineamientos introductorios sobre como analzar conjuntos pequenos de datos, similares a los que podemos obtener durante los trabajos practicos de laboratorio.

El software puede clasificarse en dos grandes categorías considerando el tipo de licencias que posee: privativo o libre.

El software privativo abarca todos los programas con copyright. No puede ser modificado ni compartido y para poder usarlo de manera legal se tiene que poseer una copi original del mismo habiendo adquirido previamente la licencia necesaria para usarlo. Usualmente las licencia del softwate privativo usado en ciencia son muy costosas. Ejemplos de este tipo de software comunmente usados son: 

1. Microsoft Office (Word, Excel y Power Point, para edicion de texto, hojas de calculo y presentaciones)
2. Origin Pro Lab, Graphpad (para analisis y representacion de datos)
3. Photoshop, Illustrator, Corel Draw (para edicion de figuras)
4. Endnote (para gestionar bibliografía)

Aunque existe la posibilidad de usar estos programas de manera ilegal a traves de la instalacion de copias obtenidas por canales diversos, existe otro tipo de software que tiene detras una filosofia de trabajo opuesta al software privativo: el software libre.

El software libre usualmente posee licencia de Copy Left, puede ser compartido libremente y el codigo es de libre acceso para ser estudiado o modificado si es necesario. Ademas, aunque no exclusivamente, la gran mayoria del software libre es tambien gratituito. Estos programas pueden descargarse libremente de los repositorios oficiales y su instalacion y actualizacion suele ser muy sencilla de realizar.

Algunas alternativas a los programas mencionados anteriormente son las siguientes:

1. [Libre Office](https://www.libreoffice.org/) (Writer, Calc, Impress, para edicion de texto, hojas de calculo y presentaciones)
2. [Alpha plot](https://alphaplot.sourceforge.io/), [SciDavies](https://scidavis.sourceforge.net/), [Gnuplot](http://www.gnuplot.info/), [R](https://www.r-project.org/), [Python](https://www.python.org/) (para analisis y representacion de datos)
3. [GIMP](https://www.gimp.org/) and [Inkscape](https://inkscape.org/) (para edicion de figuras)
4. [Zotero](https://www.zotero.org/), [Mendeley](https://www.mendeley.com/) (para gestionar bibliografia)

Todos los programas mencionados en la lista anterior son muy utiles y es recomendable que los chequeen, sin embargo la curva de aprendizaje sobre todo para aquellos que no tienen interfase grafica (R, Python, Gnuplot) puede ser un poco empinada al comienzo. R es uno de los lenguajes de programacion mas usado en todo el mundo para analisis y representacion de datos, en el siguiente [link](https://github.com/foni90mdq/introduccion-a-r.github.io) podran encontrar una introduccion aquellos que estén interesados.

Para los trabajo practicos que desarrollaremos en Quimica General es suficiente con usar la suite Libre Office. Usaremos Calc (programa de hoja de calculo alternativo a Excel) y Writer (programa de hoja de calculo alternativo a Excel).

## Ejemplo 1: Solubilidad

Queremos investigar como varia la solubilidad del NaCl con la temperatura. Se preparan soluciones saturadas de NaCl a distinta temperatura y se mide su concentración. Los datos obtenidos son los que se muestran en la Tabla 1. 

Tabla 1. Solubilidad de NaCl obtenida a distintas temperaturas.

| Muestra | Temperatura (C) | Solubilidad (g NaCl/100 g water) |
| ------- | --------------- | -------------------------------- |
| 1       | 0.00            | 35.2                             |
| 2       | 20.0            | 36.1                             |
| 3       | 40.0            | 37.0                             |
| 4       | 60.0            | 37.7                             |
| 5       | 80.0            | 38.4                             |
| 6       | 100.0           | 39.0                             |

Este ejemplo servira para tener un primer acercamiento a como deben presentarse y analizarse los datos obtenidos. Tanto tablas como figuras deben tener un tiutulo, en las tablas suele ir antes de la tabla, como se mostros en el ejemplo y en las figuras debajo. Siempre deben numerarse (las tablas por un lado, las figuras por otro) y deben estar siempre referidas en el texto, como se hizo en el parrafo anterior. Todas las variables deben escribirse con unidades adecuadas.

Como dijimos antes, queremos ver como varia la solubilidad del NaCl con la temperatura, es decir, queremos ver si existe alguna funcion matematica que relaciones la solubilidad (**s**) con la temperatura (**T**), es decir, queremos encontrar

s=f(T) 																														(1)

Las ecuaciones deben escribirse con un editor de ecuaciones apropiado y deben numerarse para poder referidas en el texto (Eq. 1)

Hay dos variables estudiadas, **T** y **s**. Lasvariables dependientes son las que se miden durante el experimento (**s**) mientras que las Independientes son las que son fijadas *a priori* por el disenio experimental, en este caso, **T**.

Cuando queremos graficar dos variables es usual poner la independiente en el eje x y la dependiente en el eje y como se muestra en la Fig. 1.

![solubilidad](fig/solubilidad.png)

Figura 1. Variacion de la solubilidad del NaCl con la temperatura.

En este primer ejemplo pueden verse algunos espectos que es importante tener en cuenta a la hora de hacer una figura para informe o un articulo cientifico. Todas las fiugras (y tambien las tablas) deben tener un titulo (pueden tambien poseer una descripcion breve) y deben estar referidas en el texto de forma similar a como se hizo aqui.

Cuando se presentan graficos en los que queremos mostrar la relacion entre dos variable numericas continuas como en este caso, el tipo mas usual utilizado es el grafico de *dispersión*, en el que cada punto representa uno de los datos obtenidos. Como regla general no deben unirse los puntos con lineas segmentadas. El area donde los datos esta graficados debe ocupar un porcentaje grande del area disponible y la escala de los ejes debe ser adecuada y los mismos deben poseer el nombre de la variable representada con su unidad correspondiente. El tamano de la fuente utilizada para ejes y escalas debe ser apropiada para que puedan leerse con facilidad en el documento terminado.









