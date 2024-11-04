https://education.launchcode.org/intro-to-professional-web-dev/chapters/unit-testing/index.html

## JASMINE

Jasmine es un framework que proporciona una estructura específica y una colección de herramientas para escribir y ejecutar pruebas de JavaScript. No es solo una librería; establece convenciones y patrones que facilitan la organización y ejecución de tests. Permitiendo definir pruebas, expectativas y aserciones, funcionando como una solución completa para las pruebas unitarias.

Jasmine es conocida por ser fácil de usar y no requiere dependencias adicionales, es ideal para asegurarte de que el código no tenga errores.

### Creación de Carpeta para prueba de framework Jasmine

Antes de comenzar con la instalción del framework Jasmine verifucalemos las version de npm que tenemos instalada: 

```bash
npm -v 
```
NOTA: npm (Node Package Manager) es una herramienta que viene con Node.js y se usa para gestionar paquetes (librerías y módulos) en proyectos de JavaScript. Te permite instalar, actualizar y desinstalar paquetes, así como manejar dependencias de tu proyecto

Luego, creamos una carpeta para nuestra práctica en `c:\temp\` llamadas `palindrome`

```bash 
cd /c/temp/
mkdir palindrome
cd palindrome
```

y creamos el archivo con la función que queremos probary lo editamos: 

```bash 
touch palindrome.js
vim palindrome.js
```
la función tiene la sig. lógica: 

```javascript
function reverse(str) {
  return str.split('').reverse().join('');
}

function isPalindrome(str) {
  return reverse(str) === str;
}

module.exports = isPalindrome;
```

## Instalar Jasmine 

Instalar Jasmine y ejecutar pruebas es bastante sencillo. Aquí tienes los pasos:

- Instalar Jasmine localmente:

Primero, navega al directorio del proyecto en la terminal y ejecuta:

```bash
npm install --save-dev jasmine
```
- Inicializar Jasmine:

Luego, inicializa Jasmine en el proyecto:

```bash
npx jasmine init
```
Esto creará una estructura de carpetas y archivos de configuración para Jasmine.
```bash
ls -alh
ls -alh ./node_modules/
```

Para listar los paquetes globales hacemos:

```bash
npm list -g --depth=0
```
y para los listarar los paquetes locales

```bash
npm list --depth=0
```

Escribir una prueba:

Crea un archivo de prueba en el directorio `spec` (creado por Jasmine):

```bash
cd spec/
touch palindrome.spec.js
vim palindrome.spec.js
```

En este archivo escribiremos nuestros casos de pruebe Positívos, Negativos y casos de borde (o de extremos) 

- Ejecutar las pruebas:

```bash
npx jasmine
```
Jasmine ejecutará las pruebas y las mostrará los resultados en la terminal.
___
### Actividad 1: 
1- Agregar en spec/palindrome.spec.js los casos de prueba los [casos de prueba positivos](https://education.launchcode.org/intro-to-professional-web-dev/chapters/unit-testing/unit-testing-in-action.html#positive-test-cases) y luego ejecutar jasmine desde el terminal 
```bash
npx jasmine
```
2- Añadir en spec/palindrome.spec.js los casos de prueba los [casos de prueba negativos](https://education.launchcode.org/intro-to-professional-web-dev/chapters/unit-testing/unit-testing-in-action.html#negative-test-cases) y luego ejecutar jasmine desde el terminal 
```bash
npx jasmine
```
3- Añadir en spec/palindrome.spec.js los casos de prueba los [casos de prueba de borde](https://education.launchcode.org/intro-to-professional-web-dev/chapters/unit-testing/unit-testing-in-action.html#edge-cases) y luego ejecutar jasmine desde el terminal 
```bash
npx jasmine
```
____

## Como funciona la función isPalindrome() ?.

La función `isPalindrome(str)` invoca a `reverse(str)`  y luego compara dos string, retornando `true` en caso que sean estrictamente iguales.

```javascript

function isPalindrome(str) {
  const cleanedStr = str.toLowerCase().replace(/\s+/g, '');
  return reverse(cleanedStr) === cleanedStr;
}
```

La función  `reverse(str)` toma una cadena de texto (str) y la devuelve invertida.

```javascript
function reverse(str) {
   return str.split('').reverse().join('');
}
```

Vamos a desglosarlo paso a paso con la cadena "hola":

1- str.split(''): Divide la cadena en un array de caracteres.
```javascript
"hola".split('')
```
Salida: ['h', 'o', 'l', 'a']

2- reverse(): Invierte el orden de los elementos del array.
```javascript
['h', 'o', 'l', 'a'].reverse()
```
Salida: ['a', 'l', 'o', 'h']

3- join(''): Junta los caracteres del array nuevamente en una cadena de texto.
```javascript
['a', 'l', 'o', 'h'].join('')
```
Salida: "aloh"

Así, al final del proceso, la función convierte "hola" en "aloh"
___

### Actividad 2: 

1. Supongamos que actualizamos isPalindrome() para que no distinga entre mayúsculas y minúsculas ( por ejemplo, isPalindrome('Radar') devuelve true ).

  - ¿Cuál de los siguientes es un ejemplo de caso de prueba positivo de isPalindrome() para verificar si no distingue entre   mayúsculas y minúsculas?
```  
  a- aa
  b- aBa
  c- Mom
  d- Taco Cat
  c- AbAb
```
  - ¿Cuáles de los casos de prueba negativos enumerados anteriormente ya no son válidos para nuestro sistema que no       distingue entre mayúsculas y minúsculas isPalindrome?

```
 a- ab
 b- launchcode
 c- abA
 d- so many dynamos
```

2. Modificar la función `isPalindrome(str)` para que no distinga entre mayusculas y minusculas y no tenga cuenta los espacios en blanco. De modo que por ejemplo:  _Anita lava la tina_ devuelva true.
   
3. Modificar los casos de prueba de acuerdo al nuevo requerimiento de modo que la ejecutación de Jasmine quede libre de errores.
   
