[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sensioai/blog/blob/master/001_python#0/post.ipynb)

# Python para Análisis de Datos

Este es el primer post en una serie en la que aprenderemos a utilizar `Python` para el **análisis de datos**. O lo que es lo mismo, herramientas para manipular, procesar, limpiar y extraer información a partir de imágenes, texto, series temporales o tablas. En esta serie aprenderemos a manejarnos con la sintaxis básica de `Python` que luego combinaremos con algunas librerías orientadas al análisis de datos dentro del gran ecosistema existente. Los motivos que convierten a `Python` en el lenguaje ideal para el análisis de datos son básicamente su **facilidad de uso** y el gran **ecosistema** de librerías que existe enfocado a este tarea en concreto y que podemos utilizar de forma sencilla. Además, `Python` no solo sirve para el análisis de datos sino que también se puede utilizar para implementar servidores [web](https://flask.palletsprojects.com/en/1.1.x/) e incluso hacer [juegos](https://www.pygame.org/wiki/GettingStarted). Otra de las grandes ventajas que `Python` ofrece es que puede utilizarse como capa de integración para código optimizado escrito en otros lenguajes como C o C++. Esto hace que `Python` sea un lenguaje muy versátil, ya que podemos utilizar su sintaxis sencilla para definir la estructura de nuestros programas y, de ser necesario, optimizar algunas partes implementándolas en lenguajes de bajo nivel como C, C++ o CUDA (así es como están implementadas librerías de Deep Learning como `Tensorflow` o `Pytorch`). Existen varios lenguajes alternativos a `Python` para el análisis de datos, algunos ejemplos son `R` o `MATLAB`, muy utilizados en la industria.

Las principales librerías de análisis de datos en `Python`que vamos a ver son las siguientes: 

- `Numpy` es la librería que utilizamos para **cálculo numérico**, ya que nos provee de estructuras de datos y algoritmos con implementaciones optimizadas y eficientes. 
- `Pandas` provee de estructuras de datos de alto nivel para trabajar con **datos tabulares** de forma rápida y sencilla.
- Utilizaremos `Matplotlib` para generar gráficas y **visualizaciones** de nuestros datos.

Entrando en el mundo del `Machine Learning`:

- Utilizaremos `Scikit-Learn` para entrenar modelos de clasificación, regresión o clustering.
- Por último, librerías como `Tensorflow` o `Pytorch` nos proveerán de todo lo necesario para definir y entrenar **redes neuronales** para `Deep learning`.

En este post te enseñaré cómo instalar `Python` y algunas de las diferentes herramientas que podemos utilizar a la hora de hacer nuestros programas. En los próximos posts nos adentraremos en la sintaxis del lenguaje y cómo trabajar con las diferentes librerías mencionadas.

## Instalando Python 🐍

Vamos a empezar instalando `Python`. Es muy probable que ya lo tengas instalado en tu ordenador, para comprobarlo simplemente abre un terminal y escribe `python`. Si recibes un mensaje de error significará que `Python` no está instalado, mientras que si se abre el **interpretador** de `Python` significa que está instalado y puedes empezar a utilizarlo. Si no estás familiarizado con el terminal, puedes abrirlo buscando `command prompt` en `Windows` o `terminal` en `MacOS` (si usas `Linux` asumo que ya conoces de lo que hablo 😛). 

Podemos instalar `Python` de varias maneras. Una de ellas es directamente desde su página [web](https://www.python.org/) sin embargo existe una mejor opción para el análisis de datos: [Anaconda](https://www.anaconda.com/). Al instalar `anaconda` instalaremos no solo `Python` sino también el gestor de paquetes `conda`, que nos permitirá instalar todas las librerías necesarias de manera fácil y optimizado para nuestro sistema. Aún así, la opción que personalmente recomiendo es instalar [Miniconda](https://docs.conda.io/en/latest/miniconda.html) que solo nos instalará `Python` y el gestor de paquetes `conda` sin ninguna librería siendo así una instalación más ligera. 

### Windows

Para instalar `miniconda` en `Windows`, elige la opción de instalación que se ajuste a tu sistema y luego sigue las instrucciones del instalador. 

> ⚠️ Durante la instalación, asegúrate de marcar la opción de añadir `conda` al `PATH`, ya que si no lo marcas es posible que tengas problemas más adelante.

En lo que se refiere a las versiones de `Python`, la opción recomendad es instalar la `versión 3` (`miniconda3`) ya que la `versión 2`de `Python`ha dejado de ser mantenida. Todas las librerías que usaremos son compatibles con la `versión 3`. 

### MacOS

Los pasos para instalar `miniconda` en `MacOS` son muy similares a los de `Windows`. Selecciona el instalador adecuado para tu sistema (de nuevo, escogeremos la `versión 3`) y sigue los pasos del instalador. Puedes verificar que `miniconda`se añadido correctamente en tu archivo `.bash_profile` (de no ser así, puedes añadirlo manualmente).  

### Linux

Los detalles de la instalación de `miniconda`en `Linux` pueden variar en función de la versión de `Linux` que utilices. Para una instalación típica en `Ubuntu` puedes descargarte el instalador adecuado para tu sistema desde la página de `miniconda`. Ésto descargará un `script` que puedes ejecutar con el comando `bash`, lo cual instalará `Python` y `conda`. Puedes verificar que el instalador ha añadido la variable de entorno `PATH` en tu archivo `.bashrc` (o `.zshrc`si usas el terminal `zsh`). De no ser así puedes añadirlo manualmente.

## Hola Mundo

Una vez hemos instalado `Python` podemos ejecutar el **iterpretador** desde el terminal simplemente escribiendo `python`. Si ésto no funciona es probable que haya algún problema con la variable de entorno `PATH`(o quizás tengas que reiniciar el ordenador). Si has podido abrir el interpretador, es el momento de escribir tu primer programa en `Python`. Para ello escribe `print("Hola Mundo")` y luego aprieta `enter`. Deberías ver como el mensaje `Hola Mundo` aparece en el terminal. ¡Felicidades, has escrito tu primer programa en `Python`! 🎉

![](pics/hello.png)

Puedes cerrar el interpretador con la función `exit()`. 

## Instalando librerías

Podemos instalar librerías con el comando `conda install`. Es posible que algunas librerías no esten disponibles en `conda`, en ese caso las podemos instalar con el gestor de paquetes por defecto de `Python`, `pip`.

## *Scripting* con un editor de texto

Normalmente no trabajamos desde el terminal, sino que escribimos nuestros programas (también llamados `scripts`) en un editor de texto. Existen varias opciones especialmente diseñadas para trabajar con `Python` como [Pycharm](https://www.jetbrains.com/pycharm/). Sin embargo, aquí usaremos [VSCode](https://code.visualstudio.com/). Ambos son `IDEs` (*integrated development environment*) por lo que además de poder editar nuestros scripts nos darán muchas funcionalidades que nos harán la vida más sencilla. Instala `VSCode` desde su página web y, una vez instalado, navega a la pestaña de extensiones e instala la extensión de `Python`. Esto nos activará funcionalidades tales como navegación, formateo de código, *linting*, etc.

Una vez instalado, abre `VSCode`y crea un nuevo archivo llamado `main.py`. Añade la línea `print("Hola Mundo")` al archivo y ejecútalo para ver el resultado. Para ello, abre el terminal integrado en `VSCode` y escribe `python main.py` para ejecutar el *script*. El resultado debería ser el mismo que hemos obtenido anteriormente.

![](pics/vscode.png)

## Jupyter Notebooks

Si bien podemos utilizar `VSCode` para implementar y ejectura nuestros programas de `Python`, existe una herramienta muy utilizada en el mundo del análisis de datos que facilita mucho el trabajo sobre todo durante la fase de exploración. Esta herramienta se llama [Jupyter](https://jupyter.org/) y nos ofrece la posibilidad de crear, editar y compartir documentos formados por celdas en las que podemos ejecutar de manera interactiva código, texto y visualizaciones (entre otras cosas). ¡El post que estás leyendo ahora mismo ha sido creado en un *notebook* de Jupyter (exportado al formato adecuado para ser mostrado como una página web)!

En primer lugar, necesitaremos instalar la librería. Para ello, abre un terminal y ejecuta el comando `conda install jupyter`. Una vez instalada la librería podemos ejecutar `jupyter` con el comando `jupiter notebook`. Esto abrirá una nueva pestaña en el navegador desde donde podremos manejar nuestros *notebooks*. Para crear un nuevo *notebook*, haz click en el botón `New` y selecciona la opción `Notebook de Python 3`. En el nuevo notebook, introduce en una casilla tu programa `Hola Mundo`. Al ejecutar la casilla debería obtener el mismo resultado que en las ocasiones anteriores.

![](pics/notebook.png)

Puedes aprender más acerca del funcionamiento de los *notebooks* de `jupyter` [aquí](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb), aun así iremos aprendiendo a manejarnos a medida que vayamos aprendiendo las diferentes herramientas de análisis de datos y haciendo ejemplos.

## Google Colab

La última pieza que introduciré en este post es [Google Colab](https://colab.research.google.com/). Éste es un servicio que nos ofrece Google (gratuito) para editar y ejecutar nuestros notebooks en la nube, en sus propios servidores, y almacenarlos en nuestro *Google Drive*. Además, en Google Colab podremos utilizar una `GPU` o `TPU` durante un tiempo limitado. Esto es una gran ventaja a la hora de entrenar grandes redes neuronales ya que, como hablaremos en otros posts, para entrenar grandes redes se necesita mucha potencia de cálculo, y poder entrenar nuestras redes en una GPU o TPU acelerará el proceso. Otra gran ventaja de `Colab` es que permite compartir *notebooks* muy fácilmente, de manera que cualquier persona pueda acceder al contenido y ejecutar el *notebook* de manera interactiva. Por ejemplo, para abrir este post en `Colab` directamente, puedes hacer click en el botón que tienes arriba.  

## Resumen

En este post hemos introducido `Python` para el análisis de datos, una de las herramientas más utilizada hoy en día gracias a su facilidad de uso y gran ecosistema de librerías que nos permiten llevar a cabo multitud de tareas, desde el procesado de datos hasta el entrenamiento de grandes redes neuronales. Hemos visto cómo instalar `Python` a través de `miniconda` y ejecutado un ejemplo sencillo de programa en el interpretador de `Python` del terminal. También hemos introducido el desarrollo de programas de `Python` con el *IDE* `VSCode` y la herramienta `Jupyter` que nos permite el desarrollo de documentos interactivos en los que podemos ejecutar código, añadir texto, visualizaciones, etc. Por último, hemos hablado de `Google Colab`, un servicio en la nube para almacenar, editar, ejecutar y compartir nuestros *notebooks* con acceso a *hardware* especializado para entrenar grandes modelos. 

Ahora que ya conoces lo que es `Python` y las diferentes formas de trabajar con él para el análisis de datos y *machine learning* podemos empezar a aprender los elementos básicos del lenguaje. Nos vemos en el siguiente post.
