### 1 - Introducción a GIT

Trabajar con nuesto código de forma segura es tan importante como aparender a programar. 
  
Hay dos conceptos distintos que vamos a trabajar en este eje, **Git** y **GitHub**

###### Git es un VCS de código abierto rápido, versátil, muy escalable y gratuito. 

Git es un sistema distribuido, lo que significa que el historial completo de un proyecto se almacena en el cliente y en el servidor. Se pueden editar archivos sin conexión de red, protegerlos localmente y sincronizarlos con el servidor cuando una conexión esté disponible. Si un servidor deja de funcionar, todavía tendrá una copia local del proyecto. Técnicamente, ni siquiera es necesario tener un servidor. Los cambios pueden pasarse por correo electrónico o compartirse mediante medios extraíbles, pero, en la práctica, nadie usa Git así.

###### GitHub es una plataforma en la nube que usa Git como tecnología principal. 

GitHub actúa como el repositorio remoto, además, funciona como una red social que conecta a desarrolladores y usuarios con el fin de ir introduciendo constantemente mejoras, simplificando el proceso de colaboración en proyectos y proporciona un sitio web, más herramientas de línea de comandos y un flujo integral que los desarrolladores y usuarios pueden usar para trabajar juntos.  mencionado anteriormente.

En esta primer seccion nos vamos a concentrar unicamente de **Git**. 
    
  * Git, es independiente de GitHub. GitHub depende de Git
  * Web oficial de GIT es: https://git-scm.com
  * Es de código abierto. Todo su código fuente se pude leer en GITHUB.
  * Git es un sistema de control de versiones distribuido.
  * Libro oficial en español: https://git-scm.com/book/es/v2
  
La principal diferencia con respecto a otros sistemas de control es que se basa en una arquitectura distribuida, es decir, no cuenta con un único espacio en donde almacenar el histórico de versiones sino que facilita que cada desarrollador pueda guardar el historial completo de todas las modificaciones que ha realizado. Probablemente, esa característica sea la principal causa de su popularidad, pues nos git nos permite: 

  * Registrar historico de trabajo código
  * Crear copias de seguridad
  * Trabajar en equipo de forma rapidad y sin errores
       
### 2 - Historia de Git

**Git was created for use in the development of the Linux kernel by _**Linus Torvalds**_ and others developing the kernel. 2005**

  ![image](https://github.com/lole-s/Testing-QA-CUAC/assets/84929029/99bf0c9b-9dae-403f-a396-34647122bbd6)

Desde que en 2005, el ingeniero de software Linus Torvalds (padre del kernel del sistema operativo Linux) diseño Git como un sistema de código abierto con el que supervisar la versiones, este ha ido evolucionando y presentando actualizaciones periódicas, adaptándose a las necesidades que surgen con la permanente evolución de la tecnología digital hasta convertirse en una herramienta indispensable para la mayoría de los desarrolladores.

### 3 - Instalación de Git

WEB: 
  clientes gráficos
  

Git es una herramienta por consola de comandos que se integra bastante bien en los principales editores de programación existente. A continuación te indicamos cómo instalarlo para los diferentes sistemas operativos. 

**Instalar Git en Ubuntu**

La instalación de git en Ubuntu no puede ser más fácil. Sólo hay que abrir un terminal de comandos y ejecutar: 

> sudo apt install git

**Instalar Git en Windows**

Sólo debe descargarse el instalador correspondiente desde la página oficial del proyecto Git y descargar el instalador correspondiente al sistema operativo usado teniendo en cuenta la arquitectura de nuestro sistema: 32 o 64bits.

https://git-scm.com/downloads

El instalador para Windows abrirá un asistente que mostrará una serie de opciones durante el proceso. Dejar las opciones marcadas por defecto será suficientes en la mayoría de las situaciones.

### 4 - Comandos básicos de la terminal

Vamos a comenzar a trabajar por consola creando un proyecto sencillo con Git en forma local para entender cómo funciona y vamos a ver los comandos básicos a utilizar tanto de linux como especificamente de git. Luego la idea es ver como se integra git con Visual Studio Code

Abrir  Git Bash --> Luego de la instalción, localizar en acceso a la consola "Git Bash"

GIT BASH es una herramienta de línea de comandos para Windows que nos permite ejecutar comandos de Git.

💡 Tip: Bash significa Bourne Again Shell. Un bash es una aplicación usada para interactuar con el sistema operativo de una computadora a través de comandos.

![image](https://github.com/lole-s/Testing-QA-CUAC/assets/84929029/febcb0f2-f618-460d-a2b2-ef9565ae65a7)

Una vez que el proceso haya terminado correctamente, compruebe la instalación ejecutando git de prueba con:

> git --version

> git -v

> git --help 

> git -h

Comandos básico de terminal:

list 
> ls -lha

change directory
> cd

print working directory
> pwd

make directory
> mkdir

Clear console
> clear

> touch

### 5 - Configuración de Git

Asociamos por única vez nuestro usuario y email

--Configuracion global:

> git config user.name "lole-s" user.email "jcsodo@gmail.com" 

*ver archivo de configuración C:/Users/operador4/.gitconf

### 6 - "git init"

Crear una carpeta de proyecto nuevo

> mkdir miProyecto

> cd miProyecto

> ls -alh

--inicializar el contexto de un control de versiones en el directorio raiz del proyecto

> git init

O bien si no quieres posicionarte en la carpeta puedes darle la dirección de la misma como argumento al comando

> git init "directorio"

Listamos nuevamente los archivos y directorios de nuestro proyecto

> ls -alh

y vemos que se ha creado el directirio ".git"

**a partir de aquí el directorio trabaja con control de versiones**

--ver directorio oculto "../miProyecto/.git/" en el cual se guarda la logica de git para este proyecto

--el .git indica que el directorio trabaja con control de versiones

### 7 -  Conceptos básicos de Git

**¿Cómo funciona Git al momento de administrar mi proyecto?**

Entender el funcionamiento de Git normalmente es muy fácil, pero se vuelve confuso al momento de llevarlo a la práctica. Para simplificar  tratemos de verlo en  imágenes:

###### Primero: tanto al momento de crear un proyecto como cuando lo clonamos, tendremos 3 áreas de importancia que son parte del software Git:

**La carpeta (directirio) o área de trabajo (Working Área)**
**El área de ensayo o preparación (Stagin Área)**
**Nuestro repositorio local («.git»)**

Los siguientes conceptos son esenciales para trabajar con Git.

**Repositorio (Repository)**
Un repositorio es donde Git almacena los archivos de tu proyecto y las distintas versiones de tus archivos. Un repositorio puede ser local o remoto. Un repositorio local se guarda de forma local en tu computadora. Un repositorio remoto se guarda en los servidores del servicio de hosting que escojas (por ejemplo, GitHub).

**Directorio de trabajo (Working directory)**
Este es el directorio del proyecto en el sistema de archivos, donde se guardan los archivos. Esta es, por ejemplo, la carpeta que abres en tu editor de código o IDE para trabajar con tus archivos.

**Área de preparación (Staging area)**
Este es el conjunto de archivos y cambios que serán incluidos en el siguiente commit. Podemos agregar y remover archivos de esta área si es necesario.
![image](https://github.com/lole-s/Testing-QA-CUAC/assets/84929029/86678da4-5858-4a1b-ac28-8edd56da062a)

**Commit**
Un commit es como una "foto" de tu proyecto en un momento en particular. Un commit registra un cambio que se realizó en el proyecto. Tú escoges cuándo crear un commit y qué incluir en el commit.
  * Para describir los cambios registrados en un commit, escribimos un mensaje de commit que podemos verificar al trabajar en el proyecto.
![image](https://github.com/lole-s/Testing-QA-CUAC/assets/84929029/208310a1-a83f-4ee7-b42a-662682ca584b)

**Rama (Branch)**
Una rama es una línea independiente de desarrollo de un proyecto que es administrada y rastreada por Git. Cada proyecto iniciar con una rama por defecto que normalmente llamamos MAIN o MASTER. Podemos crear una rama para trabajar en un aspecto nuevo del proyecto sin afectar la versión principal.

![image](https://github.com/lole-s/Testing-QA-CUAC/assets/84929029/09690117-2d33-4c8c-a922-e9f4d32ddc87)

**Fusionar (Merge)**
Podemos combinar o fusionar (merge) ramas si necesitamos incorporar los cambios que hicimos en una rama en otra rama. Esto es lo que normalmente hacemos cuando un aspecto nuevo está listo para ser incorporado a la versión en vivo del proyecto.

![image](https://github.com/lole-s/Testing-QA-CUAC/assets/84929029/a8c53866-0830-4b1d-8180-d473ad1d0023)


### 8 - "git status", "git add" y "git commit"

--ver estado de proyecto

> git status

Not commits yet

-- creo un nuevo archivdo dentro de mi proyecto

> touch hellogit.py

> git status

**Status:** 
El comando «git status» nos mostrará el estado del directorio de trabajo, es decir, de donde estamos posicionados trabajando y también aquellos archivos que Git está siguiendo. Recuerdas que Git llevaba algo así como un historial o cache llamado "Stagin Area" donde los Commits eran los cambios realizados y marcaban un punto de referencia en cada cambio del archivo. El comando «git status» nos mostrará aquellos archivos que están en el Stagin Area, es decir, que están siendo seguidos en el área de ensayo.
Vemos que Git nos indica que estamos sobre la rama «master» que es la principal de los proyectos. Y que además no hemos realizado ningún Commit todavía, por lo que no hay un punto de referencia al que volver. No hemos realizado cambios, pero lo más importante es que nos muestra un archivo en letra rojas.  Y nos avisa que estos archivos no están siendo seguidos. Así que vamos a seguirlos. Usando el comando «git add».

--preparar archivos para la primer foto del proyecto

**Add (Seguimiento de archivos):**

En Git el proceso de guardar resulta diferente a el clásico «guardar» al que estamos acostumbrados. En git podemos verlo como «ir confirmando cambios a distintos niveles».

Al utilizar el comando «git add» seguido del nombre de un archivo o bien utilizando un comodín «.» para todos los archivos del directorio, estamos ordenando a Git realizar un seguimiento del mismo. Lo que significa que nos avisará cuando se hagan cambios.
Cada vez que modifiques el archivo con tu editor de código y des «guardar..» en el mismo. Git detectará que el archivo ha cambiado.. Y haciendo otro «git status» lograrás verlo en rojo nuevamente.

Como para ejemplificar esto a continuación añadiremos el archivo nuestro a seguimiento:

> git add hellogit.py

o bien podemos usar comodín para añadir todos los archivos que se encuentren en el directorio

> git add .

Al hacerlo simplemente Git no nos mostrará nada, pero al volver a solicitar un «estado» mediante «git status» veremos lo siguiente:
> git status

Donde ahora vemos el archivo como agregado para seguimiento de cambios. Pero sin ninguna foto (commit)

--Hacemos la primer confirmación o foto del proyecto
> git commit -m  "este es mi primer commit"
> git status

#### Git log
--git añade un hash al commit para identificar el momento de la foto
> git log
commit fb8e3eb7742961cafcac4f25b4ce098d91c0fda0
Author: lole-s <jcsodo@gmail.com>
Date:   Wed Feb 21 08:51:34 2024 -0300

    este es mi primer commit

> touch hellogit2.py
> vim hellogit2.py
	print ("hello Git!")
> git status
> git add hellogit2.py
> git status
> git commit -m  "este es mi 2do commit"
> git log

#### Git de VSCode


_____
* Apunte de Majo: https://drive.google.com/file/d/1sHgKrrea1-HpityOEYqFLjRdaum85CnW/view
* Curso Mouredev: https://www.youtube.com/watch?v=3GymExBkKjE&t=196s
* Curso freeCodeCamp.org: https://www.freecodecamp.org/espanol/news/aprende-git-y-github-curso-desde-cero/
____

