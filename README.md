# JavaScript Esencial

Se crea este repositoria para subir las practicas del curso JavaScript Esencial

[Contacto](https://www.facebook.com/yeco13)

---

### Primer JavaScript - Hola Mundo!!

1. Se crea hola mundo desde archivo practicas/index.html

```html
<html lang="es" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>JavaScript Esencial</title>
  </head>
  <body>
    <script>
      alert('Hola Mundo!!');
    </script>
  </body>
</html>
```
### Elementos basicos de JavaScript

##### JavaScript desde archivo externo

- Se crea carpeta js y archivo app.js en ella
- Se enlaza archivo js/app.js a practica-1.html usando la etiqueta `<script>` dentro de etiqueta `<head>`

**Archivo: practica-1.html**
```html
<!DOCTYPE html>
<html lang="es" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>JavaScript Esencial</title>
    <script src="../js/app.js"></script>
  </head>
  <body>
    <script>
      alert('Hola Mundo!!');
    </script>
  </body>
</html>
```
**Archivo: app.js**
```JavaScript
alert('Hola Mundo!! desde archivo externo');
```

#### La Consola

1.- Se crea mesaje desde la consola en archivo externo
```JavaScript
alert('Hola Mundo!! desde archivo externo');

console.log('Hola Mundo!! desde la consola');
```
###### resultado:
![Hola Mundo, desde consola](/img/consola.png)

2.- Se crea variable "nombre" desde archivo practica-1.html
```html
<!DOCTYPE html>
<html lang="es" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>JavaScript Esencial</title>
    <script src="../js/app.js"></script>
  </head>
  <body>
    <script>
      alert('Hola Mundo!!');

      var nombre = 'Sergio';

      console.log('El nombre es: ',nombre);
    </script>
  </body>
</html>
```
3.- Se manda el resultado de la variable nombre a la consola
![Resultado consola](/img/consola1.png)
### Escribiendo comentarios en JavaScript

##### Comentarios de 1 sola linea
1- Se crea comentario de Linea en archivo js/app.js - estos comentarios abarcan 1 sola linea

```JavaScript
//alert('Hola Mundo!! desde archivo externo');

console.log('Hola Mundo!! desde la consola');
```
##### Comentarios de bloque
2.- Se crea comentario de Bloque en archivo practica-1.html - Estos comentarios pueden abarcar tantas lineas como se necesiten

```html
<!DOCTYPE html>
<html lang="es" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>JavaScript Esencial</title>
    <script src="../js/app.js"></script>
  </head>
  <body>
    <script>
      /*alert('Hola Mundo!!');

      var nombre = 'Sergio';

      console.log('El nombre es: ',nombre);*/
    </script>
  </body>
</html>
```
Tambien podemos usar los comentarios para dejar alguna referencias de nuestro trabajo *ejemplo:*

```JavaScript
//alert('Hola Mundo!! desde archivo externo');

//Este es un mensaje de la consola
console.log('Hola Mundo!! desde la consola');
```

### Strict Mode

1.- Se crea ejemplo usando variable no declarada

2.- Se crea ejemplo usando palabra reservada

3.- Se agrega modo estricto en la primera linea 'use strict'

```JavaScript
"use strict"

//alert('Hola Mundo!! desde archivo externo');

//Este es un mensaje de la consola
console.log('Hola Mundo!! desde la consola');
```

## Variables

Las variables en los lenguajes de programación siguen una lógica similar a las variables utilizadas en otros ámbitos como las matemáticas. Una variable es un elemento que se emplea para almacenar y hacer referencia a otro valor. Gracias a las variables es posible crear "programas genéricos", es decir, programas que funcionan siempre igual independientemente de los valores concretos utilizados.

Las variables en los lenguajes de programación siguen una lógica similar a las variables utilizadas en otros ámbitos como las matemáticas. Una variable es un elemento que se emplea para almacenar y hacer referencia a otro valor. Gracias a las variables es posible crear "programas genéricos", es decir, programas que funcionan siempre igual independientemente de los valores concretos utilizados.

```JavaScript
"use strict"

var nombre = 'Sergio';
```


### Ámbito de las variables

El ámbito de una variable (llamado "scope" en inglés) es la zona del programa en la que se define la variable. JavaScript define dos ámbitos para las variables: global y local.

### Variable Local

Solamente está definida dentro de la función. Cualquier instrucción que se encuentre dentro de la función puede hacer uso de esa variable, pero todas las instrucciones que se encuentren en otras funciones o fuera de cualquier función no tendrán definida la variable

```JavaScript
"use strict"

var nombre = 'Sergio';

console.log(nombre);

function saludo (){
  var nombre = 'Bruno';
    console.log(nombre);
}

saludo ();
```

### Variables Globales

Está definida en cualquier punto del programa (incluso dentro de cualquier función).

Si una variable se declara fuera de cualquier función, automáticamente se transforma en variable global independientemente de si se define utilizando la palabra reservada var o no. Sin embargo, las variables definidas dentro de una función pueden ser globales o locales.

```JavaScript
"use strict"

var nombre = 'Sergio';

function saludo (){

}

saludo ();
```


Si en el interior de una función, las variables se declaran mediante var se consideran locales y las variables que no se han declarado mediante var, se transforman automáticamente en variables globales.

¿Qué sucede si una función define una variable local con el mismo nombre que una variable global que ya existe? En este caso, las variables locales prevalecen sobre las globales, pero sólo dentro de la función

¿Qué sucede si dentro de una función se define una variable global con el mismo nombre que otra variable global que ya existe? En este otro caso, la variable global definida dentro de la función simplemente modifica el valor de la variable global definida anteriormente

La recomendación general es definir como variables locales todas las variables que sean de uso exclusivo para realizar las tareas encargadas a cada función. Las variables globales se utilizan para compartir variables entre funciones de forma sencilla.
