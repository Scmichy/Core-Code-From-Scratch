# :tada: Week Challenges 2
" Los grandes trabajos mo som hechos por la fuerza, sino por la perseverancia"

# :date: Monday exercises

# :date: Tuesday exercises
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
___
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

# :date: Thursday exercises


