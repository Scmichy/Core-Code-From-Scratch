# :tada: Week Challenges 2
" Los grandes trabajos mo som hechos por la fuerza, sino por la perseverancia"

# :date: Monday exercises

# :date: Tuesday exercises
## **1. HTML Course**
Lo que aprendí hoy en el curso :exclamation::point_down:

1.1 LAS PÁGINAS WEB SE CONFORMA POR :computer:

:small_orange_diamond:**Frontent:** Es todo lo que el usuario puede ver, es decir el diseño de la página, colores, forma, temas, etc.

:small_orange_diamond:**Backend:** es la parte que el usuario no puede ver, normalmente se encarga de la parte pesada, como leer y guardar datos, ingresar a las BD, retornar los datos al fronted, segun reaqeurimiento, etc. 

img

1.2 ROLES DE DESARROLLADORES

:woman: **Frontend Developer:** se encarga del código para la parte visual que el usuario va a poder ver. 

:man: **Backend Developer:** Se encarga de las cosas que el usuario no puede ver, por ejemplo el manejo de datos.

:department_store: **Fullstack Developer:** Es la combinacion de los dos.

1.3 Lenguajes de las páginas web:

- **HTML:** no es lenguaje de programacion, es un lenguaje de marcado de hipertexto, y su funcion es crear la estructura que va a tener la página web.

- **CSS:** Tampoco es un lenguaje de programación, es una hoja de estilo en cascada, y define las propiedades del estilo de la página web

- **Javascript:** si es un lenguaje de programacion y se encarga de darle la funcionalidad a nuestra pagina web

1.4 Analogía de una página web: Podemos compararlo como un edificio :department_store:

HTML --> es la estructura del edificio

CSS --> es el estilo del edificio por ejemplo los colores y decoraciones.

JavaScript --> es la funcionalidad del edificio por ekjemplo los elevadores.

1.5 TRÁFICO EN RED: En las páginas existen las partes **cliente** y **servidor**.

Un *Cliente* realiza una busqueda, entonces le manda un *Request* al servidor y el servidor le realiza un *Response* al *cliente* para de volverle la información solicitada. Y luego el navegador crea el *DOM* (Modelo del Documento en OBjeto), donde están los datos del html que devuelve el servidor.

- Cliente --> Request ...
- Servidor --> Response...
- DOM


## **2. Multiply Excercise** :boom:
Bad Code **CODEWARS** :x:
```javascript
function multiply(a, b){
  a * b
} return multiply;

console.log(multiply(8,10)); //Test
```
Correct Code :heavy_check_mark:
```javascript
function multiply(a,b){
  var result;
 result = a * b;
  return result;
}
console.log(multiply(8,10)); //Test
```
:interrobang::eyes: *El error se encontraba en el retorno del resultado de la multiplicción, pues se estaba retornando la funcion como tal, pero no el resultado*

## **3. ASCII Exercise** 
<h3 style="color:#01A9DB; text-align:center">3.1ASCII (American Stand Code for Information Interchange):</h3>

El **código ASCII** fue creado en 1963 por ASA (hoy en día ANSI), Este código requiere 7 bits, (dándonos 128 caracteres). La mayoría de los teclados de computadora se estandarizan de acuerdo al código ASCII. 
- Los primeros 32 caracteres ASCII son comandos *NO gráficos*, sin representación en la pantalla ya que son caracteres de control. Por ejemplo espacios, comas, puntos, signos de exclamación e instrucciones para comunicar al receptor.
- El resto son caracteres que pueden mostrarse en pantalla (excepto el carácter 128 que es de control). 
- El código ***ASCII extendido*** requiere de 8 bits

img

<h3 style="color:#01A9DB; text-align:center">3.2 Katana CODERWARS</h3>

:clipboard: You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.

examples:
uniTotal("a") == 97 uniTotal("aaa") == 291

:small_blue_diamond: Solution :

```javascript 
//The reduce method receives 2 parameters and is told where to start
function uniTotal(cadena) { //The string as a parameter.
  //1. An array is created with the entered string.
  //2. suma total + letra 
//total --> sum result
 //char --> each parameter of the array.
  var MetodReduce = Array.from(cadena).reduce((total, letra) => total + 
 letra.charCodeAt(0), 0); //convert character to decimal (ASCII) 
  //and indicate where it starts.
  return MetodReduce; //return the previous process
}
  console.log(uniTotal("abc")); //test
```

# :date: Wednesday exercises
## **1. HTML Course :part_alternation_mark:**

<h3 style="font-size: 20px;">1.1 ESTRUCTURA BASE DE UNA PÁGINA WEB</h3>

<p align="center">
  <img src="/src/weeks/imgs/estructura_html.png" width="350" title="Estructura base HTML">
  <img src="estructura_html_2.jpg" width="350" title="Etiquetas base HTML">
</p>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>

<!-- por cierto, este es un comentario.
<head></head> --- Aqui se ubican los metadatos.
<title></title> --- Texto que aparece en la pestaña de la página.
<body></body> --- El cuerpo, donde va a ir el contenido de la página.
-->

```
***Metadatos***: Son caracteres que vamos a utilizar en nuestras páginas web, si bien no son obligatorios, algunos son necesarios.

<h3 style="font-size: 20px;">1.2 FORMAS DE AGREGAR ESTILO EN HTML:</h3>

Existen tres formas de agregar estilo a nuestra páginas:

1. In Line Style: se le agrega estilo directamente sobre un elemnto, con el atribulo "style":
```html
 <p style="color: rgba(226, 124, 218)">hello word!</p> 
 ```
 :no_entry_sign: (NO es lo recomendado).

2. In Ternal Style: el estilo css esta interno en el código de nuetro html: esta en el head
```html
<style>
      p {
        color: rgb(0, 255, 106);
      }
    </style>
```

3. External CSS: se crea un achivo externo de css, luego se enruta en el archivo html:
Esto va en head 
```html
<link rel="stylesheet" href="index.css">
```
  -  Esto va en la hoja css externa: 
```css
p{
    color:aqua;
    font-size: 50px;
    font-family: cursive;
}
```
<h3 style="font-size: 20px;">1.3 Elementos de css</h3>

- **id:** es el identificador único de cada elemeto que lo diferencia del resto, por lo tanto, no se puede compartir. En css se invoca de la siguiente manera: *#NombreId{ }*

- **class:** es la clasificación de los elementos, y esta se pueden compartir. En css se manda a llamar --> *.NombreClass{ }*, (con punto).



| Tag | Description | 
| :----------------- |:-------------| 
| 'head' | Se escribe en un lenguaje definido y modificable en cada momento
| Las instrucciones se envían directamente al procesador, ya traducidas.      |  Las instrucciones se traducen antes de llegar.      
| Se requiere de un paso extra para que se ejecute el código fuente | El código fuente se ejecuta a través de un solo comando      
| Se ejecuta más rápido. | Se tarda en ejecutar, porque debeb de traducir todo cada vez     | 
| El programa se ejecuta en ciertos equipos o sistemas operativos | El programa funciona en todas las máquinas y sistemas      
| Los errores de compilación impiden que se compile el código. |  Los errores son visibles cuando se inicia el programa    
| Ejemplos: C, C++, Delphi, Go | Ejemplos: Python, Javascript, Ruby, Perl, PHP   


## **2. Char From ASCII Value**
2.1 Katana Coderwars:

:scroll: Escriba una función get_char() / getChar() que tome un número y devuelva el carácter ASCII correspondiente a ese valor.

Example: get_char(65) --> should return: 'A'

:small_blue_diamond: Solution:

```javascript
function getChar(c){
  return String.fromCharCode(c); //method to convert ASCII code
}
console.log(getChar(50)); //Test
```
## **3. Binary Addition**
3.1 Katana Coderwars

:scroll: Implemente una función que sume dos números y devuelva la suma en binario. La conversión se puede hacer antes o después de la adición. El número binario devuelto debe ser una cadena. Ejemplos:(Entrada1, Entrada2 --> Salida (explicación)))

:small_blue_diamond: Solution: 
```javascript
function addBinary(a, b) {
  return (a + b).toString(2); //the method returns the number in base 2 (binary)
}
console.log(addBinary(3,5)); //test
```
## **4. Student's Final Grade Exercise**
4.1 Katana Koderwars:
:scroll: Cree una función notaFinal, que calcule la nota final de un estudiante en función de dos parámetros: una nota para el examen y una cantidad de proyectos completados. Esta función debe tomar dos argumentos: examen - calificación del examen (de 0 a 100); proyectos - número de proyectos completados (de 0 en adelante);

Esta función debería devolver un número (calificación final). Hay cuatro tipos de calificaciones finales:

- 100, si la calificación del examen es superior a 90 o si el número de proyectos terminados es superior a 10.
- 90, si la calificación del examen es superior a 75 y si el número de proyectos completados es mínimo 5.
- 75, si la calificación del examen es superior a 50 y si el número de proyectos completados es mínimo 2.
- 0, en otros casos

:small_blue_diamond: Solution:
```javascript
function finalGrade (exam, projects) { //entry parameters, exam grade and delivered projects
  var finalNote; //variable for final note

  if (exam > 90 || projects > 10){ // if you comply with this
    finalNote = 100; // get a grade of 100
  } else if (exam > 75 && projects >= 5){ //but if you get this
    finalNote = 90; // get a grade of 90
  } else if(exam > 50 && projects >= 2){ // but if you get this
    finalNote = 75; // get a grade of 75
  } else{ 
   finalNote = 0; /// get a grade of 0
  }
  return finalNote; // return the final grade corresponding to the case
}
console.log(finalGrade(20, 2)); //Test
```
**Note: cambie las notas según los casos, para verificar que se cumplan todos**

# :date: Thursday exercises
## **1. HTML Course (part 2)** 


