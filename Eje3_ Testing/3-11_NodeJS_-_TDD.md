### TDD (Test-Driven Development)

Ahora que sabemos más sobre las pruebas unitarias, vamos a aprender una nueva forma de usarlas. Hasta ahora hemos escrito pruebas para verificar la funcionalidad del código existente . A continuación, vamos a utilizar pruebas para verificar la funcionalidad del código que NO existe. Puede parecer extraño, pero este proceso tiene muchos beneficios, como veremos a continuación.

Como su nombre indica, el desarrollo impulsado por pruebas (TDD, por sus siglas en inglés) es un proceso de desarrollo de software en el que primero se escriben las pruebas unitarias. Sin embargo, eso no lo explica todo. Escribir primero las pruebas y pensar más intencionalmente en el diseño del código conduce a un mejor código. El nombre proviene de la idea de que las pruebas impulsan el proceso de desarrollo.

Antes de poder comenzar a usar TDD, necesitamos una lista de características discretas que se puedan convertir en pruebas unitarias. Esto nos ayudará a mantener nuestras pruebas enfocadas en una funcionalidad específica que debería generar un código fácil de leer. A medida que vayamos agregando características, iremos ganando confianza.

#### Rojo, verde, refactorización 

Si bien el objetivo principal es agregar nuevas características y hacer que nuestro código funcione, también queremos escribir código legible y eficiente que nos enorgullezca. El mantra rojo, verde y refactorización describe el proceso de escribir pruebas, ver que pasan y luego mejorar el código. 

- Rojo -> Escribe una prueba fallida.
- Verde -> Hazlo pasar implementando el código.
- Refactorizar -> Mejorar el código.

<img src="https://github.com/user-attachments/assets/319fbd81-2cda-438c-a557-bfb32620f4cc" alt="Descripción alternativa de la imagen" width="300" height="200">

**Refactorizar código** significa mantener la misma característica general, pero cambiar la forma en que se implementa esa característica. Dado que tenemos una prueba para verificar nuestro código, podemos cambiar el código con confianza, sabiendo que la prueba identificará inmediatamente cualquier error. A continuación, se muestran algunos ejemplos de refactorización:

  1. Utilizando diferentes estructuras de datos,
  2. Reducir la cantidad de veces que es necesario recorrer una matriz,
  3. Convertir la lógica duplicada en una función para que pueda reutilizarse.

La refactorización también se realiza en un proceso TDD:
  
  1. Decidir cómo mejorar la implementación de la función,
  2. Cambie la prueba unitaria para utilizar esta nueva idea,
  3. Ejecute el código para ver si la prueba falla.
  4. Refactorizar el código para implementar la nueva idea,
  5. Finalmente, vea la prueba aprobada con el diseño refactorizado.
_____________________________

#### Ejemplo 1:  TDD con NodeJs y Jasmine

Supongamos que se nos solicita escribir un modulo Js que verifique su un número es primo. 

A partir de la solicitud podriamos pensar los siguientes requisitos discretos 

Requisitos Discretos

1- Entrada Válida: La función debe aceptar solo un número entero como entrada. Caso contrario retornar 'false'.

2- Comprobación de números menores o iguales a 1: La función debe retornar false para cualquier número menor o igual a 1, ya que no son primos.

3- Comprobación de divisibilidad: La función debe verificar si el número es divisible por algún número entero mayor que 1 y menor que él mismo. Si se encuentra un divisor (aparte de 1 y el mismo número), debe retornar false.

  Caso contrario: Si no se encuentra ningún divisor, la función debe retornar true.


##### Paso 1: Escribir una prueba (Red)

Vamos a escribir las pruebas para una función (que aún No existe) que valide si un número es primo. Creamos  un archivo llamado *prime.spec.js* en el directorio *spec* y agregamos las siguientes pruebas:

```javascript
const isPrime = require('../isPrime.js');
 
describe('isPrime', () => {

  it('should return false for non-number inputs', () => {
    expect(isPrime('seven')).toBe(false);
    expect(isPrime(null)).toBe(false);
    expect(isPrime(undefined)).toBe(false);
  });

  it('should return false for non-integer numbers', () => {
    expect(isPrime(2.5)).toBe(false);
    expect(isPrime(3.1)).toBe(false);
  });

  it('should return false for numbers less than or equal to 1', () => {
    expect(isPrime(0)).toBe(false);
    expect(isPrime(1)).toBe(false);
    expect(isPrime(-5)).toBe(false);
  });

  it('should return false for non-prime numbers', () => {
    expect(isPrime(4)).toBe(false);
    expect(isPrime(6)).toBe(false);
    expect(isPrime(9)).toBe(false);
  });

  it('should return true for prime numbers', () => {
    expect(isPrime(2)).toBe(true);
    expect(isPrime(3)).toBe(true);
    expect(isPrime(5)).toBe(true);
    expect(isPrime(7)).toBe(true);
  });
});
```
##### Paso 2: Escribir el código mínimo (Green)

Crea un archivo prime.js en el directorio raíz del proyecto y agrega la siguiente función:

```javascript

function isPrime(num) {
  if (!Number.isInteger(num) || num <= 1) return false;
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
  if (!Number.isInteger(num) || num <= 1) return false;
  for (let i = 2, sqrt = Math.sqrt(num); i <= sqrt; i++) {
    if (num % i === 0) return false;
  }
  return true;
}

module.exports = isPrime;
```

#### Ejemplo 2: TDD con NodeJs y Jasmine

Ahora veamos, en el siguiente link, un ejemplo un poco mas realista de diseño de una función  basada en TDD usando NodeJs y Jasmine.

(TDD en Acción)[https://education.launchcode.org/intro-to-professional-web-dev/chapters/unit-testing/tdd-example.html] 
