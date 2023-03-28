[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-f4981d0f882b2a3f0472912d15f9806d57e124e0fc890972558857b51b24a6f9.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=10662363)
# 🙌 ¡Bienvenido a tu primera clase!

# Clase 1: Herramientas de desarrollo y línea de comandos

## Tabla de Contenido

1. [Sistemas operativos](dev_tools.md#operating-systems)
2. 2. [La línea de comandos](dev\_tools.md#the-command-line)
3. 3. [Terminal de nivel principiante](dev\_tools.md#nivel-principiante)&#x20;
   1. 1. [Navegación en el terminal](dev\_tools.md#navigating-in-terminal)
   2. 2. [Trabajar con archivos y carpetas](dev\_tools.md#working-with-files-and-folders)
   3. 3. [Listado de archivos y banderas](dev\_tools.md#listing-files-and-flags)
4. 4. [Ejercicios básicos de terminal](dev\_tools.md#terminal-basics-exercises)
5. [Terminal de nivel intermedio](dev\_tools.md#intermediate-level)
   1. 1. [Permisos y enlaces](dev\_tools.md#permissions-and-links)
   2. 2. [Redirección](dev\_tools.md#redirection)
   3. 5. [Tuberías](dev\_tools.md#piping)
6. 6. [Permisos, redirección y ejercicios de tuberías](dev\_tools.md#permissions-redirection-and-piping-exercise)
7. 7. [Herramientas de desarrollo](dev\_tools.md#development-tools)
8. 8. [Extensiones de código de Visual Studio](dev\_tools.md#optional-visual-studio-code-extensions-for-web-development)
9. [Más recursos](dev_tools.md#more-resources)
10. [Nivel avanzado - 1](dev\_tools.md#advanced-level-1-optional) **{ OPCIONAL }**
11. 11. [Nivel avanzado - 2](dev\_tools.md#advanced-level-2-optional) **{ OPTIONAL }**

## Sistemas operativos

Un Sistema Operativo (SO) es un programa potente, y normalmente grande, que controla y gestiona el hardware y el software de un ordenador. Todos los ordenadores y dispositivos similares requieren sistemas operativos, incluidos portátiles, tabletas, ordenadores de sobremesa y teléfonos inteligentes. El sistema operativo realiza todas las tareas básicas, como la gestión de archivos, la gestión de memoria, la gestión de procesos, el manejo de la entrada y la salida, y el control de dispositivos periféricos como unidades de disco e impresoras.

Los sistemas operativos más comunes para ordenadores de sobremesa y portátiles son:

* Microsoft Windows (Windows 95, Windows 7, Windows 10,...)
* Linux (Debian, Red Hat, Ubuntu,..)
* MacOS
* Chrome OS
* Android e iOS son sistemas operativos para dispositivos móviles.

#### Unix

Unix es una familia de sistemas operativos. La primera versión se desarrolló a partir de 1969. Unix se caracteriza por ser portable y multitarea.

Los sistemas operativos Unix se utilizan ampliamente en multitud de dispositivos que van desde los superordenadores más capaces hasta los teléfonos móviles y ordenadores que utilizamos a diario. La filosofía de los sistemas Unix se caracteriza por:

* un sistema de archivos jerárquico,
* una gran colección de pequeños programas que pueden trabajar en serie,
* el uso de archivos de texto para almacenar los datos,
* el tratamiento de los dispositivos como archivos.

Linux y MacOS son ejemplos de sistemas Unix.

#### Linux

Linux es una familia de sistemas operativos tipo Unix que utilizan el núcleo Linux. El nombre proviene del programador original, un estudiante llamado Linus Torvals, que en 1991, trabajando con el proyecto GNU de la Fundación para el Software Libre, creó la primera versión de este sistema operativo.

El desarrollo de Linux es uno de los ejemplos más claros de desarrollo de software libre y de código abierto por parte de una comunidad diversa de programadores de todo el mundo. Cualquiera puede utilizar el sistema operativo, estudiarlo y modificarlo. La naturaleza de código abierto de Linux está protegida por la licencia GPL (GNU General Public License).

#### Ubuntu

Ubuntu es una distribución de Linux. Es un sistema operativo de código abierto dirigido a usuarios de escritorio, y sus puntos fuertes son que es fácil de usar e instalar. Aunque el escritorio es algo diferente al de Windows o Mac OS, un usuario acostumbrado a cualquiera de estos sistemas operativos no tendrá muchos problemas para familiarizarse con Ubuntu. Ubuntu es una distribución de Linux basada en Debian y compuesta en su mayor parte por software libre y de código abierto. Ubuntu se publica oficialmente en tres ediciones: Desktop, Server y Core para dispositivos y robots del Internet de las cosas.

Si estás usando [Ubuntu](https://ubuntu.com/), verás esta pantalla:

![](<.content/image (97).png>)

Demo de Ubuntu:

* El Escritorio amigable
* El sistema de archivos: navegar por carpetas y archivos usando el Administrador de Archivos
* El software de Ubuntu: una herramienta para instalar software fácilmente

## La línea de comandos

La **Línea de Comandos**, también conocida como **Bash**, **Terminal** o **Shell** (**Línea de Comandos** ó **Símbolo de sistema** en español) es una forma de controlar un ordenador, basada en una interfaz de texto.

![](<.content/image (31).png>)

¿Por qué debo utilizar la línea de comandos/terminal?

* Una vez que conozcas los conceptos básicos, te ayudará a interactuar con tu ordenador más rápidamente.
* Algunos programas para desarrolladores deben utilizarse siempre desde un terminal.
* Tienes más control sobre el software
* Te permite crear scripts (listas de comandos) y automatizar tareas manuales.
* Es lo que usan los hackers en las películas.

#### ¿Cómo uso el terminal en mi ordenador?

Aquí tienes las instrucciones para los tres sistemas operativos:

* **MacOS:** Puedes encontrar el Terminal.app en tus Aplicaciones, en la carpeta Utilidades. Una forma alternativa de abrir el Terminal es buscar con Spotlight y escribir "terminal". Selecciona la aplicación llamada terminal y pulsa la tecla de retorno. Esto debería abrir una aplicación con fondo negro. Cuando veas tu nombre de usuario seguido de un signo de dólar, estarás listo para empezar a utilizar la línea de comandos.
* **Linux:** Puedes abrir la Terminal pulsando directamente \[ctrl+alt+T] o puedes buscarla haciendo clic en el icono del guión (#), escribiendo "terminal" en el cuadro de búsqueda y abriendo la aplicación Terminal. Se abrirá una aplicación con fondo negro. Cuando veas tu nombre de usuario seguido de un signo de dólar, estarás listo para empezar a utilizar la línea de comandos.
* **Windows:** Windows tiene su propio **Instructor de Comandos**. Es muy similar a la línea de comandos de Unix, pero algunos comandos no son exactamente iguales. Para ver las principales diferencias vaya a este [enlace](https://enexdi.sciencesconf.org/data/pages/windows\vs\_mac_commands\_1.pdf). Debido a estas diferencias, y porque queremos aprender comandos UNIX, usamos el **Git Bash**. Ve al botón "Inicio" de Windows y busca el programa **Git Bash**. Al abrirlo verás una pantalla como ésta:

![](<.content/image (105).png>)

Después de seguir las instrucciones, abre un terminal y escribe `ls`, luego pulsa la tecla `Enter`. ¿Qué verás?

#### Comandos más utilizados

Estos son los comandos más utilizados con los que te sentirás cómodo rápidamente durante el curso. Estos comandos te permiten moverte eficazmente por el sistema de ficheros y escribir software en tu portátil. Hay más comandos en las tablas con más comandos y descripciones más abajo.

* `cd` - cambiar directorio. Para subir un nivel de carpeta y entrar en el directorio padre usa: `cd ..`
* `ls` - lista el contenido de un directorio. También puede usarse como `ls [nombre_directorio]` para listar el contenido de un directorio específico sin moverse (con `cd`) a él.
* `pwd` - imprime el directorio de trabajo: imprime la ubicación completa de la carpeta en la que se está trabajando
* `mkdir [nombre]` - make directory: crea un nuevo directorio, con el `nombre` dado después de un espacio
* `touch [nombre_archivo]` - crear un nuevo archivo, con el nombre dado (no olvide añadir la extensión, como `.css` o `.html`)
* `rm [nombre_archivo]` - elimina un archivo
* `rm -r [nombre_directorio]` - elimina un directorio (**y todos los archivos dentro de ese directorio**)

**Obtener ayuda

Cuando estés atascado y necesites ayuda con un comando, la ayuda suele estar a sólo unas pulsaciones de distancia. La ayuda para la mayoría de los comandos está integrada en los propios comandos, disponible a través de programas de ayuda en línea (como [https://linux.die.net/man](https://linux.die.net/man)) y, por supuesto, en línea.

**Utilizar la ayuda integrada de un comando***.
Muchos comandos (pero no todos) tienen pantallas de ayuda simples que pueden ser llamadas con banderas de comando especiales. Estas opciones suelen tener el aspecto de `-h` o `--help`. Ejemplo: `grep --help`.

**Manuales en línea: las páginas man***.
La mejor fuente de información para la mayoría de los comandos son las páginas de manual, también conocidas como páginas man. Para leer la página man de un comando, escriba `man` más un espacio y el comando.

| Ejemplo
| --------- | -------------------------------------- |
| Man ls: Obtén ayuda sobre el comando ls.
| `man man` | Obtén información sobre el manual |



## Nivel Principiante



### { Navegando en Terminal. }

#### Objetivos:

Al finalizar este capítulo, deberás ser capaz de:

* Definir qué es Terminal y cómo está estructurado
* Navegar y listar archivos en su máquina
* Definir los siguientes términos: shell, terminal, directorio, ruta absoluta, ruta relativa

| Linux/Mac | Windows | Descripción
| ------------------ | --------------- | -------------------------------------------------------------------------- |
| Imprimir directorio de trabajo: muestra la ubicación actual.
| Cambiar directorio: vuelve al directorio inicial.
| cambiar al directorio especificado
| `cd ~` | | significa directorio personal; acceso directo al directorio personal | `cd ..` | cambiar directorio
| `cd ..` | `cd ..` | subir un directorio | `cd ..` | subir un directorio
| `cd -` | vuelve al directorio de su ubicación anterior | `ls
| Lista todos los ficheros del directorio actual
| `ls directorio` | `dir directorio` | lista todos los ficheros en el directorio especificado | | `ls -l` | `dir /w
| `ls -l` | `dir` | lista todos los ficheros en formato largo: un fichero por línea, con información sobre el fichero | | `ls -a` | `dir /w
| `ls -a` | `dir /a` | lista todos los ficheros, incluidos los ocultos (= nombres de fichero que empiezan por .) | `ls -ld directorio` | lista todos los ficheros en formato largo: un fichero por línea, con información sobre el fichero
| `ls -ld directorio` muestra información detallada sobre el directorio
| `ls /usr/bin/d*` | `dir d*.*` | lista todos los ficheros que empiezan por d en el directorio `/usr/bin` | `ls -ld directorio` | muestra información detallada sobre el directorio

****

#### ¿Qué es Terminal?

Terminal es una aplicación que nos proporciona una interfaz de línea de comandos (o CLI) para interactuar con el ordenador. Todo lo que puedes hacer en Finder/Explorador de Windows lo puedes hacer en Terminal. Los desarrolladores utilizan Terminal porque suele ser mucho más rápido utilizar Terminal que una interfaz gráfica de usuario (GUI) como Finder/Windows Explorer. Aunque la interfaz de Terminal puede parecer desalentadora al principio, con un poco de práctica, estarás al día en muy poco tiempo.

#### ¿Qué es un shell? Bash/ZSH

También oirás el término "shell" cuando aprendas sobre Terminal, así que es importante distinguir entre estos términos. De [Stack Overflow](https://superuser.com/questions/144666/what-is-the-difference-between-shell-console-and-terminal):

> El **shell** es el programa que realmente procesa los comandos y devuelve la salida. La mayoría de los shells también gestionan los procesos en primer y segundo plano, el historial de comandos y la edición de la línea de comandos. Estas características (y muchas más) son estándar en bash, la shell más común en los sistemas linux modernos. (Nosotros usamos `zsh`).
>
> Un **terminal** se refiere a un programa que ejecuta un shell. Hace décadas, era un dispositivo físico que consistía en poco más que un monitor y un teclado. A medida que los sistemas unix/linux añadieron mejores sistemas de multiprocesamiento y ventanas, este concepto de terminal se abstrajo en software.

Si usas Windows, hay una herramienta estupenda llamada [Babun](https://babun.github.io/), que es una shell que puedes instalar y usar los mismos comandos que si estuvieras en Mac o Linux. Esto no es esencial, pero su uso le permitirá seguir más fácilmente el material.

#### Cómo está estructurado Terminal

En Terminal, todos los archivos y carpetas comienzan en el directorio raíz. El directorio raíz se marca con un `/`. Dentro del directorio raíz están los archivos/carpetas esenciales que tu máquina necesita, pero no modificamos los archivos y carpetas en el directorio raíz a menudo. Dentro del directorio raíz, tenemos una carpeta llamada `Users` que contiene todas las cuentas de usuario de tu ordenador. Si te mueves al directorio de tu cuenta de usuario, estarás en el directorio `home`, que se indica con `~`. Por ejemplo, si tu nombre de usuario en el ordenador es `eschoppik`, entonces tu directorio home sería `/Users/eschoppik`. Un sinónimo de la ruta `/Users/eschoppik` es `~` cuando estás conectado como `eschoppik`.

#### Moverse

Lo primero que querrás empezar a entender cuando uses Terminal es cómo navegar de carpeta en carpeta. Uno de los comandos más comunes que usarás en la Terminal es `cd` que es la abreviatura de "cambiar directorio". Para cambiar un directorio, escribe `cd` seguido del directorio o una ruta al directorio. Si queremos movernos hacia arriba en un directorio usamos `cd ..` y si queremos movernos hacia dentro de un directorio especificamos el nombre del directorio al que nos estamos moviendo. Por ejemplo, si estás en tu directorio personal y escribes `cd Escritorio`, te moverás a tu directorio Escritorio.

Acabamos de mencionar que puedes escribir `cd` seguido de un directorio o ruta. Pero, ¿qué es una ruta? Aprendamos algo más de vocabulario:

#### Rutas absolutas vs. Rutas relativas

Una ruta es simplemente la forma de llegar a un archivo o carpeta; es como una dirección para el archivo o carpeta que estás tratando de alcanzar. Cuando especificamos una ruta que comienza en el directorio raíz `/`, la llamamos ruta absoluta. Por ejemplo, si actualmente estoy en el directorio raíz `~` y me gustaría cambiar de directorio a mi carpeta Escritorio, puedo hacerlo de dos de las siguientes maneras:

1. 1. `cd Escritorio` - relativa a donde estoy actualmente
2. 2. `cd /Users/eschoppik/Desktop` - absoluto, empezando desde la raíz (primero `/`, luego `Users`, luego `eschoppik`, luego `Desktop`)

**Preguntas para responder**

* ¿Cuál es la diferencia entre `/` y `~`? ¿Cómo llamamos a cada uno de estos directorios?
* ¿Qué comando usamos para cambiar de directorio?
* ¿Cuál es la diferencia entre una ruta absoluta y una relativa?



### { Trabajando con Archivos y Carpetas. }

#### Objetivos

Al final de este capítulo, usted debe ser capaz de:

* Crear archivos y carpetas en Terminal usando `mkdir` y `touch`.
* Mover archivos y carpetas en Terminal usando `mv`.
* Copiar archivos y carpetas en la Terminal usando `cp`.
* Eliminar archivos y carpetas en Terminal usando `rm` y `rmdir`.
* Explicar qué es una bandera en Terminal
* Explicar qué hacen los siguientes comandos: `whoami`, `pwd`, `cat`, `echo`, `less`, `open`.



| Linux/Mac | Windows | Descripción |
| --------- | ----------------------- | ------------------------------------------------- |
| Copiar un archivo de una ubicación a otra.
| Mueve un archivo a una nueva ubicación o cambia el nombre de un archivo.
| eliminar (= borrar) un fichero
| crear un nuevo directorio
| eliminar un directorio.



#### Creación de archivos y carpetas

Ahora que tenemos una buena comprensión de cómo cambiar directorios y navegar en la Terminal, vamos a ver cómo podemos crear nuestras propias carpetas y archivos. Para crear una carpeta usamos el comando `mkdir` (abreviatura de "make directory"), seguido del nombre (o nombres separados por espacios) de la(s) carpeta(s) que queremos crear. Así que vayamos a nuestro `Desktop` y creemos una nueva carpeta llamada `primera_carpeta`.

```
cd /Usuarios/$USUARIO/Escritorio
mkdir primera_carpeta
```

Vaya... deberías estar preguntándote, ¿qué es eso de `$USUARIO`? Es una variable de entorno en tu shell que mantiene un registro del usuario actual del shell. También puedes ver quién es `$USER` tecleando `echo $USER` o usando el comando `whoami`. Prueba ambos métodos para comprobar quién es el usuario actual.

Como otra nota al margen, este tutorial usará rutas absolutas para navegar, sólo para facilitarte el seguimiento. Sin embargo, no sientas que DEBES usar rutas absolutas sobre las relativas.

Ahora que hemos creado la `primera_carpeta`, ¿cómo cambiamos los directorios dentro de ella? Si estás pensando en el comando `cd`, ¡estás en lo cierto! Así que vamos a `cd /Usuarios/$USUARIO/Escritorio/primera_carpeta`. O, si ya estás en tu Escritorio, puedes simplemente `cd primera_carpeta`.

Acabamos de mencionar "si ya estás en tu Escritorio". ¿Cómo saber en qué directorio se encuentra si lo olvida? Por suerte, existe un comando muy útil llamado `pwd` que mostrará la ruta absoluta y te permitirá saber en qué directorio estás trabajando. Así que si alguna vez no estás seguro, teclea `pwd` (que es la abreviatura de _present working directory_).

Ahora que estamos dentro de nuestra nueva carpeta, `primera_carpeta`, vamos a crear un nuevo archivo. Una forma sencilla de crear un archivo es con el comando `touch`. El comando `touch` simplemente crea un archivo vacío. Vamos a crear un fichero llamado `primer_fichero`: `touch /Usuarios/$USUARIO/Escritorio/primera_carpeta/primer_fichero`. Alternativamente, si te encuentras en el directorio `primera_carpeta`, puedes simplemente escribir `touch primer_archivo`. Ahora use el comando `ls` para verificar que su archivo fue creado. `ls`, que es la abreviatura de "list", listará todos los archivos y carpetas de tu directorio actual.

#### Mostrar el contenido de un archivo

Un comando muy común para mostrar el contenido de un archivo es el comando `cat`. Si tecleas `cat NOMBRE_DE_FICHERO` puedes ver el contenido del fichero fácilmente, ahí mismo en el Terminal. Pruébalo con el fichero que acabas de crear, "primer_fichero". No deberías ver ninguna salida después de pulsar enter. No hay salida porque "primer_archivo" está vacío.

Vamos a añadir algo de texto al fichero para poder utilizar `cat`. Escribe:

`echo "Hola Mundo" > primer_fichero`.

El comando `echo` simplemente escribe texto en el terminal. El `>` se llama redirección. El `>` redirige la salida del comando de la izquierda al fichero de la derecha. Veremos más redirecciones en el próximo capítulo.

Ahora intenta usar `cat` en el fichero de nuevo. ¿Ves "Hola Mundo"?

Hay otras formas de ver el contenido de un fichero en el terminal. Prueba a usar el comando `less`: `less primer_fichero`. `less` es un programa que muestra el contenido de un fichero y permite al usuario navegar arriba y abajo por el fichero o buscar texto en el fichero. Para salir de `less`, pulse `q`.

#### Abrir un fichero

Si quieres abrir un fichero, puedes utilizar el comando `open`. Así, si queremos ver el contenido de `primer_archivo` podemos hacer `open primer_archivo`. El comando `open` también es muy útil si quieres abrir todos los archivos y carpetas de un directorio (utilizando la interfaz de usuario de tu sistema operativo). Pruebe a teclear `open .` y vea lo que ocurre. Si estás en Windows, el comando para hacer esto es `start NAME_OF_FILE`.

#### Mover archivos y carpetas

Ahora que ya sabes cómo crear archivos y carpetas, pasemos a otra operación esencial: mover y copiar carpetas. Para mover archivos y carpetas utilizamos el comando `mv`. ¡Vamos a probarlo!

Vuelve al Escritorio tecleando `cd ~/Escritorio` y creemos un nuevo archivo llamado `prueba.txt` (¿recuerdas ese comando? Si no es así, deja de leer y repasa la sección anterior). Ahora en tu Escritorio deberías tener una carpeta llamada `primera_carpeta` y un archivo llamado `prueba.txt`. Nuestro objetivo es mover `prueba.txt` dentro de `primera_carpeta` - vamos a hacerlo usando el comando `mv`. Primero asegúrate de que estás en el Escritorio (teclea `pwd` para estar seguro), teclea `mv prueba.txt primera_carpeta/prueba.txt`, y pulsa intro.

¿Ha funcionado? No deberías ver ningún tipo de mensaje de éxito o confirmación desde Terminal, pero tampoco deberías ver un error. Esto es muy común cuando se trabaja con Terminal: verás mensajes de error si un comando es incorrecto, pero muy raramente verás un mensaje de éxito. En otras palabras, ninguna noticia es una buena noticia. En este caso, para asegurarnos de que hemos hecho lo correcto, vamos a `cd` en `primera_carpeta` y tecleamos `ls`. Deberíamos ver `test.txt` dentro de `first_folder`.

#### Copiando archivos y carpetas

A veces podemos querer hacer una copia de un fichero o una carpeta. Para copiar un fichero, utilizamos el comando `cp` (abreviatura de copy). La sintaxis general es la siguiente

```
cp RUTA_AL_ARCHIVO_ORIGINAL RUTA_AL_ARCHIVO_COPIADO
```

Por ejemplo, si quisiéramos crear una copia de `prueba.txt` y llamarla `prueba_copia.txt`, podríamos introducir el siguiente comando (suponiendo que estamos dentro de `primera_carpeta`:

```
cp prueba.txt prueba_copia.txt
```

Si lista todos los archivos de `primera_carpeta`, verá tres archivos de texto.

¿Y si quieres copiar un directorio entero? Prueba a subir un directorio desde `primera_carpeta`, y luego escribe `cp primera_carpeta primera_carpeta_copia`. Y, ¡oh! Debería ver un error: `cp: questions_copy es un directorio (no copiado).`

Para copiar un directorio, necesitas modificar el comando `cp` de la siguiente manera:

```
cp -r primera_carpeta primera_carpeta_copia
```

La `-r` se llama _bandera_; puedes pensar en una bandera para un comando como una opción que se puede pasar a ese comando. Para saber más sobre las opciones que puedes pasar a `cp`, puedes escribir `man cp` (`man` es la abreviatura de manual, en Windows este comando es `--help`) y usar las flechas para moverte arriba y abajo. Cuando hayas terminado, pulsa `q` para salir.

#### Borrar archivos y carpetas

Muy bien, ya basta con todos estos archivos y carpetas, vamos a deshacernos de ellos. Asegúrate de que estás dentro de la `primera_carpeta` y escribe `rm prueba.txt`. Una vez más, no deberías ver mucha respuesta de la terminal, así que ejecuta un rápido `ls` para asegurarte de que el archivo ha sido eliminado. Ahora que ya no está... ¿dónde ha ido? ¿A la papelera? La respuesta es que ha sido completamente eliminado de tu ordenador. No hay confirmación ni deshacer, así que ten MUCHO cuidado cuando uses el comando `rm`. Después de eliminar este archivo, elimine también el archivo copiado. Por último, elimine "primer_archivo". Ahora que la carpeta `first_folder` está vacía, subamos un directorio y eliminemos la carpeta `first_folder`.

Aquí puedes encontrarte con un problema. Si intentas usar `rm` en un directorio, verás este mensaje: `rm: primera_carpeta: es un directorio`. Resulta que `rm` es para un fichero, mientras que el comando `rmdir` se usa para eliminar directorios (vacíos). Así que vamos a utilizar el comando `rmdir` para eliminar `primera_carpeta`. Asegúrate de que no hay nada más dentro de esa carpeta, o de lo contrario verás un mensaje parecido a este: `rmdir: primera_carpeta: Directorio no vacío`.

Si hay algo dentro de la carpeta, tendrás que usar `rm -rf primera_carpeta`. Como vimos con `cp`, `r` y `f` en `-rf` son ejemplos de banderas. ¿Cómo puedes saber más sobre las banderas de `rm`? Sigue adelante y elimina el directorio `first_folder_copy` usando `rm -rf`.

**Ejercicios

1. Crea un fichero llamado `nombre.txt`.
2. Intenta renombrar el fichero a `renombrar.txt` utilizando el comando `mv`. ¿Qué te dice esto sobre el comando?
3. Utilizando el comando `cp`, haz una copia de `renombrar.txt` y llámala `copiar.txt`.
4. 4. Elimina el fichero `copiar.txt`.
5. Crea una carpeta llamada `preguntas`.
6. Cambia de directorio a la carpeta `questions`.
7. Crea un fichero llamado `primero.txt`.
8. Crea un fichero llamado `segundo.txt`.
9. Retrocede un directorio y haz una copia de la carpeta de preguntas y llámala `copia_preguntas`.
10. 10. Cuando usas `cp -r` ¿cómo se llama la `-r`? ¿Qué hace?
11. Borra la carpeta original `questions` y la copia.



### { Listado de Archivos y Banderas. }

#### Objetivos

Al final de este capítulo, deberías ser capaz de:

* Entender lo que hace el comando `ls
* Definir flags y describir cómo funciona la sintaxis
* Listar archivos usando flags

#### Listado de archivos

Como has visto en el capítulo anterior, uno de los comandos más importantes que vas a utilizar es `ls`, que lista el contenido de un directorio. Si escribes `ls` en un directorio verás todo tipo de contenido. Por ejemplo, si escribes `ls` en tu directorio personal verás todos los archivos y carpetas que hay dentro de ese directorio. Normalmente, tu directorio personal contiene carpetas como `Desktop`, `Documents`, `Downloads`, `Music`, `Pictures`, etc.

A veces el comando por defecto `ls` no nos da toda la información que queremos. En esos casos, necesitaremos añadir algunas banderas para obtener más detalles.

#### Banderas

En el capítulo anterior, vimos cómo se podían utilizar las banderas para modificar el comportamiento de `cp` y `rm`. Los flags pueden cambiar e incluso mejorar los comandos y se añaden usando un `-` después del comando. Los flags se representan normalmente con letras mayúsculas y minúsculas. Con el comando `ls`, podemos pasar la bandera `-a` para listar "todos" los archivos (incluyendo los archivos y carpetas ocultos). Si queremos que el comando `ls` nos proporcione más información sobre cada archivo, podemos introducir el indicador `-l`. Para combinar banderas podemos usar una `-` y pasar cada bandera. Así que el comando para usar `ls` y mostrar todos los archivos e información más detallada sobre cada uno sería `ls -la`.

Usar banderas para `ls` será esencial cuando trabajes con permisos así como cuando empieces a trabajar con `git`. También veremos muchos otros comandos de terminal que aceptan flags más adelante en este curso.



## { Ejercicios Básicos de Terminal. }

Escribe los siguientes comandos de terminal para realizar las siguientes tareas:

#### Parte I

1. crea un directorio llamado "first
2. cambia el directorio a la carpeta `first
3. crea un fichero llamado `persona.txt`.
4. Cambia el nombre de `persona.txt` a `otro.txt`.
5. Haga una copia del fichero `otro.txt` y llámela `copia.txt`.
6. elimine el archivo "copia.txt
7. Haga una copia de la carpeta "first" y llámela "second".
8. elimine la carpeta "second

#### Parte II

1. ¿Qué hace el comando `man`? Escribe `man rm`. ¿Cómo se desplaza y sale?
2. Mira la página `man` para `ls`. ¿Qué hace la bandera `-l`? ¿Qué hace la bandera `-a`?
3. Escribe el siguiente comando para descargar y guardar el contenido de google.com: `curl https://www.google.com > google.html`
4. Utiliza `less` para ver el contenido de `google.html`.
5. 5. Mira la página `man` de less. 6. Lee la sección sobre `/pattern`. Busca el texto **hplogo** en el fichero `google.html`.
6. Cómo se salta entre palabras en el terminal?
7. ¿Cómo se llega al final de una línea en el terminal?
8. Cómo se desplaza el cursor al principio en terminal?
9. ¿Cómo se borra una palabra (sin pulsar varias veces retroceso) en terminal?
10. ¿Cuál es la diferencia entre terminal y shell?
11. 11. ¿Qué es una ruta absoluta?
12. 12. ¿Qué es una ruta relativa?
13. 13. ¿Qué es una bandera? Pon tres ejemplos de banderas que hayas utilizado.
14. 14. ¿Qué hacen las banderas `r` y `f` con el comando `rm`?





## Nivel Intermedio



### { Permisos y Enlaces. }

#### Objetivos

Al final de este capítulo, usted debe ser capaz de:

* Determinar los permisos establecidos para un archivo o directorio.
* Gestionar y cambiar permisos usando `chmod`.
* Gestionar y cambiar usuarios y grupos usando `chown` y `chgrp`.
* Explicar qué es `root` y la relación entre `root` y `sudo`.
* Crear enlaces en el sistema de ficheros utilizando el comando `ln`.
* Explicar la diferencia entre un enlace duro y un enlace simbólico

#### Introducción

Cuando estás trabajando en Terminal, a veces puedes encontrar que no se te permite hacer cosas que quieres hacer. Tal vez estás tratando de instalar algo, o mover un archivo de un directorio a otro, y recibes un error que te dice algo parecido a "permiso denegado". Este tipo de errores de permisos son extremadamente comunes, por lo que es importante entender cómo lidiar con ellos. Eso es lo que aprenderemos a hacer en este capítulo.

#### Usuarios y Grupos

Antes de aprender acerca de los permisos, primero necesitas entender a los usuarios y grupos. Veamos un ejemplo. Dirígete a tu directorio personal y lista todo usando el comando `ls -lah`. (¿No estás seguro de lo que hace la bandera `h`? ¡Consulta el manual!)

La salida que obtienes puede ser algo como esto:

![](<.contenido/imagen (151).png>)

Los detalles de estos archivos no son importantes. Lo que debería ver es un montón de filas de salida, una fila por cada archivo o directorio. Veamos qué significa todo esto. Por ejemplo, aquí está la línea para el archivo `.bashrc` de la captura de pantalla anterior:

`-rwxr-xr-x 1 eschoppik staff 67B Ago 29 2014 .bashrc`

La tercera columna especifica el nombre de usuario al que pertenece el archivo. En este caso, `eschoppik` es el propietario del archivo. La cuarta columna especifica el nombre del grupo asociado con el archivo. En este caso el grupo `staff` está asociado al fichero.

En la mayoría de los sistemas Mac, los usuarios también son miembros del grupo `staff`. Para ver a qué grupos pertenece, escriba el comando `groups` en Terminal. El grupo `staff` será probablemente uno de los muchos grupos a los que perteneces. Como veremos a continuación, los permisos se pueden establecer para el propietario del archivo, un usuario que está en un grupo asociado con el archivo, o un usuario que no es ni el propietario ni un miembro del grupo asociado.

#### Permisos

Echemos un vistazo a esa línea `.bashrc` de nuevo:

`-rwxr-xr-x 1 eschoppik staff 67B Ago 29 2014 .bashrc`

Ya hemos hablado de la tercera y cuarta columnas de esta salida. Ahora hablemos de la primera columna. El `-rwxr-xr-x` se refiere a los _permisos_ del archivo `.bashrc`. Cada caracter de la cadena de permisos, `-rwxr-xr-x` describe algo sobre los permisos del archivo. Pero, ¿qué son los permisos? Los permisos de un archivo son un conjunto de reglas que describen qué operaciones puede o no puede realizar un usuario en un archivo o carpeta. Hay 3 tipos de operaciones que se pueden permitir o no:

* `r` - leer el fichero
* w` - escribir en el fichero
* `x` - ejecutar el fichero (entraremos en esto con más detalle próximamente)

En este punto te estarás preguntando, ¿por qué la cadena de permisos es tan larga si sólo hay 3 operaciones que se pueden especificar? Bueno, una cadena de permisos describe diferentes tipos de usuarios que pueden o no realizar operaciones de lectura, escritura y ejecución. Usted puede ser uno de 3 tipos diferentes de usuarios:

1. 1. El propietario del fichero.
2. No propietario, pero miembro de un grupo asociado al fichero.
3. 3. Otro. No es propietario y no pertenece a un grupo asociado al fichero.

Así que una cadena de permisos especifica los permisos para los 3 tipos de usuarios más un carácter extra para especificar el tipo (archivo, carpeta, etc).

Así es como se descompone la cadena de permisos anterior:

![](<.contenido/imagen (185).png>)

En otras palabras, esta cadena dice que `.bashrc` es un archivo, que el propietario del archivo puede leer, escribir y ejecutar, los usuarios del grupo sólo pueden leer y ejecutar, y otros usuarios sólo pueden leer y ejecutar también.

#### Cambio de permisos

Para cambiar los permisos de un fichero utilizamos el comando `chmod`. Para cada conjunto de permisos (propietario, grupo, todos) podemos asignar un número del 0 al 7. Esto se llama **octal**. Esto se llama notación **octal** (base-8). Aquí hay una tabla que ilustra lo que significa cada número.

| Número Permiso `rwx` (mostrar en terminal)
| ------ | ----------------------- | --------------------------- |
| 0 Ninguno
| 1. Ejecutar.
| 2. Sólo escritura.
| 3. Escribir y ejecutar.
| 4. Sólo lectura.
| 5. Lectura y ejecución.
| 6. Lectura y escritura.
| 7. Lectura, escritura y ejecución.

Así que si queremos cambiar un fichero para que sólo el propietario y el grupo puedan leer, escribir y ejecutar, escribiríamos `chmod 770 algunfichero.txt`.

Si quieres ser un poco más específico, también puedes establecer permisos usando lo que se llama **notación simbólica**. Aquí tienes un ejemplo:

```
chmod ug+rwx,o-rwx hi.txt
```

Esto está diciendo "añade permisos de lectura, escritura y ejecución al **u**ser y al **g**roup, y quita permisos de lectura, escritura y ejecución a **o**ther". Aunque es un poco más verboso, también es un poco más descriptivo. Para ver más ejemplos de notación simbólica, consulta [este](https://askubuntu.com/questions/518259/understanding-chmod-symbolic-notation-and-use-of-octal) artículo.

Si queremos cambiar los permisos de una carpeta, tenemos que añadir la bandera `-R`: `chmod -R 755 alguna_carpeta`.

Puedes leer más sobre `chmod` [aquí](https://en.wikipedia.org/wiki/Chmod).

#### Archivos ejecutables y carpetas

Ahora hablemos un poco más sobre lo que la `x` (ejecutable) significa para los permisos de un archivo o una carpeta. Si tienes permisos de ejecutable en una carpeta, significa que puedes entrar en ella. Mira lo que pasa con los siguientes comandos:

```
mkdir carpeta_prueba
cd carpeta_prueba
cd ..
chmod 666 carpeta_prueba
cd carpeta_prueba
```

Deberías ver un error diciendo permiso denegado. Vuelva a añadir el permiso de ejecución a la carpeta y, a continuación, elimínela.

Ahora pasemos a los archivos ejecutables. Cuando un archivo es ejecutable, puede ser ejecutado desde tu shell como si fuera un programa. Primero creemos nuestro archivo. Escribe lo siguiente en tu terminal:

```
echo ls > prueba.sh
echo pwd >> prueba.sh
echo pushd . >> prueba.sh
echo "cd ~" >> prueba.sh
echo "pwd" >> prueba.sh
echo popd >> prueba.sh
cat prueba.sh
```

El fichero `test.sh` debería tener ahora el siguiente aspecto:

```
ls
pwd
pushd .
cd ~
pwd
popd
```

(¿Te has dado cuenta de que nuestro primer comando `echo` utiliza una sola flecha (`>`), mientras que los otros comandos utilizan dos? Exploraremos la diferencia entre estos dos operadores en el próximo capítulo).

Ahora hagamos ejecutable el archivo y ejecutémoslo. Usa chmod para hacerlo ejecutable: `chmod 755 prueba.sh`. A continuación, ejecuta el archivo proporcionando una ruta al archivo. En nuestro caso, el archivo está en el directorio actual, así que para ejecutarlo, hacemos lo siguiente: `./test.sh`. ¡Acabamos de crear nuestro primer script de shell ejecutable!

#### chown y chgrp

Ahora que tenemos una comprensión más clara de los usuarios, grupos y permisos, vamos a echar un vistazo a la línea de `ls -lah` de nuevo:

`-rwxr-xr-x 1 eschoppik staff 67B Ago 29 2014 .bashrc`

* El `1` se refiere al número de archivos (siempre será 1 para los archivos)
* `eschoppik` es el "propietario".
* `staff` es el grupo
* `67B` es el tamaño del fichero
* `Aug 29 2014` es el último día que se modificó el fichero
* `.bashrc` es el nombre del fichero

¿Y si ya no queremos que `eschoppik` sea el propietario del archivo? ¿O si queremos que otro grupo sea el propietario del fichero? Podemos usar uno de los siguientes comandos:

`chown otrousuario:otrogrupo .bashrc`

O si sólo queremos cambiar el grupo

`chgrp otrogrupo .zshrc`.

Ahora echemos un vistazo a esta línea del comando `ls -lah`:

`drwxr-xr-x 6 root admin 204B Oct 20 2015 ..`

El otro archivo decía `eschoppik` para usuario y `staff` para grupo, pero este dice `root` y `admin`. También podemos ver que se trata de un directorio, ya que comienza con una "d" antes de enumerar los permisos. Entonces, ¿cuál es el usuario `root`?

#### usuario root y sudo

El usuario `root` es un usuario especial en tu ordenador que tiene el poder de hacer lo que quiera. Puede cambiar los permisos de cualquier archivo, borrar lo que quiera, etc. Cuando veas que `root` es el propietario, y quieras hacer un cambio en ese archivo, tienes que usar un comando llamado `sudo`. El comando `sudo` te da los poderes del usuario `root` para un solo comando y te pedirá tu contraseña para poder preformar el comando. Prueba comandos con sudo. Crea un archivo llamado `somefile.txt`. Luego haz que el propietario sea el usuario root:

`sudo chown root algúnarchivo.txt`.

Ahora intenta borrar el archivo sin usar sudo. No está permitido. Mira los permisos. ¿Por qué no está permitido?

#### Enlaces

Dado que tenemos archivos y carpetas ubicados por todo nuestro sistema de archivos, resulta difícil identificar dónde se encuentran muchos de ellos. Afortunadamente, podemos crear un enlace (también conocido como alias) a un archivo o carpeta utilizando el comando `ln`. La estructura es la siguiente:

`ln ruta_al_enlace nombre_del_enlace`.

Hay dos tipos de enlaces que podemos hacer, enlaces duros y simbólicos - ¡vamos a ver cómo funcionan!

#### Enlaces duros

Vamos a crear un archivo llamado `aprender.txt` en nuestra carpeta `Desktop` (teclea `cd /Usuarios/$USUARIO/Desktop` si necesitas llegar allí). Podemos abrir nuestro archivo `learn.txt` usando `open learn.txt` y vamos a añadir el texto "¡Aprendiendo sobre enlaces!".

Ahora vamos a crear un enlace a este archivo. Podemos llamar a nuestro enlace `primer_enlace`. Para ello usamos el comando `ln` y escribimos `ln aprender.txt primer_enlace`. Ahora si `cat primer_enlace` deberíamos ver la salida "¡Aprendiendo sobre enlaces!".

Si decidimos mover nuestro fichero `aprender.txt` a cualquier sitio, ¡seguiremos teniendo un enlace a él a través de `primer_enlace`! ¡Impresionante!

Si decidimos borrar nuestro fichero `learn.txt`, ¿qué pasa con nuestro enlace duro? Vamos a `rm learn.txt` y luego `cat first_link`. ¡Todavía vemos que tenemos un enlace! Esto puede parecer extraño; ¿no debería romperse un enlace si se elimina un archivo? Con los enlaces duros, ¡no! Un enlace duro es como una copia directa de un fichero. Si se elimina el archivo, el enlace sigue existiendo.

#### Enlaces simbólicos

Vimos que cuando eliminamos el archivo original, los enlaces duros siguen existiendo y contienen todo el archivo fuente. Esto normalmente no es lo que queremos, ya que normalmente queremos una referencia a algún archivo y no una copia directa. Para crear una referencia en lugar de una copia, hagamos un enlace simbólico.

Para crear un enlace simbólico, usamos la bandera `-s` cuando creamos un enlace. Creemos un nuevo fichero llamado `aprender_otra vez.txt` y luego creemos un enlace simbólico usando `ln -s aprender_otra vez.txt primer_enlace_simbolico`. Si `cat first_sym_link` no obtenemos ningún error. Pero si borramos o movemos `aprender_otra vez.txt`, ¡nuestro `first_sym_link` se romperá!

También podemos utilizar enlaces simbólicos para carpetas, lo que resulta muy útil si necesitamos acceder a una carpeta pero no recordamos la ruta. Sin embargo, si la ruta original del archivo/carpeta cambia o se elimina, el enlace simbólico **se romperá**.



### { Redirección. }

#### Objetivos

Al final de este capítulo, usted debe ser capaz de:

* Explicar qué es la redirección
* Explicar la diferencia entre `>`, `>>` y `<`.
* Utilizar la redirección para trabajar más eficazmente en Terminal

#### Redirección

A veces, en lugar de simplemente mostrar la salida de un comando en la terminal, es útil tomar la salida resultante de un comando y enviarla a otro lugar. A esto lo llamamos "redirección" y se denota con `>>` o `>`. Empecemos con un ejemplo simple usando el comando `echo`.

El comando `echo` es útil para mostrar texto en la terminal, pero muchas veces es más útil tomar ese texto y redirigirlo a un archivo. En Terminal, escriba el comando `echo Hola Mundo > hola.txt`. Luego, usando el comando `cat`, veamos lo que acabamos de hacer escribiendo `cat hola.txt`. Todo lo que hicimos aquí es tomar el texto "Hola Mundo" y en lugar de mostrarlo en la terminal, ¡lo enviamos a un archivo llamado `hola.txt`!

Ejecute el mismo comando de nuevo pero con un texto ligeramente diferente: `echo Hola Universo > hola.txt`. Ahora vuelve a ver el fichero. Observa que tu nuevo texto ha sobrescrito completamente el antiguo: deberías ver que "Hola Mundo" ha sido reemplazado por "Hola Universo". En otras palabras, cuando usas `>`, el texto que estás introduciendo en el fichero sobrescribirá completamente cualquier texto que ya estuviera en el fichero.

Tal vez esto es lo que quieres, pero tal vez no. ¿Y si lo que quieres es añadir texto al final del fichero, en lugar de sobrescribirlo? En este caso, utilice `>>` en su lugar. Pruébalo: `echo Hola Mundo >> hola.txt`. Ahora abre el fichero. Deberías ver lo siguiente:

```
Hola Universo
Hola Mundo
```

Un caso de uso muy común para la redirección es poner pequeños trozos de texto en un archivo. En lugar de abrir un editor de texto, escribir algo de texto, guardarlo y cerrar el archivo, podemos hacerlo todo en un solo paso.

#### Redirección con Input

Hasta ahora hemos visto la redirección usando `>` y `>>`. Estas flechas indican redirección con salida estándar (tomar algo y enviarlo a otra cosa). Sin embargo, también podemos utilizar la redirección con la entrada utilizando la flecha `<`. Usemos un comando llamado `sort`, que ordena un fichero alfabéticamente. Imaginemos que tenemos un fichero llamado `nombres.txt` con los siguientes nombres:

```
Bob
Tom
Jim
Amy
```

Si queremos ordenar este fichero, podemos teclear `ordenar nombres.txt` y saldrá

```
Amy
Bob
Jim
Tom
```

¿Y si queremos tomar el contenido de `names.txt`, redirigirlo al comando `sorted`, y luego enviar _esa_ salida a un fichero llamado `sorted.txt`? La redirección se vería así: `clasificar < nombres.txt >clasificado.txt`. Esto creará un nuevo fichero llamado `ordenado.txt` con los nombres ordenados alfabéticamente.

Esto puede parecer un poco extraño, pero pruebe a escribir estos comandos y vea qué información puede obtener y redirigir. Como vemos ahora mismo, sólo estamos usando el comando `sort`, pero ¿qué pasaría si quisiéramos usar otros comandos junto con sort? De alguna manera necesitaríamos conectar cada uno de estos comandos. Conectamos estos comandos entre sí a través de algo llamado "pipes".



### { Piping. }

#### Objetivos

Al final de este capítulo, usted debe ser capaz de:

* Explicar qué hacen los comandos `head`, `tail`, `sort`, `uniq`, `wc` y `grep
* Definir qué es la canalización
* Entender los casos de uso de piping
* Usar piping para trabajar mejor en Terminal

#### Canalización

Al final del último capítulo, vimos cómo podíamos usar la redirección para combinar un par de comandos en uno. En ese caso, en una sola línea pudimos ordenar un archivo de texto y enviar su contenido a un nuevo archivo.

Pero, ¿y si queremos encadenar aún más comandos? Aquí es donde entra en juego el piping. Antes de aprender sobre piping, sin embargo, vamos a aprender/revisar un par de otros comandos de terminal.

`head` - muestra las primeras líneas de un fichero (usando la bandera `-n` podemos especificar el número de líneas)

`tail` - muestra las últimas líneas de un fichero (usando la bandera `-n` podemos especificar el número de líneas)

`sort` - ordena las líneas de un fichero de texto

`uniq` - elimina las líneas duplicadas (sus datos **deben** estar ordenados para que esto funcione)

`wc` - cuenta palabras, líneas, caracteres y bytes

Ahora vamos a crear dos archivos - `first.txt` que contiene el texto

```
Primer
Segundo
Tercero
```

Y `second.txt` que contiene:

```
Cuarto
Quinto
Sexto
```

Si queremos concatenar (unir) estos dos archivos, utilizamos el comando `cat`:

`cat primer.txt segundo.txt` (asegúrate de que los archivos y los comandos están separados por un espacio).

Pero, ¿qué pasa si queremos concatenar estos dos archivos y luego encontrar el recuento de palabras? ¿Y si queremos concatenarlos y luego ordenarlos? Aquí es donde necesitamos una tubería. Puedes pensar en una tubería como una conexión entre la salida de un comando y la entrada de otro comando. Así, una vez concatenados dos archivos, queremos enviar (o canalizar) el resultado a otro comando. Incluso podemos combinar esto con la redirección.

Para canalizar un comando utilizamos el carácter `|`. Así que si queremos pasar `cat` a `sort` se vería así:

`cat first.txt second.txt | sort` o `cat first.txt second.txt | sort | head -n 2`.

Echa un vistazo a este comando e intenta averiguar qué está haciendo. Encontrarás una respuesta paso a paso más abajo.

`cat primer.txt segundo.txt | ordenar | tail -n 3 | head -n 1`

1. Concatenar los dos archivos first.txt y second.txt
2. Ordenar los resultados
3. Buscar las 3 últimas líneas
4. Busca la primera línea de esas 3 últimas líneas

Así es como podemos encontrar la antepenúltima línea de un fichero (sin saber cuántas líneas tiene el fichero).

#### `grep

Examinemos otro comando útil llamado `grep` que es extremadamente poderoso para encontrar texto. Por sí solo es útil, pero es bastante útil cuando se combina con `cat`. Intentemos un ejemplo simple con `cat primer.txt | grep Primer` - ¿qué ves?

Deberías ver la palabra `First` en el terminal. Esto se debe a que `grep` ha buscado en el fichero el texto `Primero` y ha encontrado una coincidencia.

Observa que si `grep` no encuentra ninguna coincidencia, no mostrará nada. Si encuentra varias coincidencias, las imprimirá todas. Prueba estos comandos y mira lo que te devuelve `grep`.

```
cat primero.txt segundo.txt | grep Nope
cat primero.txt segundo.txt | grep th
```

Veamos otro ejemplo. Imagina que tienes un fichero llamado `nombresdeperros.txt`, y dentro tienes la siguiente lista de nombres:

```
Lassie
Moxie
Whiskey
Fido
Lassie
Moxie
```

Vemos aquí que hay bastantes duplicados, así que vamos a intentar usar el comando `uniq` para eliminar estos nombres duplicados. El problema es que cuando ejecutamos `uniq petnames.txt` obtenemos lo siguiente

```
Lassie
Moxie
Whiskey
Fido
Lassie
Moxie
```

Si volvemos a nuestra definición de cómo funciona el comando `uniq`, veremos que nuestros datos deben estar ordenados. Entonces, ¿cómo podemos usar primero `sort` en `petnames.txt` y luego adjuntar el comando `uniq`? ¡Piping al rescate!

El comando `sort petnames.txt | uniq` nos da

```
Fido
Lassie
Moxie
Whiskey
```

Tiene una pinta estupenda. Pero este texto sólo se está mostrando en el terminal, ¿qué pasa si queremos mostrar este texto en un nuevo archivo llamado `nombres_de_mascota_clasificados.txt`? Podemos combinar piping con redirección y usar `sort petnames.txt | uniq > petnames_sorted.txt`. Ahora si `cat nombres_mascota_clasificados.txt` deberíamos ver nuestros cuatro nombres únicos clasificados.



## { Ejercicio de Permisos, Redirección y Canalización. }

#### Parte I (Permisos y enlaces)

Escribe comandos de terminal para hacer lo siguiente:

1. Crear un archivo llamado `restricted.txt`.
2. 2. Cambia los permisos del fichero `restricted.txt` para permitir al propietario leer y escribir en el fichero `restricted.txt`. Hazlo utilizando la Notación **Octal**.
3. 3. Cambia los permisos del archivo `restricted.txt` para que sólo el propietario, el grupo y todos puedan leer, escribir y ejecutar el archivo `restricted.txt`. Hazlo utilizando la notación **Simbólica**.
4. Crea una carpeta llamada `archivos_secretos`. Dentro de la carpeta `secret_files` crea un fichero llamado `first_secret.txt` y otra carpeta llamada `classified`. Dentro de la carpeta `classified` crea un fichero llamado `super_secret.txt`.
5. 5. Cambia los permisos de los archivos secretos para que sólo el propietario y el grupo puedan leer, escribir y ejecutar en todos los archivos y carpetas dentro de los archivos secretos. Hazlo utilizando la Notación Octal.
6. Crea un enlace duro para el `restricted.txt` llamado `hard_link`.
7. 7. Crea un enlace simbólico para la carpeta `classified` llamado `classified_link`.

#### Parte II (Canalización y Redirección)

Para los siguientes ejercicios, crea un archivo de texto llamado `vegetables.txt` con el siguiente texto:

```
Lechuga
Amaranto
Remolacha
Apio
Col rizada
Eneldo
Col
Brécol
Lechuga
Amaranto
Remolacha
Espinacas
Acelga
Brécol
Col
Eneldo
```

Escribe los siguientes comandos de terminal para hacer lo siguiente

1. Ordenar `vegetables.txt`.
2. Contar el número de líneas en `vegetables.txt`.
3. Cree un archivo llamado `verduras_ordenadas.txt` que contenga todas las verduras únicas ordenadas de forma ascendente en verduras.txt (hágalo sin el comando touch).
4. Cree un archivo llamado `últimas_tres.txt` que contenga las tres últimas verduras del archivo `verduras.txt` (haga esto sin el comando `tocar`).
5. 5. Cuente el número de líneas en las que aparece la palabra "Brócoli" (usando `wc` y `grep`).





## Herramientas de desarrollo

#### Visual Studio Code

Visual Studio Code o VS Code es un IDE. IDE significa Entorno de Desarrollo Integrado. Es el software que utilizarás para escribir la mayor parte de tu código. Está diseñado para ayudarte a desarrollar tus aplicaciones rápidamente, centrándose en los problemas que necesitas resolver en lugar de tener que buscar en Internet detalles menores.

**Autocompletar

Una de las características más importantes de un IDE es que proporciona _autocompletado_. Esto significa que te dará sugerencias de lo que puedes escribir a continuación, mientras estás escribiendo algo.

Por ejemplo, al escribir una propiedad CSS, VSC te dirá qué valores puedes asignar a esta propiedad.

![](<.contenido/imagen (166).png>)

**Vista de árbol de archivos**

La razón por la que llamamos a un IDE _integrado_ es que casi no necesitas salir de la ventana cuando estás escribiendo tu código. Por ejemplo, crear, renombrar y mover archivos se puede hacer directamente desde el IDE. Esta funcionalidad se puede conseguir desde algo llamado **vista de árbol**. Puedes encontrar esta vista en la parte izquierda de tu IDE.

![](<.contenido/imagen (177).png>)

**Buscar archivos**

Cuando trabajes con proyectos grandes, a menudo necesitarás encontrar un archivo rápidamente, sin tener que recorrer la vista de árbol manualmente.

![](<.contenido/imagen (198).png>)

**Activar formato al guardar**

Para dar automáticamente a tu código el formato adecuado:

* En Visual Studio, abra el archivo de configuración (consulte [https://code.visualstudio.com/docs/getstarted/settings#_creating-user-and-workspace-settings](https://code.visualstudio.com/docs/getstarted/settings#_creating-user-and-workspace-settings)).
* Busque `editor format`.
* Establecer `editor.formatOnSave` y `editor.formatOnPaste` a `true`.

### { OPTIONAL } Extensiones de código de Visual Studio para desarrollo web

Visual studio code ofrece una amplia gama de extensiones. Aquí se explica cómo instalar la extensión.

Pulse **SHIFT+COMMAND (o Windows)+X** o simplemente haga clic en el icono de extensión de visual studio code. Busca la extensión y pulsa instalar

![](<.contenido/imagen (88).png>)

Aquí hay algunas extensiones de visual studio code para el desarrollo web. La elección de la extensión es una opinión personal.

#### 1: Fragmentos de código Javascript (ES6)

No es necesario mencionar que JavaScript es el núcleo del desarrollo web. Hay un montón de fragmentos de código que utilizamos a diario y esta extensión le ayuda a no escribir ese código repetitivo una y otra vez.

Proporciona JavaScript, TypeScript, Vue, React, y fragmentos de código HTML. Esta es una extensión imprescindible para el desarrollo web.

Enlace: [https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets)

Puedes instalarla buscando el nombre en la sección de extensiones del código de visual studio.

#### 2: CSS Peek

Como su nombre indica, esta extensión te permite saltar al código CSS usando clases e IDs.

Enlace: [https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek)

Puedes instalarla buscando el nombre en la sección de extensiones del código de visual studio.

#### 3: Etiqueta de cierre automático

Esta extensión añade automáticamente la etiqueta de cierre de HTML y XML.

Enlace:[ https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)

Puedes instalarla buscando el nombre en la sección de extensiones del código de visual studio.

#### 4: ESLint

ESLint es la utilidad de linting para JavaScript. Comprueba tu código en busca de errores comunes y te lo hace saber en el propio editor. Es como un compañero virtual que valida tu código mientras lo escribes.

Enlace:[ https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

Puedes instalarlo buscando el nombre en la sección de extensiones del código de visual studio.

Antes de instalar ESLint en visual studio, instálalo primero como paquete global. `npm install -g eslint`.

#### 5: Prettier - Formateador de código

Esta extensión realiza el formateo del código JavaScript, CSS y HTML.

Enlace: [https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

Puedes instalarla buscando el nombre en la sección de extensiones del código de visual studio.

#### 6: Intellisense de ruta

Importar código de otros archivos es lo que todo el mundo hace a diario. Esta extensión agiliza el tiempo de desarrollo autocompletando los nombres de los archivos.

Escribes el nombre del archivo en las sentencias y te buscará y dará sugerencias.

Enlace: [https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

Puedes instalarlo buscando el nombre en la sección de extensiones del código de visual studio.

#### 7: GitLens

Usamos Git casi todos los días de nuestra vida. GitLens es el plugin de visual studio code para potenciar las capacidades de git.

Con GitLens, es muy fácil ver la autoría del código, comprobar el número de commit, ver los cambios entre el último commit y los cambios existentes, etc.

Enlace: [https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)\
Puedes instalarlo buscando el nombre en la sección de extensiones del código de visual studio.

#### 8: Gestor de proyectos

¿Trabajas en varios proyectos y cambias de uno a otro? Sé que lo hago y el gestor de proyectos ha sido un salvador para gestionar múltiples proyectos en visual studio code

Enlace: [https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)

Puedes instalarlo buscando el nombre en la sección de extensiones de visual studio code.

#### 9: Servidor Live

La extensión Live Server proporciona una vista previa en vivo de tu aplicación web directamente desde el editor.

Esto es muy práctico y útil para los desarrolladores front-end.

Enlace:[ https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)\
Puedes instalarla buscando el nombre en la sección de extensiones del código de Visual Studio.

#### 10: Depurador para Chrome

Esta extensión trae el potente depurador de Chrome directamente al código de Visual Studio.

Es muy útil para los desarrolladores front-end para realizar las pruebas y depuración.

Enlace: [https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)\
Puedes instalarlo buscando el nombre en la sección de extensiones del código de visual studio.

#### 11: Mejores comentarios

Esta extensión te ayuda a crear comentarios más amigables y fáciles de leer.

Enlace: [https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)\
Puedes instalarla buscando el nombre en la sección de extensiones del código de visual studio.

#### 12: Tiempo de código

Esta extensión realiza un seguimiento de tu tiempo de desarrollo y te proporciona estadísticas útiles como cuántas horas has codificado hoy, etc.

Es bastante útil para hacer un seguimiento y ver el progreso. Esto no es estrictamente para el desarrollo web sólo, cualquiera puede utilizar esta extensión.

Enlace: [https://marketplace.visualstudio.com/items?itemName=softwaredotcom.swdc-vscode](https://marketplace.visualstudio.com/items?itemName=softwaredotcom.swdc-vscode)\
Puedes instalarla buscando el nombre en la sección de extensiones del código de visual studio.

#### 13: Sincronización de ajustes

Uso una máquina diferente para mi trabajo y para uso personal. Uso visual studio code en ambas máquinas, sin embargo, no quiero repetir los mismos pasos para configurar el editor cada vez.

Entra en la extensión Setting Sync. Crea y almacena tu configuración en Github gist y sincroniza donde quieras. ¡Simple e impresionante!

Enlace: [https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)\
Puedes instalarlo buscando el nombre en la sección de extensiones del código de visual studio.



## **Más Recursos**

* [Tutorial: ¡Terminal para principiantes!](https://medium.com/@grace.m.nolan/terminal-for-beginners-e492ba10902a)
* [Tutorial de comandos básicos 10 mins](https://youtu.be/vhZLTp6N4XA)
* [Introducción a Ubuntu y tutorial de comandos útiles 45 mins](https://youtu.be/KSh9-6FIu1w)



No pasa nada si te quedas atascado o si algo no te parece correcto. Cuando eso ocurra, por favor pide ayuda a tus profesores o compañeros en Slack, o utiliza el canal **#support-coding**.







{% hint style="info" %}
**Todo lo que sigue es opcional y no es un requisito de nuestro curso. Los estudiantes a los que les guste desafiarse a sí mismos pueden continuar con el Nivel Avanzado.**
{% endhint %}

## Nivel Avanzado - 1 { OPTIONAL }

### { Entorno Terminal. }

#### Objetivos:

Al final de este capítulo, usted debe ser capaz de:

* Describir qué es un entorno de terminal
* Crear y modificar variables de entorno de terminal, incluyendo el `PATH
* Guardar variables de entorno en un fichero de configuración

#### ¿Cuál es el entorno de su terminal?

El entorno de un terminal es una lista de configuraciones que pueden ser referenciadas por los programas. Para ver cómo es el entorno de tu terminal en este momento, intenta escribir `env` en tu terminal. Debería ver una salida similar a la siguiente:

```
rvm_bin_path=/Usuarios/tim/.rvm/bin
TERM_PROGRAM=Apple_Terminal
GEM_HOME=/Usuarios/tim/.rvm/gems/ruby-2.3.1
TERM=xterm-256color
SHELL=/bin/bash
CLICOLOR=1
IRBRC=/Usuarios/tim/.rvm/rubies/ruby-2.3.1/.irbrc
TMPDIR=/var/carpetas/5s/zstwqxy52pl_lq_lr3b5v7nc0000gn/T/
Apple_PubSub_Socket_Render=/private/tmp/com.apple.launchd.Q7TcyOvK4P/Render
TERM_PROGRAM_VERSION=361.1
OLDPWD=/Usuarios/tim
TERM_SESSION_ID=281162A1-5C58-4285-9A35-AC9306923C34
USUARIO=tim
__CF_USER_TEXT_ENCODING=0x1F5:0x0:0x0
LSCOLORS=GxFxCxDxBxegedabagaced
PATH=/usr/local/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Users/tim/.rvm/bin
PWD=/Usuarios/tim/Proyectos/Rithm/prework
.
.
.

```

Cada palabra a la izquierda del signo igual se denomina **variable de entorno**. El valor a la derecha es el valor de la variable.

#### Uso de variables de entorno

En el terminal, puedes ver qué valor tiene una variable de entorno utilizando `echo`. Cuando hagas referencia a una variable de entorno, debes utilizar `$` como prefijo. En otras palabras, para imprimir el valor de la variable de entorno `PWD`, el comando sería:

```
echo $PWD
```

Prueba esto en tu terminal. Deberías obtener la misma salida que con el comando `pwd`.

#### Creación de variables de entorno

Ahora vamos a crear nuestra propia variable de entorno. Ve a tu directorio personal y crea una carpeta llamada `Projects`. Ahora vamos a crear una variable de entorno llamada `PROJDIR` (las variables de entorno suelen ir en mayúsculas) que guarda la ruta a tu directorio de proyectos. Para crear una variable de entorno, puedes utilizar el comando `export`. En una máquina Mac o Linux, el comando sería:

```
export PROJDIR=/Usuarios/tim/Proyectos
```

Observa que en este caso no se utiliza el `$`. Cuando defines una variable de entorno, no utilizas el `$`. Utilice el `$` sólo cuando desee hacer referencia al valor de la variable.

Ahora que has creado la variable de entorno, vamos a utilizarla:

```
cd ~
cd $PROJDIR
```

Ahora debería estar en el directorio de su proyecto.

Así que ahora tenemos una gran manera de guardar una variable útil en el entorno de nuestro terminal, pero tenemos un problema. Cada vez que cierras la ventana de tu terminal, las variables de entorno se reinician, por lo que la variable de entorno `PROJDIR` se perderá. ¿Cómo lo solucionamos?

#### Guardar variables de entorno

Ahora que sabemos cómo crear variables de entorno, necesitamos aprender cómo guardarlas para que cada vez que abramos una nueva ventana de terminal, tengamos esas variables de entorno configuradas. Para guardar variables de entorno, necesitas modificar el archivo de configuración del shell en tu directorio home. Este archivo es diferente dependiendo de cuál sea tu shell por defecto. Si estás usando oh-my-zsh, entonces tu fichero de configuración se llamará `.zshrc`; si estás usando bash, entonces tu fichero de configuración se llamará `.bash_profile`.

Abre el archivo de configuración de tu shell, ya sea `.zshrc` o `.bash_profile`. A continuación, añade la siguiente línea a tu archivo:

```
export PROJDIR=/Usuarios/$USUARIO/Proyectos
```

Guarde el archivo, salga de todas las ventanas del terminal y vuelva a abrir el terminal. Intente ejecutar `echo $PROJDIR`. Debería ver la ruta a su directorio de proyectos.

Hicimos otra cosa interesante aquí. En lugar de utilizar una ruta codificada al directorio de proyectos, utilizamos otra variable de entorno para averiguar el nombre de usuario correcto. Intente escribir `echo $USER` en su terminal. Debería ver su nombre de usuario. Lo importante aquí es que una variable de entorno puede ser definida usando otras variables de entorno. Por ejemplo, si tuviéramos una carpeta `python` dentro del directorio `Projects`, podríamos querer una variable para eso también. Podríamos definirla de la siguiente manera:

```
export PYTHON_PROJ=/Usuarios/$USUARIO/Proyectos/python
```

O podemos utilizar la variable de entorno `PROJDIR` que ya tenemos configurada:

```
export PYTHON_DIR=$PROJDIR/python
```

La única pega es que la línea para exportar `PROJDIR` debe ir antes de la línea que utiliza `PROJDIR`. De lo contrario, `PROJDIR` aún no estará definido cuando lo utilicemos en la definición de `PYTHON_DIR`.

#### La variable de entorno `PATH

Una variable de entorno importante de conocer y entender es el `PATH`. Tu terminal utiliza la variable de entorno `PATH` para encontrar programas para ejecutar. Prueba lo siguiente en una nueva ventana de terminal:

```
export PATH=
```

Ahora intenta usar `ls` en la terminal. No funciona. Prueba otros comandos como `man` o `chgrp`. Ninguno de ellos funciona. Eso es porque comandos como `ls` son sólo programas almacenados en un fichero en algún lugar de tu sistema de ficheros. La razón por la que normalmente no necesitamos dar la ruta completa al comando `ls` cuando lo usamos es porque `ls` es un fichero que se encuentra en una de las carpetas especificadas en la ruta.

Abre una nueva ventana de terminal. El comando `ls` debería funcionar de nuevo. Ahora usa el comando `which` para ver de qué parte de la ruta proviene `ls`:

```
which ls
```

Normalmente, el comando `ls` se encuentra en el directorio `/bin` (aunque si estás usando oh-my-zsh, el comando puede tener el alias `ls -G`). Cambiemos nuestra variable de entorno `PATH` de nuevo, pero esta vez, asignémosla a `/bin`:

```
export PATH=/bin
```

Ahora intenta utilizar el comando ls. Debería seguir funcionando. Eso es porque `ls` se encuentra ahora en una de las carpetas del `PATH`, concretamente en `/bin`. Sin embargo, otros comandos siguen sin funcionar. El comando `man` sigue sin funcionar porque no se encuentra en el `PATH`. Vamos a añadir algunos directorios más al `PATH` en la misma ventana de terminal. Queremos añadir `/usr/bin`, `/usr/sbin`, y `/sbin`, pero no queremos reescribir la variable `PATH` completamente. En su lugar, vamos a añadir a la `PATH` que ya existe. Para ello, hacemos referencia a la variable de entorno `PATH` utilizando `$` y separamos las rutas múltiples utilizando dos puntos:

```
export PATH=$PATH:/usr/bin:/usr/sbin:/sbin
```

Ahora si haces `echo $PATH`, deberías ver la siguiente salida:

```
/bin:/usr/bin:/usr/sbin:/sbin
```

Y comandos como `man` deberían funcionar. Ahora que entiendes el `PATH`, cierra la ventana del terminal y abre una nueva ventana, para que tu `PATH` se configure correctamente.



### { Processes. }

#### Objetivos

Al final de este capítulo, usted debe ser capaz de:

* Definir qué es un proceso
* Examinar los procesos que se están ejecutando en su máquina
* Matar un proceso usando el comando `kill

#### ¿Qué es un proceso?

Un proceso es un programa que se está ejecutando en tu ordenador. Por ejemplo, cuando tienes abierto el navegador Chrome de Google, eso es un proceso ejecutándose en tu máquina. Una aplicación de correo electrónico, una ventana de terminal e incluso el comando `ls` también son procesos cuando se están ejecutando en tu máquina.

Lo bueno de los procesos es que el sistema operativo se asegura de que otro proceso no pueda acceder a toda la memoria de un proceso. En otras palabras, si un proceso falla, no debería tener ningún efecto en el resto del sistema.

Pero, ¿cómo saber qué procesos se están ejecutando en un momento dado? ¿Y cómo se puede detener un proceso desde el terminal?

#### `ps`

El comando `ps` es una herramienta útil para ver qué procesos se están ejecutando en tu máquina. Puedes ejecutar el comando `ps` por sí solo, pero lo más habitual es que utilices el comando `ps aux`. La `a` indica que estás interesado en todos los procesos, no sólo en los procesos de tu usuario actual; `u` asegura que se mostrará el propietario del proceso; finalmente, especificando `x` te aseguras de que verás una lista de todos los procesos activos, no sólo de aquellos adjuntos a un terminal.

(Nota: puede que se pregunte por qué el comando es `ps aux`, y no `ps -aux`. Para algo de historia sobre el comando, echa un vistazo a [esta](https://stackoverflow.com/questions/15102576/ps-aux-works-but-ps-aux-doesnt) pregunta de Stack Overflow).

Intenta escribir `ps aux` en tu terminal y mira lo que obtienes. Deberías ver algo similar a esto:

```
USER PID %CPU %MEM VSZ RSS TT STAT STARTED TIME COMMAND
tim 74874 8.3 1.7 3408348 139912 ??  S 3:34PM 6:39.74 /Applications/Google Chrome.app/Contents/Versions/53.0.2785.116/Google Chrome Helper.app/Contents
tim 74858 6.2 2.8 3224740 233060 ??  S 3:34PM 8:34.62 /Applications/Google Chrome.app/Contents/MacOS/Google Chrome
tim 61431 2.5 0.6 2698840 53728 ??  R 9:46AM 0:59.49 /Aplicaciones/Utilidades/Terminal.app/Contenidos/MacOS/Terminal
```

Algunas columnas importantes son `USER`, `PID`, y `COMMAND`. La columna USUARIO es el nombre de usuario del usuario que ejecutó el proceso. La columna PID es un número que identifica unívocamente al proceso. Este PID será útil muy pronto cuando aprendamos cómo detener un proceso.

#### `kill`

A veces puedes tener un proceso que por cualquier razón no responde. En otras palabras, el proceso continúa ejecutándose cuando no queremos que lo haga. Podemos detener la ejecución del proceso utilizando el comando `kill`.

Vamos a probarlo. Primero, abre cualquier archivo en la terminal usando el comando `less`. El proceso continuará ejecutándose mientras no hayas pulsado `q` para salir. En otra ventana de terminal, escribe lo siguiente:

```
ps aux
```

Ahora desplázate por la lista hasta que encuentres un proceso en ejecución que haya sido iniciado por tu nombre de usuario y cuya ruta de comandos termine en less. Una vez que hayas identificado el proceso, toma nota del PID.

A continuación, para matar el proceso, escribe `kill` y luego el PID y pulsa intro. Por ejemplo, si tu proceso tiene el siguiente aspecto:

```
tim 10011 0.0 0.0 2434948 900 s000 S+ 5:32PM 0:00.00 less readme.md
```

Entonces tu PID es `10011`. Así que para matar a less, su comando sería el siguiente:

```
kill 10011
```

Después de matar el proceso, debería ver que la ventana de terminal que se estaba ejecutando menos vuelve a un prompt de terminal normal.

#### `kill` vs. `kill -9`

A veces, cuando estás leyendo tutoriales y necesitas matar un proceso, verás que se ejecuta el comando `kill -9`, no `kill`. ¿Cuál es la diferencia entre ambos?

Cada vez que intentas matar un proceso, se envía una señal a ese proceso diciéndole que termine. Por defecto esa señal es la señal `TERM`. Sin embargo, si un programa se ha bloqueado o está congelado por alguna razón, es posible que no capte esa señal y el proceso no termine. La bandera -9 envía una señal diferente al proceso: según el manual de `kill`, -9 representa la señal `KILL`, que es un "kill no capturable, no ignorable". Si matar un proceso no funciona, intente matarlo con -9 y vea si eso hace el trabajo.

Para más información sobre `kill` y las diferentes señales que puede enviar, consulte [esta](https://superuser.com/questions/107543/bash-man-page-kill-pid-vs-kill-9-pid) pregunta de superusuario.



### { Encontrando Archivos y Carpetas. }

#### Objetivos

Al final de este capítulo, usted debe ser capaz de:

* comparar y contrastar `find` y `grep
* usar `find` para buscar ficheros y carpetas
* usar `grep` para buscar patrones en una cadena o texto
* definir qué es una _expresión regular

#### `encontrar

Uno de los comandos de terminal más útiles es el comando `find`. Cuando sabes usarlo bien, puedes encontrar fácilmente archivos en tu ordenador sin usar Spotlight, Alfred o cualquier otra GUI. Empecemos aprendiendo cómo funciona la sintaxis.

Para encontrar un archivo específico en tu directorio actual, simplemente escribe `find` y el nombre del archivo. (Si intentas encontrar una carpeta, también encontrarás todo el contenido de su interior). Por ejemplo, si intentas escribir el siguiente comando desde tu directorio personal:

```
find Descargas
```

Debería ver una lista de todas sus descargas en el terminal.

Para encontrar algo con un poco más de complejidad, utilice el siguiente patrón

1. `encontrar
2. una ruta de archivo
3. una expresión (aquí es donde tienes más flexibilidad)

Vamos a `cd` en una carpeta llamada `views` y probar este patrón para encontrar cualquier cosa con el nombre `first.txt` dentro de la carpeta `views`:

`encontrar . -name "primer.txt"`

Esto está bien si sabemos exactamente el nombre del fichero que buscamos, pero muchas veces necesitamos usar caracteres comodín como `*`, `?` y `[]`. La diferencia entre estos caracteres es la siguiente:

`*` - cualquier número de caracteres
`?` - un carácter
`[]` - cualquiera de los caracteres dentro de los corchetes

He aquí algunos ejemplos más:

* encontrar dentro de la carpeta `views` (supongamos que estamos dentro de la carpeta views) cualquier cosa que termine en `.html` => `find . -name "*.html"`
* buscar dentro de la carpeta `views` (supongamos que estamos dentro de la carpeta views) cualquier cosa que termine con una extensión de tres letras como `.txt` o `.css` => `find . -name "*.???"`
* buscar dentro de la carpeta `views` (supongamos que estamos dentro de la carpeta views) cualquier cosa que empiece por la letra `f` `t` o `s` => `find . -name "[fts]*"`
* encontrar dentro de la carpeta `views` cualquier cosa que tenga el texto `main` en algún lugar del nombre del archivo (esto podría ser el principio también) `find . -name "*main*"`

#### `grep`

Otra herramienta extremadamente útil para encontrar información que ya hemos visto antes es `grep`. Mientras que `find` es para archivos y carpetas, `grep` es excelente para buscar valores específicos en una cadena o en un archivo de texto. Si escribes `grep` por sí solo, no es tan valioso porque necesitas asegurarte de pasarle un nombre de fichero y un texto. También puedes usar `grep` con piping y `cat`.

Ya hemos visto ejemplos usando `grep` con `cat` para encontrar palabras como `cat gente.txt | grep Elie` para encontrar si la palabra Elie existe en el fichero `gente.txt`. Utilicemos como ejemplo el siguiente fichero al que llamaremos `names.txt`:

```
Lisa
Mark
Elie
Beth
Tim
Elizabeth
Tom
Matt
Liza
Janey
Jane
Shana
```

Aumentemos un poco más nuestros conocimientos sobre `grep` e introduzcamos algunas banderas.

* `-i` para buscar sin distinguir mayúsculas de minúsculas

`grep -i "elie" nombres.txt` => `Elie`

* `-w` para buscar palabras completas

`grep -i "beth" nombres.txt` => `grep -i "beth" nombres.txt`

```
Beth
Elizabeth
```

`grep -iw "beth" nombres.txt` => `Beth`

* `-A` mostrar un cierto número de líneas después de

`grep -A 3 "Beth" nombres.txt`

```
Beth
Tim
Elizabeth
Tom
```

* `-B` mostrar un cierto número de líneas líneas antes de

`grep -B 3 "Beth" nombres.txt`

```
Lisa
Mark
Elie
Beth
```

* `-C` mostrar un cierto número de líneas alrededor de

`grep -C 3 "Beth" nombres.txt`

```
Lisa
Mark
Elie
Beth
Tim
Elizabeth
Tom
```

* Patrón de inversión `-v` (puede pensar en esto como cualquier cosa que NO sea lo que está buscando)

`grep -v "Jane" nombres.txt`

```
Lisa
Mark
Elie
Beth
Tim
Elizabeth
Tom
Matt
Liza
Shana
```

* `-c` cuenta partidos

`grep -c "Jane" nombres.txt` => `2`

* `-n` muestra el número de línea

`grep -ni "Jane" nombres.txt`

```
10:Janey
11:Jane
```

Hay **muchas** más opciones con `grep`; puedes buscar más en google o en `man grep`.

#### Comodines con `grep

Anteriormente vimos comodines con `find`, así que ¿cómo podemos usarlos con `grep`? La clave es usar _expresiones regulares_. Las expresiones regulares se utilizan para definir patrones en una cadena de caracteres, que luego se usan para buscar posibles coincidencias en un texto. Las expresiones regulares son comunes y bastante potentes: puede utilizarlas para comprobar si un usuario ha enviado una dirección de correo electrónico o un número de teléfono con el formato adecuado, por ejemplo.

No profundizaremos aquí en las expresiones regulares. Hay un gran número de [referencias interactivas](https://regexr.com/) en línea. Por ahora, veamos un par de ejemplos de la sintaxis:

`.` - coincide con cualquier carácter

**Ejemplo:** ¿Cuántos nombres tienen un nombre completo de cuatro caracteres?

`grep -wc "...." nombres.txt` => `7`

`*` - coincide con cero o más del carácter o expresión precedente.

**Ejemplo:** ¿Cuántos nombres empiezan por T mayúscula?

`grep -wc "T.*" nombres.txt` => `2

`[]` - cualquier carácter específico

**Ejemplo:** ¿Cuántos nombres empiezan por L, M o E mayúscula?

`grep -wc "[LME].*" nombres.txt` => `6`

`[^]` - no coincide

**Ejemplo** ¿Cuántos nombres **no** empiezan por T mayúscula?

`grep -wc "[^T].*" nombres.txt` => `10



## { Terminal Avanzado - 1 Ejercicios. }

#### Parte I

Responda a las siguientes preguntas:

1. Crea una variable de entorno llamada `FIRST_NAME` y establécela igual a tu nombre de pila (no es necesario que sea permanente).
2. Imprime la variable "PRIMER_NOMBRE
3. Imprime la variable `$PATH
4. ¿Qué es la variable `$PATH`?
5. ¿Por qué querrías crear una variable de entorno?
6. ¿Cómo se guardan permanentemente las variables de entorno?
7. 7. ¿Qué es un proceso?
8. ¿Cómo se listan todos los procesos que se están ejecutando en la máquina?
9. 9. ¿Qué es un PID?
10. 10. ¿Cómo se termina un proceso?
11. ¿Cuál es la diferencia entre `kill` y `kill -9`?
12. ¿Qué opción de `grep` permite buscar sin distinguir mayúsculas de minúsculas?
13. ¿Qué opción de `grep` permite un cierto número de líneas antes de la coincidencia?
14. ¿Qué bandera `grep` permite un cierto número de líneas alrededor de la coincidencia?
15. ¿Qué bandera `grep` permite un cierto número de líneas después de la coincidencia?
16. ¿Qué bandera `grep` permite la búsqueda completa de palabras?
17. ¿Qué opción de `grep` muestra el número de línea de una coincidencia?

#### Parte II

Escribe los siguientes comandos de terminal para hacer lo siguiente (asume que `instructores.txt` es un fichero imaginario):

1. Encuentra todos los archivos dentro de la carpeta `Desktop` que tengan el nombre "learn".
2. Encuentra todos los archivos dentro de la carpeta `Desktop` que empiecen por "P".
3. 3. Encuentre todos los archivos dentro de la carpeta `Desktop` que terminen con `.txt`.
4. Encuentra todos los archivos dentro de la carpeta `Desktop/views` que tengan el nombre `data` en algún lugar de su nombre de archivo.
5. Dentro del archivo `instructors.txt`, obtenga el número de veces que aparece la palabra "Elie".
6. Dentro del fichero `instructors.txt`, listar todas las coincidencias de cualquier palabra completa que empiece por "P" mayúscula.
7. Dentro del archivo `instructors.txt`, liste todos los números de línea de cualquier palabra completa que empiece por "z" (debe coincidir independientemente de si es mayúscula o minúscula).



## Nivel Avanzado - 2 { OPTIONAL }



### { SSH. }

#### Objetivos

Al final de este capítulo, deberías ser capaz de:

* configurar una instancia EC2 en Amazon
* utilizar el comando `ssh` para conectarte de forma segura a un servidor remoto
* usar el comando `scp` para copiar archivos a un servidor remoto

#### SSH

SSH, o **S**ecure **Sh**ell, proporciona un canal seguro para acceder a otros ordenadores. Comúnmente utilizamos SSH para iniciar sesión de forma remota y conectarnos de forma segura a otros servidores. Para practicar con SSH vamos a configurar nuestros propios servidores remotos utilizando Amazon EC2. Esta configuración puede ser un poco intimidante, pero es una habilidad muy valiosa para saber con cualquier tipo de desarrollo. ¡Vamos a empezar!

#### Configurando una Instancia EC2

Como se muestra en la siguiente lista, hay un buen número de pasos para configurar tu instancia. Los enlaces proporcionados también proporcionan una buena cantidad de contexto y ayudan a explicar el propósito de cada uno de los siguientes pasos.

1. Asegúrese de que dispone de una cuenta de Amazon Web Services (AWS). Puede iniciar sesión / registrarse [aquí](https://docs.aws.amazon.com/) y haga clic en la parte superior derecha.
2. Crea un usuario IAM [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-an-iam-user).
3. Crea un par de claves [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-a-key-pair)
4. Crear una VPC [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-a-vpc)
5. Crear un grupo de seguridad [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html#create-a-base-security-group)
6. Lance su instancia [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2\_GetStarted.html#ec2-launch-instance\_linux)
7. 7. Conéctese a su instancia [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html#ec2-connect-to-instance-linux).

Para conectarse a su instancia mediante SSH puede iniciar [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html).

Antes de intentar utilizar SSH, asegúrese de que su instancia se está ejecutando y de que se han superado las comprobaciones. Para ello, escriba algo parecido a `ssh -i ./me-key-pair-uswest2.pem ec2-user@YOUR_PUBLIC_DNS`.

Una vez que se haya conectado a través de SSH, puede salir del intérprete de comandos escribiendo `exit`.

#### Copia segura de archivos a la Instancia EC2 con scp

Para mover archivos a tu instancia EC2, usamos el comando `scp` para copiar información de forma segura. Necesitaremos nuestro archivo `pem` que usamos antes, así que asegúrate de saber dónde se encuentra. El patrón para `scp` es el siguiente:

`scp -i PATH_TO_YOUR_PEM_FILE FILE_TO_MOVE USERNAME@PUBLIC_DNS`.

Este comando movería el archivo `move.txt` de mi directorio actual al directorio `home` de mi instancia EC2.

`scp -i ./me-key-pair-uswest2.pem mover.txt ec2-user@ec2-54-213-7-226.us-west-2.compute.amazonaws.com:/`

#### Finalice su instancia

Cuando termine de trabajar en este tutorial, **DEBE** finalizar su instancia para que no siga en ejecución. Esto asegura que no se le cobrará nada. Puede leer más sobre esto [aquí](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2\_GetStarted.html#ec2-clean-up-your-instance)





### { Cut, Sed, Awk, y Xargs. }

#### Objetivos

Al final de este capítulo, deberías ser capaz de:

* Entender qué hace el comando `cut` y enumerar algunos casos de uso.
* Entender lo que hace el comando `sed` y enumerar algunos casos de uso para el mismo.
* Entender qué hace el comando `awk` y enumerar algunos casos de uso.
* Entender qué hace el comando `xargs` y enumerar algunos casos de uso.

#### cut

El comando `cut` es muy útil para separar o delimitar cadenas y caracteres. Si necesitas separar archivos de texto o encontrar ciertos caracteres, `cut` es el camino a seguir. Veamos cómo funciona con algunos ejemplos en un archivo llamado `languages.txt`:

`idiomas.txt`

```
Java,James
Ruby,Matz
Lisp,John
Bash,Brian
Self,David
```

He aquí un ejemplo usando `cut` para tomar los 4 primeros caracteres de cada línea (la bandera `-c` indica que el rango numérico que viene después de la bandera se refiere a caracteres, no a bytes):

`cut -c 1-4 idiomas.txt`

```
Java
Ruby
Lisp
Bash
Auto
```

Ahora vamos a coger los apellidos, pero no por el número de caracteres. En su lugar, vamos a hacerlo delimitando (dividiendo) en la coma

`cut -d, -f2 idiomas.txt`

```
James
Matz
John
Brian
David
```

¿Qué es `-f2`? `-f` se refiere a cada porción que ha sido dividida por la bandera delimeter (`-d`). Así que si sólo queremos los nombres podemos hacer

cut -d, -f1 idiomas.txt

```
Java
Ruby
Lisp
Bash
Auto
```

Esto es mucho mejor porque si tuviéramos idiomas con longitudes de caracteres diferentes, `cut -c 1-4 idiomas.txt` ¡no funcionaría!

A continuación, intente utilizar `cut` para imprimir sólo los autores. Luego ordénalos y devuelve los dos primeros autores.

He aquí una solución:

`cut -d, -f2 idiomas.txt | ordenar | head -n 2`

#### sed

Sed, o Stream EDitor, es uno de los comandos de terminal _mucho_ más complejos, así que sólo repasaremos algunos casos de uso sencillos. Hay muchas, muchas cosas que puedes hacer con `sed` así que intenta seguir estos ejemplos y ¡anímate a seguir aprendiendo!

Sed se usa comúnmente para encontrar y reemplazar texto, editar texto en un archivo, e imprimir ciertas partes de un archivo (aunque puede hacer mucho más). Empecemos por encontrar y reemplazar cada coma en el archivo `languages.txt` por dos puntos.

Este es el comando:

`sed 's/,/:/g' languages.txt`

Vamos a desglosar esto:

`sed` - el comando
`s` - sustituto
`,` - nuestro antiguo valor, una coma\_
`:` - nuestro nuevo valor
`g` - globalmente, hacer esto en todas partes no sólo el primer partido\
`languages.txt` - el archivo con el que estamos trabajando

Esto es lo que el comando debería mostrar:

```
Java:James
Ruby:Matz
Lisp:Juan
Bash:Brian
Yo:David
```

Observa que si `cat languages.txt` después de ejecutar el comando `sed` anterior, el archivo original no se modifica. Para editar el archivo, necesitamos usar la bandera `i` para editar en su lugar. Pero si intentas ejecutar el comando con la bandera `-i` obtendrás un error sobre caracteres extra. Puesto que también estamos especificando argumentos adicionales, necesitamos utilizar la bandera `-e` también.

sed -ie 's/,/:/g' idiomas.txt

Si ejecutas este comando y luego `cat languages.txt`, ¡verás que todo ha sido reemplazado!

Sólo estamos arañando la superficie con `sed`. Si quieres aprender más sobre él puedes leer [esto](https://www.tutorialspoint.com/sed/sed\_basic_syntax.htm) y [esto](http://www.panix.com/\~elflord/unix/sed.html)

#### awk

Similar a `sed`, `awk` es una herramienta de procesamiento de texto increíblemente potente. De hecho, AWK es en sí mismo un lenguaje que puede hacer prácticamente cualquier tipo de manipulación de texto que se te ocurra. Cubriremos brevemente `awk` y repasaremos algunos comandos útiles que puedes usar con él.

Comencemos con el simple comando `awk '{print}' languages.txt`. Esto simplemente imprimirá el archivo `languages.txt`. ¿Pero qué pasa si sólo queremos imprimir una parte determinada del fichero? También podemos utilizar `awk` como delimitador utilizando la bandera `-F`. Pongamos `:` como delimitador e imprimamos sólo la primera parte delimitada con `$1`.

`awk -F ':' '{print $1}' languages.txt`

Veamos otro ejemplo, utilizando el comando `history`. Si escribes esto en el terminal, deberías ver una lista de tus comandos recientes. Usemos `awk` para obtener un historial de sólo los nombres de los comandos que hemos usado, sin más detalles. Cuando usamos `awk`, si el delimitador es un espacio vacío no necesitamos la bandera `-F`. Así que si queremos encontrar los comandos que hemos usado recientemente podemos escribir `history | awk '{print $2}'`.

También podemos usar `awk` para imprimir filas y columnas. Por ejemplo, si escribimos `df -h` en el terminal veremos una tabla con información sobre nuestro disco duro (`df` es la abreviatura de display free desk space). Pasemos el resultado de este comando a `awk`:

```
df -h | awk 'FNR == 2 {print $4}''
```

FNR se refiere al número de registro, que normalmente es un número de línea. Esencialmente le estamos diciendo a `awk` que coja el elemento de la 2ª fila y 4ª columna de la tabla, que en este caso debería ser tu espacio disponible en disco.

Si quieres leer más sobre `awk`, echa un vistazo a [este](https://www.tutorialspoint.com/awk/) tutorial.

#### xargs

A veces puedes querer ejecutar el mismo comando para múltiples entradas. Por ejemplo, tal vez quieras buscar un determinado texto en varios archivos de texto. Este es un caso en el que el comando `xargs` puede ser muy útil. Aquí tienes algunos ejemplos de uso de `xargs`; cada uno ejecuta el comando para un grupo de ficheros en lugar de para uno solo.

Buscar . -name *.html | xargs grep "elie"` - busca el texto "elie" dentro de cada fichero `html` de la carpeta actual.

`ls | xargs wc -l` - cuenta la cantidad total de líneas de cada fichero de una carpeta

`find . -name "*" | xargs open` - abre todos los ficheros de la carpeta actual.

Buscar . -name "*.css" | xargs open` - abre todos los archivos `css` de la carpeta actual.

buscar . -name "*.html | xargs rm` - elimina todos los archivos que terminan en `.html`.

`ls | xargs -t -I {} mv {} {}.md` - añade una extensión de archivo markdown a todos los archivos (la bandera `-I` reemplaza las ocurrencias; la bandera `-t` hace que el comando que se ejecuta para cada entrada se registre en el terminal antes de ser ejecutado, lo que puede ser útil para la depuración).

Puedes leer más sobre `xargs` [aquí](http://www.cyberciti.biz/faq/linux-unix-bsd-xargs-construct-argument-lists-utility/)





### { Shell Scripting y Vim. }

#### Objetivos

Al final de este capítulo, deberías ser capaz de:

* escribir scripts de shell simples con argumentos
* usar `vi` para abrir y editar archivos

#### Shell Scripting

Hasta ahora hemos aprendido a usar comandos de terminal, pero nuestros comandos no son dinámicos. Sabemos exactamente cuáles son los nombres de los archivos o lo que podríamos estar buscando. Nuestros comandos tampoco son fácilmente reutilizables; si el nombre del archivo cambia, tenemos que escribir todo el comando de nuevo. Para reducir la duplicación y ejecutar comandos mucho más sofisticados en el terminal, podemos escribir scripts de shell utilizando un lenguaje llamado bash. Para empezar, creemos un archivo llamado `first.sh` y dentro coloquemos lo siguiente

```
echo "Hola Mundo"
```

Ahora si intentamos ejecutar `./first.sh` nos dirá `permission denied: ./first.sh`. Así que tenemos que hacer que este programa sea ejecutable. Cambiemos los permisos a `755` para que cualquiera pueda ejecutar este archivo: `chmod 755 primer.sh`. ¡Ahora podemos ejecutar `./first.sh`!

Hagamos un segundo script llamado `second.sh`. Dentro de este archivo, escribe lo siguiente:

```
echo Hola $1
```

¿Qué crees que representa `$1`? Primero `chmod 755 second.sh` y luego ejecuta `./second.sh` - deberíamos ver "Hola". ¡Ahora probemos `./second.sh World` y deberíamos ver "Hello World"! Lo que acabamos de hacer es pasar un argumento a nuestro script. Usando argumentos que comienzan con `$1` y continúan hacia arriba es como podemos hacer scripts más dinámicos.

#### Tu turno

Escribe un script llamado `sum.sh` que acepte dos argumentos y se haga eco de la suma de los dos números. Puede que necesites investigar un poco [aquí](https://stackoverflow.com/questions/6348902/how-can-i-add-numbers-in-a-bash-script).

Aquí tienes una solución:

```
echo $(($1+$2))
```

#### Scripts más complejos

Hay mucho más que podemos hacer con shell scripting, incluyendo lógica condicional, sentencias if, y mucho más. Pero por ahora, intentemos escribir algunos scripts prácticos que nos ayuden con las tareas diarias. Muy comúnmente buscamos un proceso usando `ps aux | grep "Algo"`. En lugar de teclear todo eso, podríamos hacer un script que lo haga por nosotros y le pase un argumento. Intentémoslo con un script llamado `process.sh`. Podría ser algo como esto.

```
ps aux | grep $1
```

¡Ahora esto es útil si queremos buscar un proceso! Si quieres usar el script frecuentemente, querrás asegurarte de que está en algún lugar de tu $PATH. También puedes eliminar la extensión `.sh` si estás haciendo esto.

#### Vim

Vim es un editor de texto basado en terminal. Puede ser bastante intimidante al principio, pero si le dedicas tiempo a aprender a usarlo, puedes convertirte en un desarrollador extremadamente eficiente. Para abrir algo en `vi`, simplemente teclea `vi NOMBRE_DEL_ARCHIVO`. Una vez que estés en vim puedes salir **sin** guardar pulsando `escape + : + q`. Si no funciona pulse `escape` + `:` + `q!`. Si quieres salir y guardar un fichero puedes pulsar `shift + Z + Z` o `escape + : + w + q!`.

La primera vez que entres en vim estarás en lo que se llama "modo visual". Esto significa que su teclado estará configurado para navegar y no para insertar caracteres; si teclea letras y no ve que sale nada, ¡no se preocupe! Para hacer inserciones, pulse `i` para entrar en el modo `insert`. Aquí puede hacer cambios en los archivos y escribir como lo haría normalmente. Sólo recuerda que si quieres salir de un fichero tienes que estar en modo `visual`.

Puedes obtener más práctica utilizando `vimtutor` - simplemente escribe `vimtutor` en tu terminal y podrás empezar. Alternativamente, si quieres un tutorial más visual puedes echar un vistazo a [Vim Adventures](https://vim-adventures.com/).



## { Terminal Avanzado - 2 Ejercicios. }

Utilice el siguiente archivo de texto para responder a las preguntas

```
Elie-Schoppik-sushi
Tim-Garcia-gominolas
Janey-Keig-bagels
Colt-Steele-tacos
Matt-Lane-pizza
```

1. Sustituye todas las `-` por `:` utilizando `sed`.
2. Devuelve un fichero con sólo el nombre y el apellido separados por un espacio (puedes hacerlo con `cut` y `sed` o sólo `sed`)

```
1>>>>2
2>>>>3
3>>>>4
4>>>>5
```

1. Usando `cut` imprime sólo los números 2, 3, 4, 5. Usa `xargs` para imprimirlos todos en 1 línea
2. Usando `xargs` en el directorio `./Desktop`, encuentra todos los ficheros que incluyen el texto `Welcome`.
3. Escribe un script de shell llamado `access_file.sh` que acepte un parámetro y cambie los permisos a `755`
4. Escribe un script de shell llamado `unaccessible_sh.sh` que acepte un parámetro y cambie los permisos a `300`
5. Usando `sed` escribe el comando para reemplazar todas las instancias del nombre "foo" por la cadena "bar" en un fichero llamado `baz.txt`
6. Escribe el comando para imprimir sólo todos los `pid`s usando `awk`
7. Escribe el comando `df -h` - te mostrará cuánto espacio tienes en tu disco duro. Usando el comando `awk`, imprime **sólo** el primer porcentaje de capacidad.

