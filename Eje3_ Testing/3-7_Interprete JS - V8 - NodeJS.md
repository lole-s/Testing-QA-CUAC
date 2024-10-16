https://ed.team/blog/lenguajes-de-programacion-compilados-vs-interpretados
https://ed.team/blog/que-son-los-lenguajes-tipados-y-no-tipados-explicacion-sencilla


historia de JS 
https://www.youtube.com/watch?v=ZGB_hQiI4ac


nodeJS
======

V8 
https://v8.dev/
https://nodejs.org/en/about

compilado - interpretado - tipado.
https://www.youtube.com/watch?v=M32Az-IRUQI
dark - https://www.youtube.com/watch?v=H46Z2aIVvqk

historia de JS 
https://www.youtube.com/watch?v=ZGB_hQiI4ac

-- no tipado -- dinámico
-- interpretado
-- es ideal para trabajar con interfases de usuario.


---interprete vs compilador

https://www.baumannzone.dev/blog/about-testing
https://www.baumannzone.dev/blog/testing-con-javascript

git clone https://github.com/baumannzone/javascript-testing


LABORATORIO DEVELOPERS
https://www.youtube.com/watch?v=gsTfbwfVvDE&list=PLiAEe0-R7u8kqvibxkK9tqqoJXnhgtefg&index=1
1 - 8 razones para aprender a hacer pruebas.
2 - que es un test? unitTEST. 


----------------------------------------------------------------------------------------------------
2024-10-14 UNIT TEST
###########################
a- ver video 1
https://www.youtube.com/watch?v=gsTfbwfVvDE&list=PLiAEe0-R7u8kqvibxkK9tqqoJXnhgtefg&index=1

b- ver video 2 -que es unit test

https://www.youtube.com/watch?v=PLBQjsKaCu4

c- instalar node.js
https://www.luisllamas.es/curso-nodejs/
https://kinsta.com/es/base-de-conocimiento/que-es-node-js/

----------------------------------------------------------------------------------------------------
2024-10-16 UNIT TEST
###########################

a - que es un modulo en node.js
https://www.luisllamas.es/curso-nodejs/
https://www.luisllamas.es/como-crear-ejecutar-script-nodejs/
 
b - ver video 1 -que es unit test
general    -  https://www.youtube.com/watch?v=wA_y-72rLs0
javaScript -  https://youtu.be/dra4iG_rMWk?si=UbNLPXWaHMFgAfTJ

c- crear un test unitario en node.js
assert: 
https://youtu.be/3KppxYQ-j6s?si=la6wmuZBuMNWwFDa
https://www.luisllamas.es/como-hacer-test-unitarios-nodejs/




===========================================================
e- instalar JETS
https://javascript.com.es/como-hacer-test-unitarios-en-javascript
...

--- 
___________________________________________________________________________________________________________
https://www.testim.io/blog/node-js-unit-testing-get-started-quickly-with-examples/
---

# installs fnm (Fast Node Manager)
winget install Schniz.fnm

# configure fnm environment
fnm env --use-on-cd | Out-String | Invoke-Expression

# download and install Node.js
fnm use --install-if-missing 20

# verifies the right Node.js version is in the environment
node -v # should print `v20.17.0`

# verifies the right npm version is in the environment
npm -v # should print `10.8.2`



---
https://www.freecodecamp.org/espanol/news/como-iniciar-la-prueba-unitaria-de-tu-codigo-javascript/

https://marceloandrader.github.io/blog/2021/03/23/parte-1-introducci%C3%B3n-a-pruebas-de-software/
---

============================

Un módulo en Node.js es simplemente un archivo JavaScript que exporta ciertas funcionalidades o datos para ser utilizados en otros archivos. Los módulos permiten estructurar tu código de manera más organizada y reutilizable.

Por ejemplo, puedes tener un módulo que exporte una función para verificar si un carácter es una vocal:

```javascript

// isVowel.js
const isVowel = (char) => {
    return 'aeiou'.includes(char.toLowerCase());
};

module.exports = isVowel;
```

Luego puedes importar y usar ese módulo en otro archivo:

```javascript

// main.js
const isVowel = require('./isVowel');

console.log(isVowel('a')); // true
console.log(isVowel('b')); // false
```

Los módulos permiten dividir la aplicación en partes más manejables y mantener el código limpio y fácil de mantener. 

Se pueden usar las expresiones 'import' y 'export' en lugar de 'require' y 'module.exports', en el ejemplo quedaría así:

En isVowel.js exportas la función:

```javascript

// isVowel.mjs
export const isVowel = (char) => {
    return 'aeiou'.includes(char.toLowerCase());
};
```

En main.js importas la función:


```javascript

// main.mjs
import { isVowel } from './isVowel';

console.log(isVowel('a')); // true
console.log(isVowel('b')); // false
```
En este caso necesario tener configurado un entorno que soporte módulos ES6, como un archivo de configuración de Babel o asegurarte de usar la extensión .mjs en los archivos. 


================
modulos por defecto para testing

assert: Es un módulo de Node.js que proporciona un conjunto simple de funciones de prueba de afirmaciones. Es útil para verificar valores esperados y lanzar errores cuando las afirmaciones no son verdaderas. Básicamente, te ayuda a asegurarte de que tu código está funcionando como debería al comparar resultados esperados con los resultados reales.

test: Es un módulo de Node.js que ofrece una manera más estructurada y avanzada de organizar y ejecutar pruebas. Permite definir y agrupar tests, proporcionando mayor flexibilidad y control sobre el proceso de pruebas unitarias.

Ambos son fundamentales para escribir y ejecutar pruebas en Node.js, ayudando a mantener el código libre de errores y garantizando que todo funcione como se espera.
================

Ejemplo de prueba unitaria en Node.js usando assert:

Supongamos que tienes una función que quieres probar en isVowel.mjs:

```javascript

// isVowel.mjs
export const isVowel = (char) => {
    return 'aeiou'.includes(char.toLowerCase());
};
```
Se crea un archivo de prueba, por ejemplo testIsVowel.mjs, que use assert:

```javascript

// testIsVowel.mjs
import assert from 'assert';
import { isVowel } from './isVowel.mjs';

// Prueba unitaria
assert.strictEqual(isVowel('a'), true, 'a es una vocal');
assert.strictEqual(isVowel('b'), false, 'b no es una vocal');

console.log('Todas las pruebas pasaron');
´´´

para correr el test, 

´´´ bash
node testIsVowel.mjs
```  

Si todas las aserciones (assert) son verdaderas, verás el mensaje "Todas las pruebas pasaron". Si alguna falla, se lanzará un error con el mensaje correspondiente. ¿Quieres profundizar más en las pruebas unitarias o en alguna otra cosa?


=================================
ejemplo con assert y test

Unit Test sobre función que suma dos números. Ejemplo:

```javascript

// sum.mjs
export const sum = (a, b) => {
    return a + b;
};
```

Ahora, el archivo de prueba testSum.mjs utilizando los módulos assert y test:

```javascript

// testSum.mjs
import assert from 'assert';
import { test } from 'node:test';
import { sum } from './sum.mjs';

// Prueba unitaria
test('Prueba de suma', () => {
    assert.strictEqual(sum(1, 2), 3, '1 + 2 debe ser igual a 3');
    assert.strictEqual(sum(-1, -1), -2, '-1 + -1 debe ser igual a -2');
    assert.strictEqual(sum(0, 0), 0, '0 + 0 debe ser igual a 0');
});

console.log('Todas las pruebas pasaron');

Para correr el test, usar el comando:

```bash
node testSum.mjs

```


______________
Supongamos que tienes un módulo de autenticación donde verificas las credenciales de un usuario. Necesitamos probar varios casos, como contraseñas correctas e incorrectas, nombres de usuario inexistentes, etc.

Módulo de autenticación en auth.mjs:

javascript

Copiar
// auth.mjs
const users = [
    { username: 'user1', password: 'password1' },
    { username: 'user2', password: 'password2' }
];

export const authenticate = (username, password) => {
    const user = users.find(u => u.username === username);
    if (user && user.password === password) {
        return true;
    }
    return false;
};
Archivo de pruebas avanzadas testAuth.mjs:

javascript

Copiar
// testAuth.mjs
import assert from 'assert';
import { test } from 'node:test';
import { authenticate } from './auth.mjs';

// Pruebas unitarias avanzadas
test('Prueba de autenticación con credenciales correctas', () => {
    assert.strictEqual(authenticate('user1', 'password1'), true, 'Las credenciales correctas deberían autenticar al usuario');
});

test('Prueba de autenticación con credenciales incorrectas', () => {
    assert.strictEqual(authenticate('user1', 'wrongpassword'), false, 'Las credenciales incorrectas no deberían autenticar al usuario');
});

test('Prueba de autenticación con usuario inexistente', () => {
    assert.strictEqual(authenticate('nonexistentUser', 'password'), false, 'Un usuario inexistente no debería ser autenticado');
});

test('Prueba de autenticación con campos vacíos', () => {
    assert.strictEqual(authenticate('', ''), false, 'Los campos vacíos no deberían autenticar a ningún usuario');
});

console.log('Todas las pruebas pasaron');
En esta actividad, te aseguras de que tu módulo de autenticación funcione correctamente para diferentes escenarios. ¡Prueba a ejecutarlo y cuéntame cómo te va! ¿Listo para el siguiente reto?




Usted
Me explicas que hace auth.mjs ?
Copilot
En auth.mjs, lo que estamos haciendo es simple pero clave para sistemas de autenticación básicos. Aquí hay un desglose:

Definición de usuarios:

javascript

Copiar
const users = [
    { username: 'user1', password: 'password1' },
    { username: 'user2', password: 'password2' }
];
Esta parte crea una lista de usuarios, cada uno con un nombre de usuario (username) y una contraseña (password).

Función de autenticación:

javascript

Copiar
export const authenticate = (username, password) => {
    const user = users.find(u => u.username === username);
    if (user && user.password === password) {
        return true;
    }
    return false;
};
Búsqueda de usuario: const user = users.find(u => u.username === username); Se busca un usuario en la lista cuyo nombre de usuario coincida con el proporcionado.

Verificación de contraseña: if (user && user.password === password) Si se encuentra el usuario y la contraseña proporcionada coincide con la almacenada, devuelve true, indicando una autenticación exitosa.

Resultado por defecto: return false; Si no se encuentra el usuario o la contraseña no coincide, devuelve false, indicando que la autenticación falló.

Básicamente, este módulo permite verificar si un par username/password es válido según una lista predefinida de usuarios
