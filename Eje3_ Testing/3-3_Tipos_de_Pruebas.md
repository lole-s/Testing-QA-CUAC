## Tipos de pruebas de Software

El tipo de prueba de software depende de la forma en que se aplica y lo que desea verificar.

#### De acuerdo a su ejecución existen:

1. Pruebas **manuales** de software

El probador lleva a cabo los casos de prueba sin ayuda de alguna herramienta automática. Su tarea es hacer clic en la aplicación e interactuar con el software y con la interfaz de programación de aplicaciones (API por sus siglas en inglés).

Este tipo de pruebas resultan muy costosas debido a que necesita que alguien configure un entorno para la ejecución de las pruebas. También están propensas a sufrir errores humanos como que el tester (el probador o pentester) añada erratas u omita pasos en el script de la prueba. 

Por consiguiente, en las pruebas manuales de software se establecen pasos específicos a seguir y los resultados que se esperan obtener. Se requiere de conocimiento profundo, experiencia, habilidades analíticas y lógicas. 

2. Pruebas **automatizadas** de software

Se hacen mediante un software que ejecuta un script de prueba que se escribió con anticipación. Su complejidad varía: puede usarse para comprobar el único método de una clase o que se consiguen los mismos resultados con una secuencia de acciones complejas en la interfaz. 

Con la automatización de pruebas se obtienen resultados más precisos y confiables que con las manuales, pero su calidad está relacionada con lo bien que se hayan escrito los scripts de las pruebas. Además, es una excelente forma de escalar en el proceso de control de calidad, ya que puedes añadir nuevas funciones a tu aplicación. 

Además, se realizan tareas repetitivas y pruebas de regresión. Sin embargo, sigue siendo útil hacer algunas pruebas manuales mediante las llamadas pruebas exploratorias. 

#### De acuerdo con lo que verifican están:

1. Pruebas **funcionales**

      Se utilizan para garantizar que las características y funcionalidades del software se comportan según lo esperado. Son consideradas pruebas de caja negra porque validan que toda la aplicación esté acorde con las especificaciones mencionadas en el documento Software Requirement Specification (SRS). Los tipos de pruebas funcionales se dividen en: 

- Pruebas unitarias

     Son las primeras pruebas que se hacen durante la fase de desarrollo de software. Consisten en probar las piezas o unidades de la aplicación de software al principio del ciclo de vida de desarrollo (SDLC).

     Estas pruebas unitarias se hacen a cualquier función, método, procedimiento o módulo para determinar si hay algo que debe corregirse y cuál es el comportamiento esperado. 

- Pruebas de integración

    Verifican si los diferentes componentes, módulos o funciones de un sistema de software pueden operar como grupo o conjunto. Gracias a las pruebas de integración se pueden identificar los errores y problemas que surgen, por ejemplo, durante la interacción con la base de datos para resolverlos a tiempo. 

- Pruebas de sistema

     El probador utiliza varios casos de prueba para comprobar el cumplimiento del software integrado y las especificaciones. También evalúa el nivel de seguridad del sistema, la resistencia ante situaciones anormales y las pruebas de recuperación. 

2. Pruebas **no funcionales**

      Se realizan para mejorar la experiencia de usuario. Toman en cuenta el rendimiento de los observadores, la usabilidad, fiabilidad, escalabilidad, entre otros. Por lo general, usan herramientas y soluciones de automatización. Entre los diferentes tipos de pruebas no funcionales se encuentran:

- Prueba de rendimiento

     Durante el proceso de prueba se evalúa el desempeño o la velocidad de la aplicación bajo una carga de trabajo específica. Puede analizar los tiempos de respuesta a las solicitudes, la escalabilidad, velocidad y fiabilidad. Además, determina si la aplicación cumple con los requisitos, sobre todo durante los picos de tráfico, e identifica los cuellos de botella. 

- Prueba de carga

     Analiza el comportamiento del software bajo grandes cargas de trabajo. En el caso de un sitio web, por ejemplo, se evalúa la funcionalidad de la página y el rendimiento durante un tráfico alto.

- Prueba de seguridad

     Se revisa si el sistema de software está seguro en caso de sufrir ciberataques súbitos y deliberados, tanto de origen externo o interno. Esta prueba de seguridad garantiza que el software está libre de amenazas, vulnerabilidades, y riesgos que puedan causar un gran daño por pérdida de datos a una empresa. También verifica que los datos y recursos están protegidos en caso de ciberespionaje. 

- Prueba de compatibilidad

     Se prueba si el software es compatible con entornos cambiantes. Por ejemplo, si una aplicación web trabaja correctamente en diferentes buscadores o dispositivos. 

     Esta prueba también permite evaluar cómo funciona una aplicación móvil en condiciones distintas, diferentes tipos de dispositivos, según el alcance de red, el navegador usado, la resolución de pantalla y el sistema operativo.

- Prueba de confiabilidad

     También es conocida como reliability testing. En ella se evalúa el desempeño de una aplicación, durante una tarea específica y dentro de un periodo de tiempo determinado. Esto permitirá conocer si la aplicación se ejecuta bien con acciones específicas. 

- Prueba de usabilidad

     En esta prueba se examina la facilidad de uso por parte del usuario final, la forma en que interactúa con un producto o sistema y el aprendizaje durante la operatividad del mismo. Puede hacerse de manera remota o personal.

     Gracias a este tipo de prueba de software se pueden identificar los problemas y mejorar la experiencia de usuario. 

#### También existen otros niveles de prueba que se pueden realizar durante el proceso de desarrollo del software:

1. Pruebas de humo

      Sirven para comprobar el funcionamiento básico de una aplicación. Se ejecutan de forma rápida, con el objetivo de brindar la seguridad de que las principales funciones se llevan a cabo según lo previsto. 

      Este tipo de pruebas son útiles si se hacen después de una compilación nueva, ya que ayuda a decidir si se ejecutan o no pruebas más caras, o inmediatamente después de una implementación para comprobar si funciona. 

3. Pruebas de estrés

      Se ejecutan antes de dar por finalizado el proceso de desarrollo de software para comprobar cuánta tensión puede soportar antes de que ocurra un error. En esta prueba se envía más información de la habitual para determinar en qué momento se satura el sistema. 

5. Pruebas de aceptación

      Verifican si el sistema satisface los requisitos empresariales y funciona según lo previsto. Si durante la fase de desarrollo de la prueba se toman decisiones que agreguen o disminuyan criterios de aceptación, el probador debe dejar constancia. En este tipo de pruebas se ejecuta toda la aplicación y se replican las conductas de los usuarios.


#### Importancia y beneficios de las pruebas de software

###### Aunque las pruebas de software tienen un costo adicional al desarrollo y mantenimiento del mismo, son altamente recomendadas para evitar errores, demoras y fallas en el sistema. De esta manera, darás la mejor imagen posible de la marca al cliente e información objetiva sobre la calidad del producto.

###### Hacer pruebas antes del lanzamiento al mercado te ahorrará tiempo, reducirá a mediano y largo plazo los costos de desarrollo por algún problema no detectado previamente y evitará la pérdida de clientes.

##### Mediante las pruebas, el equipo de desarrollo podrá abordar problemas como:

+ Defectos arquitectónicos
+ Malas decisiones de diseño
+ Funcionalidad no válida o incorrecta
+ Vulnerabilidades de seguridad
+ Problemas de escalabilidad
+ Mala calidad del software

_Un software que funcione a la perfección y cumpla con las expectativas de la empresa y los usuarios, hará más fácil la participación en el mercado y el proceso de captación de clientes potenciales._

<!-- https://www.deltaprotect.com/blog/tipos-de-pruebas-de-software-que-son-y-como-funcionan -->
