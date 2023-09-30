# SciDavis: Instalación y primeros pasos

## Instalación

Como SciDavis es un programa Libre, podemos descargarlo con facilidad y de manera totalmente gratuita desde el siguiente [link](https://sourceforge.net/projects/scidavis/).
Luego de descargarlo sólo debemos hacer doble click sobre el instalador y seguir los pasos indicados por el mismo.

## Primeros pasos

Luego de abrir SciDavis por primera vez nos encontraremos con una pantalla similar a la siguiente:

<img src="fig/scidavis.png" width="75%" height="75%">

SciDavis combina una hoja de cálculo similar a Excel con un conjunto de herramientas destinadas al análisis y la representación de datos.
La pantalla está dividida en paneles, donde podemos encontrar la hoja de cálculo con un panel de propiedades. 
Los gráficos que creemos irán apareciendo en pantallas nuevas, por otro lado los resultados de los análisis aparecerán también en un panel de resultados. Todos estos paneles consituyen un ¨projecto¨. Cuando guardemos el trabajo realizado deberemos guardar el projecto completo. Esto generará un archivo que contendrá dentro los datos y todos los análisis y gráficos que hayamos realizado.

## Ingresando datos
Los datos pueden ingresarse a mano o pueden importarse desde otro archivo, dejaremos la importación de archivos para estudiar más tarde.

Ingresemos los datos en la tabla de la siguiente manera:

<img src="fig/ventas.png" width="25%" height="25%">

Podemos cambiar los nombres de las columnas haciendo click en el encabezado de las mismas, también podemos editar las propiedades de las columnas en el panel de la derecha:

<img src="fig/propiedades.png" style="zoom:100%;" />

## Graficos de dispersión

Debemos mirar con atención el encabezado de las columnas:

<img src="fig/encabe.png" width="50%" height="50%">

Como vemos, hay una columna $[x]$ y otra $[y]$, podemos cambiar esto haciendo click con el botón derecho sobre el encabezado de las columnas y yendo a la opción "Set column as". SciDavis siempre graficará una o mas columnas $[y]$ respecto de la columna $[x]$ que esté a su izquierda. Para hacer un gráfico de puntos (dispersión) simple solo basta con seleccionar la o las columnas $[y]$ que queremos graficar (no hace falta seleccionar la columna $[x]$) y luego seleccionamos la opción "Scatter" en el siguiente panel:

<img src="fig/scatter.png" width="50%" height="50%">

Deberiamos obtener algo como esto:

<img src="fig/ven1.png" width="50%" height="50%">

## Edicion de gráficos

Todos los campos son editables, usualmente queremos eliminar el título porque lo pondremos debajo de la figura en el manuscrito que estemos escribiendo. La leyenda también es preferible eliminarla cuando hay una sola serie de datos porque es redundante. Recuerden que siempre debemos poner el título adecuado a los ejes con sus unidades:

<img src="fig/ven2.png" width="50%" height="50%">

## Exportacion de figuras en formatos adecuados

Para este tutorial sólo estamos haciendo capturas de pantalla para obtener las imagenes presentadas, sin embargo para la presentación de figuras en informes o articulos cientificos debemos exportar las imagenes en un formato adecuado de manera que no luzcan pixeladas en el documento definitivo.

Un formato ampliamente utilizado es PNG (la calidad debe ser suficientemente alta, usualmente >300ppi), sin embargo para gráficos de este tipo es mejor utilizar formatos de imágenes vectoriales (EPS, VSG, PDF), estos formatos permiten el escalado de la imagen sin pérdida de resolución y permite mantener el tamaño de los documentos pequeños sin comprometer la calidad de imagen. Para exportar el gráfico anterior debemos ir a "export current image" (la ventana del gráfico que queremos exportar debe estar activa):

<img src="fig/exportar.png" width="50%" height="50%">

Luego debemos elejir el formato adecuado, SVG suele ser una buena opción ya que es compatible con varios editores de texto (como Microsoft Word o Libre office). No puede ser insertado en documentos de Google Docs pero de ser necesario puede ser convertido a PNG de alta resolución con otros programas como el servicio en linea [Cloud convert](https://cloudconvert.com/), [ImageMagick](https://imagemagick.org/script/download.php) o [Inkscape](https://inkscape.org/).


 <img src="fig/ven3.png" width="50%" height="50%">


Luego de elegir el formato adecuado y escribir un nombre ponemos "Save" y obtendremos nuestra image de buena calidad:

<img src="fig/ventas-export.svg" />

## Refgresión lineal

Podemos ahora hacer una regresión lineal, para eso debemos tener el gráfico en cuestión como ventana activa, luego debemos hacer click en "fit linear" en:

<img src="fig/fit.png" width="50%" height="50%">

y obtendremos lo siguiente:

<img src="fig/fiteo.png" alt="fiteo" width="50%" height="50%">

En el panel superior "Results log" podremos ver el resultado de la regesión lineal, allí apodremos encontrar los valores de la pendiente y la ordenada al origen. Nuestro gráfico muestra ahora la recta de regresión en color rojo. Podemos cambiar el espesor, el color y muchas otras opciones haciendo click con el botón derecho sobre la linea roja.

En ciertas ocaciones no queremos usar todos los puntos del gráfico para hacer la regresión, supongamos que solo queremos usar los cuatro primeros puntos, debemos usar para esto la opción "select data range":

<img src="fig/range.png" alt="range" width="50%" height="50%">

Luego en el área del gráfico movemos los círculos amarillos para abarcar el rango deseado. Primero debe moverse un círculo y luego con las flechas de direccion del teclado hay que seleccionar el otro círculo y hacer lo mismo:

<img src="fig/ran2.png" width="50%" height="50%">

Si hacemos nuevamente la regresion obtendremos ahora lo siguiente:

<img src="fig/ran3.png" width="50%" height="50%">



