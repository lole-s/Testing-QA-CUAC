### (Lenguajes de programación interpretados vs compilados: ¿Cuál es la diferencia?)[https://www.freecodecamp.org/espanol/news/lenguajes-compilados-vs-interpretados/]!

Cada programa es un conjunto de instrucciones, ya sea sumar dos números o enviar una petición a través de internet. Los compiladores e intérpretes toman código legible por los humanos y lo convierten en código máquina legible por computadoras.

En un lenguaje compilado, la máquina de destino traduce directamente el programa. En un lenguaje interpretado, el código fuente no es directamente traducido por la máquina de destino. En cambio, un distinto programa, mejor conocido como intérprete, lee el código y lo ejecuta.

Okay… ¿Pero qué significa eso realmente?
Imagina que tienes una receta de hummus y la quieres preparar, pero está escrita en griego antiguo. Hay dos maneras en que tú, alguien que no habla griego antiguo, podrías seguir dichas instrucciones.

La primera es si alguien ya lo ha traducido al español para ti. Tú (y cualquiera que hable el idioma) podrías leer la versión en español de la receta y hacer el hummus. Piensa en esta receta traducida como la versión compilada.

La segunda manera es si tienes un amigo que sabe griego antiguo. Cuando estés listo para hacer hummus, tu amigo se sienta junto a ti y traduce la receta al español mientras avanzas, línea por línea. En este caso, tu amigo es el intérprete de la versión interpretada de la receta.

Lenguajes compilados
Los lenguajes compilados son convertidos directamente a código máquina que el procesador puede ejecutar. Como resultado, suelen ser más rápidos y más eficientes al ejecutarse en comparación con los lenguajes interpretados. También le dan al desarrollador más control sobre aspectos del hardware, como la gestión de memoria y el uso del CPU.

Los lenguajes compilados necesitan un paso de compilación (build) - primero necesitan compilarse manualmente. Necesitas "recompilar" el programa cada vez que necesites hacer un cambio. En nuestro ejemplo del hummus, la traducción completa está escrita antes de que la tengas. Si el autor original decide que quiere usar un distinto aceite de oliva, toda la receta necesitaría ser traducida de nuevo y reenviada a ti.

Algunos ejemplos de lenguajes compilados puros son C, C++, Erlang, Haskell, Rust y Go.

Lenguajes interpretados
Estos lenguajes ejecutan línea por línea el programa y a la vez ejecutan cada comando. Aquí, si el autor decide que quiere usar un distinto aceite de oliva, podría borrar el anterior y agregar el nuevo. Tu amigo traductor puede decirte ese cambio a medida que sucede.

Los lenguajes interpretados alguna vez fueron significativamente más lentos que los lenguajes compilados. Pero, con el desarrollo de la compilación justo a tiempo, esa diferencia se está reduciendo.

Ejemplos comunes de lenguajes interpretados son PHP, Ruby, Python y JavaScript.

Una pequeña advertencia
La mayoría de lenguajes de programación pueden tener implementaciones tanto compiladas como interpretadas, el lenguaje en sí mismo no es necesariamente compilado o interpretado. Sin embargo, por cuestiones de simplicidad, normalmente se les conoce de tal manera.

Python, por ejemplo, puede ser ejecutado ya sea como programa compilado o como un lenguaje interpretado en modo interactivo. Por el otro lado, la mayoría de las herramientas de línea de comandos, CLIs y shells pueden ser teóricamente clasificadas como lenguajes interpretados.

Ventajas y desventajas
Ventajas de los lenguajes compilados
Los programas que son compilados a un código máquina nativo suelen ser más rápidos que los lenguajes interpretados. Esto es debido a que el proceso de traducción del código en tiempo de ejecución aumenta la sobrecarga y puede ocasionar que el programa sea más lento en general.

Desventajas de los lenguajes compilados
Las desventajas más notables son:

Tiempo extra necesario para completar la compilación completa antes de la prueba
Dependencia de la plataforma del código binario generado
Ventajas de los lenguajes interpretados
Los lenguajes interpretados suelen ser más flexibles, y a menudo ofrecen características como escritura dinámica y tamaño de programa más pequeño. Además, ya que los intérpretes ejecutan el código fuente del programa ellos mismos, el código en sí es independiente de la plataforma.

Desventajas de los lenguajes interpretados
La desventaja más notable es la velocidad de ejecución típica comparada con los lenguajes compilados.
