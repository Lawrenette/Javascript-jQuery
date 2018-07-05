## Qué es Javascript?
- Es un lenguaje de programación que fue diseñado para darle interacción a las páginas web.
- Es posible usarlo para hacer en múltiples ámbitos, aplicaciones de sevidor e incluso de escritorio.

----------

### Por qué debemos aprender Javascript?
- Es uno de los pilares del desarrollo front-end.
- Es uno de los lenguajes de programación más populares en la actualidad.

### Qué podemos hacer con Javascript?
- Agregar interactividad entre nuestro sitio web y el usuario.
- Integrar servicios que nos entregan nuevas funcionalidades.
- Actualizar información sin necesidad de recargar nuestra página.

----------

A un programa hecho en javascript se le suele llamar **script** 

...a menos que el programa sea muy grande...

----------


### Avisos:

- **Alerta:** no se usan mucho en páginas por que son molestas, solo para pruebas de javascript.

		alert("hola");
  
- **Propmt:** Este instruccion nos muestra un dialogo con un mensaje, que solicita al usuario que escriba un texto

		contenedor = prompt("Cual es tu nombre?");
		console.log(contenedor);

### Variables
Son como un contenedor, pueden almacenar los valores que nosotros queramos.
Con **=** podemos asignar un valor a una variable
Podemos cambiar el valor de un momento a otro, por eso se llaman variables

		a = 6;
		alert(a); // 6

### Introducción a operaciones y tipos de variables
Aquí el simbolo **+** funciona exactamente igual como aprendimos en matemáticas, este es un ejemplo de operador

		console.log(2+2); // 4

La consola funciona como una calculadora

		a = 3;
		b = 3;
		console.log(a*b); // 9
**Las variables pueden almacenar valores y podemos operar sobre esos valores**

----------

### Tipos de datos
- **Number:** Cualquier número entero o decimal; positivo o negativo

		number = 120;

- **Strings:** Cualquier texto encerrado entre comillas dobles o simples

		string = "Hola";

----------
Podemos hacer que la consola responda que tipo de dato es:

		typeof(2); // "number"
		typeof("2"); // "string"

----------
**En Javascript las operaciones dependen de los tipos de datos**

- String + String = String

		"10" + "10"; // 1010
		"hola" + "_mundo"; // hola_mundo

- String + Number = String

		"Mi nota es un" + 10; // "Mi nota es un 10"
		"10" + 2; // 102

### Convertir String a Number

	a = prompt("Ingresar número 1");
	a = parseInt(a);
	b = prompt("Ingresar número 2");
	b = parseInt(b);
	console.log(a+b);

----------

## Sintaxis en Javascript
Es la rama de la gramática que estudia las relaciones de las palabras al combinarse para formar unidades superiores en significado

### Sentences
Sentencias o frases

- Las instrucciones son llamadas sentencias
- Cada sentencia es terminada con punto y coma

		miNombre = "Lawren";

### Anatomía de Javascripts
- Javascripts lee las sentencias de izquierda a derecha
- Javascripts transforma la sentencia en una secuencia de elementos que pueden ser:
	- Tokens
	- Controles de caracteres
	- Espacios en blanco
	- comentarios
	- Terminaciones
	- etc

### Análisis léxico
Como el navegador interpreta la sintaxis de javascript

----------


## Tokens:

### Identificadores (variables / funciones):
Son los nombres de las variables

- Deben empezar con una ( letra ), ( _ ) ó ( $ )
- **No** se debe comenzar con números (se pueden agregar en los valores subsiguientes)
- **No** puede empezar con comillas (ni simples ni dobles)
	- Esto es para distinguir una variable de un string
- Se puede comenzar con letras mayúsculas o minúsculas
- Se pueden usar letras Unicode como **ñ** o **ä** como identificador

### Puntuadores (+, -, *, =, /, %)
Operar con valores o variables

### Valores literales (number / strings)
- Son un valor que debe ser leído **Literalmente** (cuando decimos 2, es el número 2)
- Todos los valores que asignamos, o sea, **números o strings son literales**
	- Los strings siempre estan en comillas, la variable **no**

			a = "2";
			console.log("a"+2); // 22
			
			a = 2;
			console.log("a"+2); // a2

### Palabras reservadas
- Son palabras claves que realizan funciones propias de javascript
- No se pueden utilizar como variables, funciones metodos o identificadores

#### *NO son tokens:* 
espacios en blancos y comentarios

----------

#### Operación Aritmetica

		a + b
#### Asignación

		a = 8

#### Comparación

		a == b

----------

## Qué es JQuery?
Es una biblioteca que hace más fácil trabajar con Javascript en nuestros sitios web

#### Qué nos puede ayudar a hacer?
- JQuery toma funcionalidades comunes que requieren varias lineas de codigo javascript y las empaqueta en funciones que podemos utilizar con muy pocas lineas de codigo
- Nos permite manejar de forma sencilla los llamados AJAX y la captura y manipulacion de elementos de nuestra pagina web

	1. **Crear el archivo html**
		- Crearemos un archivo HTML
		- Escribiremos un título que diga: "Sin JQuery"
	2. **Integrar JQuery**
Existen dos maneras de integrarlo en nuestros proyectos:
		- Descargando la biblioteca desde [https://jquery.com/download](https://jquery.com/download "Aquí")
		- Integrando el CDN de JQuery desde [https://code.jquery.com](https://code.jquery.com "Aquí")

Pega el código debajo del título que escribimos hace un rato

----------
### DOM
**D**ocument **O**bject **M**odel

##### Resumen:

- El DOM nos permite modificar el contenido de una página dinámicamente con javascript
- Jquery es una biblioteca para javascript que nos permite modificar el DOM y crear animaciones con muy poco código
- Para poder ocupar jquery primero tenemos que integrarlo a nuestro proyecto

#### Qué podemos lograr manipulando el DOM?
- Podemos obtener el valor de los elementos HTML
- Crear nuevos elementos HTML y añadirlos a la página
- Modificar atributos
- Aplicar animaciones a los elementos HTML

### Lógica básica para aplicar Jquery

- Integrar Jquery (Sólo 1 vez por página)
- Utilizar el selector para encontrar el elemento que se desea modificar
- Modificar el elemento

----------

Ejemplo
##### Integramos jQuery

		<script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>

##### Seleccionamos todos los elementos h1

		$("h1").text("Con JQuery");

##### Modificamos todos los elementos seleccionados

		.text que está arriba

## Anatomía de jQuery

		$("selector").acción();

- **$() ó jquery():** Constructor
- **Selectores:** Selecciona los elementos desde DOM
	- Es una de las funcionalidades más importantes de jQuery
	- Sirven para "buscar" o "seleccionar" elementos HTML en función de id, class, nombre, atributos, valores, etc.
- **Acciónes:** Acción de JQuery que se realizará en el elemento

----------

## Eventos

#### Hago click en p, y aparece alerta con "hola"
		$("p").on("click", function(){
		alert("hola")
		});
- p: selector
- click: el tipo de evento
- alert: que va a suceder cuando se gatille el evento

#### Hago click en h1, y se agrega "hola" en h1 y p
		$("h1").on(click, function(){
		$("h1").append("hola");
		$("p").append("hola");
		})
#### Hago click en h1, y cambia de color el texto
		$("h1").on("click", function(){
		$("h1").css("color", "yellow");
		})

-----
		style 
		h1{
		transition: 1s;
		.red{
		color: red;
		}
		$("h1").on("click", function(){
		$("h1").addClass("red");
		})

#### Agregar y quitar efectos con el click
		$("h1").on("click", function(){
		$("h1").toggleClass("red");
		})

## Evento ready

**jQuery 1 y 2**

		$(document).ready(function(){
		//Métodos de Jquery
		});

**jQuery 3**

		$(function(){
		/ codigo javascript /
		});

Este método nos permite ejecutar código cuando el DOM está cargado
