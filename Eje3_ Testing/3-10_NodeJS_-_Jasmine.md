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
en este archivo escribiremos nuestros casos de pruebe Positívos, Negativos y casos de borde (o de extremos) 

nota: ver estos casos en link de la parte superior de esta página. 

- Ejecutar las pruebas:

```bash
npx jasmine
```
Jasmine ejecutará las pruebas y las mostrará los resultados en la terminal.