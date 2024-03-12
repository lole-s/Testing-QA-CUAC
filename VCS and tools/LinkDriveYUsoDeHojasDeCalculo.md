#### _Eje2. Control de Código Fuente (VCS)_

## Drive
_Definición:_ Google Drive es un servicio de alojamiento y sincronización de archivos desarrollado por Google. Lanzado el 24 de abril del 2012, el servicio permite a sus usuarios almacenar archivos en la nube (en los servidores de Google), sincronizar archivos entre dispositivos y compartir archivos. Cada usuario cuenta con 15 gigabytes (GB) de espacio gratuito para almacenar sus archivos, ampliables mediante diferentes planes de pago. Es accesible a través del sitio web desde computadoras y disponen de aplicaciones para Android e iOS que permiten editar documentos y hojas de cálculo.1​

Referencia: https://es.wikipedia.org/wiki/Google_Drive

_Aprende a sacar el máximo provecho a tu Google Drive:_ https://www.youtube.com/watch?v=nOiffy6zGLY

_Trucos google drive:_ https://www.youtube.com/watch?v=EXjt8xW43Yw

**Ejercicio 1:**	
  1. Inicia sesión en Google Drive.
  2. Crear una carpeta nueva llamada *ProA2024*.
  3. Crear otra carpeta llamada *Testing_QA*
  4. Ingresar a la carpeta *Testing_QA*  y crear una hoja de cálculo llamada *Testing_Sheet_?????*
  5. Salir de la carpeta *Testing_QA* y luego moverla dentro de *ProA2024*
  6. Compartir el link del archivo *Testing_Sheet_?????* a la dirección: *jcsodo@escuelasproa.edu.ar*

**Ejercicio 2:**
  1. En tu computadora crea una carpeta llamada "Proa2024_?????" en la direccion D:\
  2. Ahora crear una carpeta desde la terminal (Run.. "cmd")
  3. mkdir D:\Proa2024_?????\Testing_QA\
  4. Ir a la carpeta creada y crear el archivo de txt "testing.prueba.txt"
  5. Copiar (arrastrar y soltar) dentro de la carpeta *Testing_QA* alojada en el Drive
____
_Qué es el CMD?_

El Símbolo del sistema, también llamado CMD, forma parte de Windows y no puede ser desinstalado. Es una herramienta que, mediante comandos, permite realizar acciones avanzadas. Si bien puede parecer a la Terminal de GNU/Linux, el CMD no es tan potente.
A continuación se proporcionas los comandos más comunes usados en Windows y sus homólogos en Linux.ones.

**TABLA DE COMANDOS SIMILARES ENTRE WINDOWS Y LINUX**

| Propósito | WINDOWS | LINUX | Ejemplo básico de LINUX |
|----|----|----|----|
| Ayuda sobre comandos | cmd /? | man cmd | man comando |
| Crear un directorio | mkdir |mkdir| mkdir /home/qdirectorio |
| Cambia a un directorio | cd |cd | cd /home/qdirectorio |
| Sube un directorio | cd .. | cd .. | |
| Lista directorio | dir | ls -ls| |
| Borra la pantalla | cls | clear| |
| Cierra la ventana | exit |exit| |
| Borrar un directorio | rmdir | rmdir | rmdir /home/qdirectorio |
| Muestra un archivo | more | more | more qfichero |
| Renombra un archivo | rename | mv | mv nombreold nombrenew |
| Copia archivos | copy | cp | cp qfichero.txt /home/qdirectorio |
| Mueve archivos | move | mv | mv qfichero.txt /home/qdirectorio |
| Muestra o conf fecha | date | date| |
| Muestra o conf hora | time | date| |
| Borra archivos| del | rm | rm qfichero.txt |
| Busca texto en archivo | find | grep | grep “que contenido” qfichero.txt |
| Crea un archivo | copy con | touch | touch newfichero.txt |
| Visualiza la salida std | echo | echo | echo Testing_QA_CUAC |
____     
## Google Sheet

_Definición:_ Hojas de cálculo de Google (en inglés Google Sheets) es un programa de hojas de cálculo que se incluye como parte del conjunto gratuito de Google Docs Editors basado en la web que ofrece Google. Hojas de cálculo de Google está disponible como aplicación web, aplicación móvil para Android, iOS, Windows, BlackBerry y como aplicación de escritorio en Chrome OS de Google. La aplicación es compatible con los formatos de archivo de Microsoft Excel. La aplicación permite a los usuarios crear y editar archivos en línea mientras colaboran con otros usuarios en tiempo real. Las ediciones son rastreadas por el usuario con un historial de revisión que presenta los cambios. La posición de un editor se resalta con un color y un cursor específicos del editor y un sistema de permisos regula lo que los usuarios pueden hacer. Las actualizaciones han introducido funciones que utilizan el aprendizaje automático que ofrece respuestas basadas en preguntas de lenguaje natural en una hoja de cálculo.

Referencia: https://es.wikipedia.org/wiki/Hojas_de_c%C3%A1lculo_de_Google

Componentes basicos de una hoja de cálculo: https://www.youtube.com/watch?v=w6MeASAl2Wc

**Ejercicio 1:** 
  1. Ir a Google Drive y abrir el archivo *\ProA2024\Testing_QA\Testing_Sheet_?????*.
  2. Renombrar la hoja actual "Hoja 1" a "Temas"
  3. En la hoja "Temas" armar la siguiente tabla:
     | Fecha | Clase n° | Eje | Tema | Actividad |
     |-------|----------|-----|------|-----------|
     | 2024-02-28 | 1 | 0 | Presentación | Presentación del espacio curricular |
     | 2024-03-04 | 2 | 2 | Trabajo Colaborativo | Uso de drive y google sheet |
  4. Poner en Negrita (CTRL+B) la primer Columna, poner en _cursiva_ (CTRL+I) la casilla 'E1'
  5. Hacer una grilla con bordes en el rango _A1:E80_ 
     
 **Ejercicio 2:** 
  1. Sobre el mismo documento *\ProA2024\Testing_QA\Testing_Sheet_?????*, crear una nueva Hoja (Hoja 2)
  2. Renombrar la hoja actual "Hoja 2" a  "Ejercicios"
  3. En la hoja "Ejercicios":
  4. Sobre la columna A, listar los números enteros desde 1 hasta el 1000
  5. Sobre las celda B1, obtener el resultado sumar 1 + 2 + 3 + ... + 1000
 
 **Ejercicio 3:**
  1. Crear una nuevo Hoja, renombrarla a Recibo
  2. Crear un tabla de recibo con las columnas Cantidad | Producto | Precio U. | SubTotal
  3. Hacer las suma de las columna Subtotal y mostrarla abajo en una casilla que se llame NETO TOTAL
  4. Hacer el cálculo del IVA sobre el NETO TOTAL y mostrarlo en una casilla que se llame TOTAL
  5. completar la tabla con 5 productos, con distintas cantidades y valores. Expresar los resultados en pesos.
 
 **Ejercicio 4:**
  1. Cree una nueva Hoja sobre el mismo archivo. y renombrarla a "notas".
  2. Haga un listado de nombres y notas (4 notas) y calcule la media de cada alumno.
     * copiar el listado nombres de: link lole
     * La media se puede calcular con la función =AVERAGE(XX:YY) o PROMEDIO(XX:YY) 
     * Y puede ser calculado tamabien sumando los valores y dividiendolo por la candidad de columnas  
 
 **Ejercicio 5:**
  1. Cree un nuevo archivo de Google Sheet llamadado _grafica de funciones_
  2. Abrirlo y renombrar la primer hoja a _funciones_.
  3. Crear en A1 una columna llamada **X** que tome valores de -10 a 10
  4. Crear en B1 una columna llamada **Y1** para almacenar los valores puntules de la función lineal `y = 3x -6` y graficar **x vs. y** , llamando a la gráfica _función lineal_
  5. Crear en C1 una columna llamada **Y2** para almacenar los valores puntules de la función cuadrática `y = x^2 - 4`  y graficar **x vs. y** , llamando a la gráfica _función cuadrática_
  6. Crear en D1 una columna llamada **Y3** para almacenar los valores puntules de la función cúbica `y = x^3 + X^2 -3X + 1`  y graficar **x vs. y** , llamando a la gráfica _función cúbica_ 
