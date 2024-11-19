### TDD (Test-Driven Development)

Ahora que sabemos más sobre las pruebas unitarias, vamos a aprender una nueva forma de usarlas. Hasta ahora hemos escrito pruebas para verificar la funcionalidad del código existente . A continuación, vamos a utilizar pruebas para verificar la funcionalidad del código que NO existe. Puede parecer extraño, pero este proceso tiene muchos beneficios, como veremos a continuación.

Como su nombre indica, el desarrollo impulsado por pruebas (TDD, por sus siglas en inglés) es un proceso de desarrollo de software en el que primero se escriben las pruebas unitarias. Sin embargo, eso no lo explica todo. Escribir primero las pruebas y pensar más intencionalmente en el diseño del código conduce a un mejor código. El nombre proviene de la idea de que las pruebas impulsan el proceso de desarrollo.

Antes de poder comenzar a usar TDD, necesitamos una lista de características discretas que se puedan convertir en pruebas unitarias. Esto nos ayudará a mantener nuestras pruebas enfocadas en una funcionalidad específica que debería generar un código fácil de leer. A medida que vayamos agregando características, iremos ganando confianza.

#### Rojo, verde, refactorización 

Si bien el objetivo principal es agregar nuevas características y hacer que nuestro código funcione, también queremos escribir código legible y eficiente que nos enorgullezca. El mantra rojo, verde y refactorización describe el proceso de escribir pruebas, ver que pasan y luego mejorar el código. 

- Rojo -> Escribe una prueba fallida.
- Verde -> Hazlo pasar implementando el código.
- Refactorizar -> Mejorar el código.

Gráfico que muestra el ciclo de fases desde el rojo para escribir la prueba, el verde para aprobar la prueba y el azul para refactorizar el código para mejorarlo, lo que apunta nuevamente al rojo.
, verde, ciclo de refactorización.

Refactorizar código significa mantener la misma característica general, pero cambiar la forma en que se implementa esa característica. Dado que tenemos una prueba para verificar nuestro código, podemos cambiar el código con confianza, sabiendo que la prueba identificará inmediatamente cualquier error. A continuación, se muestran algunos ejemplos de refactorización:

Utilizando diferentes estructuras de datos,

Reducir la cantidad de veces que es necesario recorrer una matriz,

Mover lógica duplicada a una función para que pueda reutilizarse.

La refactorización también se realiza en un proceso TDD:

Decidir cómo mejorar la implementación de la función,

Cambie la prueba unitaria para utilizar esta nueva idea,

Ejecute el código para ver si la prueba falla.

Refactorizar el código para implementar la nueva idea,

Finalmente, vea la prueba aprobada con el diseño refactorizado.
---
Desarrollo guiado por pruebas (TDD) es una metodología de desarrollo de software en la que las pruebas se escriben antes del código que se necesita para pasar esas pruebas. Esta técnica sigue tres etapas principales, conocidas como el ciclo "Red-Green-Refactor":

  1. Red: Escribir una prueba que fallará porque el código necesario aún no existe.
  2. Green: Escribir el código mínimo necesario para que la prueba pase.
  3. Refactor: Refactorizar el código para mejorarlo sin cambiar su comportamiento.

Principales Motivos de TDD

- **Mejor Diseño del Código**: TDD promueve la creación de código limpio y bien estructurado desde el principio.
- **Menos Errores**: Al escribir pruebas antes que el código, los errores se identifican y corrigen rápidamente.
- **Documentación Viviente**: Las pruebas actúan como documentación, mostrando claramente lo que hace cada parte del código.
- **Confianza al Refactorizar**: Las pruebas aseguran que las modificaciones no rompan el código existente.
- **Mayor Mantenibilidad**: Un código bien probado es más fácil de mantener y extender en el futuro.

#### Ejemplo TDD con NodeJs y Jasmine

##### Paso 1: Escribir una prueba (Red)
Vamos a escribir una prueba para una función que valide si un número es primo. Crea un archivo llamado prime.spec.js en el directorio spec y agrega la siguiente prueba:

```javascript
const isPrime = require('../prime');

describe('isPrime', () => {
  //caso positivo
  it('should return true for a prime number', () => {
    expect(isPrime(7)).toBe(true);
  });
  //caso negativo
  it('should return false for a non-prime number', () => {
    expect(isPrime(4)).toBe(false);
  });
  //caso de borde
  it('should return false for numbers less than 2', () => {
    expect(isPrime(1)).toBe(false);
    expect(isPrime(0)).toBe(false);
    expect(isPrime(-1)).toBe(false);
  });
});
```
##### Paso 2: Escribir el código mínimo (Green)

Crea un archivo prime.js en el directorio raíz del proyecto y agrega la siguiente función:

```javascript

function isPrime(num) {
  if (num <= 1) return false;
  for (let i = 2; i < num; i++) {
    if (num % i === 0) return false;
  }
  return true;
}

module.exports = isPrime;
```
##### Paso 3: Ejecutar la prueba

Corre Jasmine para ver si la prueba pasa. Si la prueba pasa, el código está correcto.

#### Paso 4: Refactorizar el código (Refactor)

Podemos mejorar la eficiencia de la función isPrime verificando solo hasta la raíz cuadrada del número:

```javascript
function isPrime(num) {
  if (num <= 1) return false;
  for (let i = 2, sqrt = Math.sqrt(num); i <= sqrt; i++) {
    if (num % i === 0) return false;
  }
  return true;
}

module.exports = isPrime;
```

#### Ejercicio TDD con NodeJs y Jasmine: Reversa de Palabras en una Frase 

Para practicar la metodología de desarrollo TDD, intentemos crear una función para la manipulación de cadenas de texto 
que cumpla con los siguientes requisitos: 


Descripción
Escribe una función que tome una frase como entrada y devuelva la misma frase con las palabras en orden inverso.

Paso 1: Escribir una prueba (Red)
Crea un archivo llamado reverseWords.spec.js en el directorio spec y agrega la siguiente prueba:

javascript
const reverseWords = require('../reverseWords');

describe('reverseWords', () => {
  it('should reverse the words in a sentence', () => {
    expect(reverseWords('hello world')).toBe('world hello');
  });

  it('should handle an empty string', () => {
    expect(reverseWords('')).toBe('');
  });

  it('should handle a single word', () => {
    expect(reverseWords('hello')).toBe('hello');
  });

  it('should handle multiple spaces between words', () => {
    expect(reverseWords('hello   world')).toBe('world   hello');
  });
});
Paso 2: Escribir el código mínimo (Green)
Crea un archivo reverseWords.js en el directorio raíz del proyecto y agrega la siguiente función:

javascript
function reverseWords(sentence) {
  return sentence.split(' ').reverse().join(' ');
}

module.exports = reverseWords;
Paso 3: Ejecutar la prueba
Corre Jasmine para ver si las pruebas pasan. Si las pruebas pasan, el código está correcto.

Paso 4: Refactorizar el código (Refactor)
En este caso, el código ya es bastante simple y eficiente. Sin embargo, podrías refactorizarlo para manejar posibles espacios en blanco al principio y al final de la frase:

javascript
function reverseWords(sentence) {
  return sentence.trim().split(/\s+/).reverse().join(' ');
}

module.exports = reverseWords;
Ejercicio Adicional
Para practicar más, intenta lo siguiente:

Agregar una prueba para convertir una cadena a camelCase.

Implementar la función que convierta una cadena a camelCase.

Refactorizar el código si es necesario.

Este ejercicio te permitirá profundizar en las técnicas de TDD y mejorar tus habilidades de manipulación de cadenas con NodeJs y Jasmine. ¡Espero que te resulte útil! 🚀

que es camelcase?
CamelCase es una convención de escritura en la que las palabras se concatenan sin espacios y cada palabra comienza con una letra mayúscula. Es comúnmente utilizada en programación para nombrar variables, funciones y clases. Hay dos variantes principales:

UpperCamelCase (o PascalCase): La primera letra de cada palabra, incluida la primera palabra, está en mayúscula. Ejemplo: ThisIsAnExample.

lowerCamelCase: La primera letra de la primera palabra está en minúscula, y la primera letra de cada palabra subsiguiente está en mayúscula. Ejemplo: thisIsAnExample.

El uso de CamelCase ayuda a mejorar la legibilidad del código al separar claramente las palabras en un identificador. ¿Te gustaría un ejemplo de cómo se usa en el código?


fuente: https://education.launchcode.org/intro-to-professional-web-dev/chapters/unit-testing/tdd.html
