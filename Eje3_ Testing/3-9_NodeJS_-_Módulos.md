## Módulos 

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

// isVowel.spec.js
const isVowel = require('./isVowel');

console.log(isVowel('a')); // true
console.log(isVowel('b')); // false
```

Los módulos permiten dividir la aplicación en partes más manejables y mantener el código limpio y fácil de mantener. 

Se pueden usar las expresiones 'import' y 'export' en lugar de 'require' y 'module.exports', en el ejemplo quedaría así:

En isVowel.mjs exportas la función:

```javascript

// isVowel.mjs
export function isVowel(char) {
    return 'aeiou'.includes(char.toLowerCase());
}
```

En isVowel.spec.mjs importas la función:

```javascript

// isVowel.spec.mjs
import { isVowel } from './isVowel';

console.log(isVowel('a')); // true
console.log(isVowel('b')); // false
```

En este caso necesario tener configurado un entorno que soporte módulos ES6 o asegurarte de usar la extensión .mjs en los archivos. 


___________________

### Módulos (para testing) intergrados en Node.JS

ASSERT: Es un módulo de Node.js que proporciona un conjunto simple de funciones de prueba de afirmaciones. Es útil para verificar valores esperados y lanzar errores cuando las afirmaciones no son verdaderas. Básicamente, te ayuda a asegurarte de que tu código está funcionando como debería al comparar resultados esperados con los resultados reales.

TEST: Es un módulo de Node.js que ofrece una manera más estructurada y avanzada de organizar y ejecutar pruebas. Permite definir y agrupar tests, proporcionando mayor flexibilidad y control sobre el proceso de pruebas unitarias.

Ambos son fundamentales para escribir y ejecutar pruebas en Node.js, ayudando a mantener el código libre de errores y garantizando que todo funcione como se espera.

________________

#### Ejemplo de prueba unitaria en Node.js usando assert:

Supongamos que tienes una función que quieres probar en isVowel.mjs:

```javascript

// isVowel.mjs
export const isVowel = (char) => {
    return 'aeiou'.includes(char.toLowerCase());
};
```
Se crea un archivo de prueba, por ejemplo testIsVowel.mjs, que use assert:

```javascript

// isVowel.spec.mjs
import assert from 'assert';
import { isVowel } from './isVowel.mjs';

// Prueba unitaria
assert.strictEqual(isVowel('a'), true, 'a es una vocal');
assert.strictEqual(isVowel('b'), false, 'b no es una vocal');

console.log('Todas las pruebas pasaron');
```
para correr el test, 

``` bash
node isVowel.spec.mjs
```  

Si todas las aserciones (assert) son verdaderas, verás el mensaje "Todas las pruebas pasaron". 

__________________

### Ejemplo con assert y test

Unit Test sobre función que suma dos números. Ejemplo:

```javascript

// sum.mjs
export const sum = (a, b) => {
    return a + b;
};
```

Ahora, el archivo de prueba testSum.mjs utilizando los módulos assert y test:

```javascript

// sum.spec.mjs
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
```

Para correr el test, usar el comando:

```bash
node sum.spec.mjs

```
______________

### Ejemplo de Unit Test sobre función Autenticación 

Supongamos que tienes un módulo de autenticación donde verificas las credenciales de un usuario. Necesitamos probar varios casos, como contraseñas correctas e incorrectas, nombres de usuario inexistentes, etc.

Módulo de autenticación en auth.mjs:

```javascript

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

```

Archivo de pruebas auth.spec.mjs:

```javascript

// auth.spec.mjs
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
    assert.strictEqual(authenticate('nonexistentUser', 'password1'), false, 'Un usuario inexistente no debería ser autenticado');
});

test('Prueba de autenticación con campos vacíos', () => {
    assert.strictEqual(authenticate('', ''), false, 'Los campos vacíos no deberían autenticar a ningún usuario');
});

test('Prueba de autenticación con credenciales incorrectas (cambiadas) ', () => {
    assert.strictEqual(authenticate('user1', 'password2'), false, 'Las credenciales incorrectas no deberían autenticar al usuario');
});

console.log('Todas las pruebas pasaron');
```

Esta test asegura que el módulo de autenticación funcione correctamente para diferentes escenarios. 


<!--
lista de usuarios, cada uno con un nombre de usuario (username) y una contraseña (password).

const users = [    
    { username: 'user1', password: 'password1' },
    { username: 'user2', password: 'password2' }
];

    
función de autenticación:

export const authenticate = (username, password) => {
    const user = users.find(u => u.username === username);
    if (user && user.password === password) {
        return true;
    }
    return false;
};

- Búsqueda de usuario: 
    - const user = users.find(u => u.username === username); 

Se busca un usuario en la lista cuyo nombre de usuario coincida con el proporcionado.

- Verificación de contraseña: 
    - if (user && user.password === password) 

Si se encuentra el usuario y la contraseña proporcionada coincide con la almacenada, devuelve true, indicando una autenticación exitosa.

Resultado por defecto: 
    - return false; 
    Si no se encuentra el usuario o la contraseña no coincide, devuelve false, indicando que la autenticación falló.

Básicamente, este módulo permite verificar si un par username/password es válido según una lista predefinida de usuarios.
-->
