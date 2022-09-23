# :smiley_cat::high_brightness: Week Challenges 4
> *"Para tener éxito tu deseo de alcanzarlo debe ser mayor que tu miedo al fracaso"* 
>***- Bill Cosby***

## :date: Monday exercises
<h3 style="font-size: 20px">1. For of loop :orange_book::black_nib:</h3>

Los objetos iterables son una generalización de arrays. Es un concepto que permite que cualquier objeto pueda ser utilizado en un bucle **for..of**. La sentencia sentencia for...of ejecuta un bloque de código para cada elemento de un objeto iterable, por ejemplo, las cadenas o strings. 
Muchos operadores y métodos se basan en la iterabilidad. Si un objeto no es técnicamente una matriz, pero representa una colección (lista, conjunto) de algo, entonces el uso de la sintaxis for..of es una gran forma de recorrerlo. 

Sintaxis 
```javascript 
for (variable of iterable)
  statement
```

<h3 style="font-size: 20px">2. JavaScript Array Filter :ledger::black_nib:</h3>

Es un método que busca los elementos que cumplen con una condición dada, y devuelve un array con todos los elementos encontrados. 

Sintaxis 

```javascript
// Arrow function
filter((element, index, array) => { /* … */ } )

// Callback function
filter(callbackFn, thisArg)

// Inline callback function
filter(function(element, index, array){ /* … */ })
```


<h3 style="font-size: 20px">3. JavaScript Array Reduce :closed_book::black_nib:</h3>

- Cuando necesitamos iterar sobre un array podemos usar **forEach, for o for..of**.
- Cuando necesitamos iterar y devolver un valor por cada elemento podemos usar **map**.
- Los métodos arr.reduce y arr.reduceRight también pueden iterar, pero son un poco más complejos. Se los utiliza para calcular un único valor a partir del array.

La función es aplicada a todos los elementos del array, uno tras de otro, y va arrastrando el resultado parcial al próximo llamado. Mientras la función sea llamada, el resultado del llamado anterior se pasa al siguiente como primer argumento. Entonces, el primer argumento es el acumulador que almacena el resultado combinado de todas las veces anteriores en que se ejecutó, y al final se convierte en el resultado de reduce.

La sintaxis es la siguiente:

```javascript 
let value = arr.reduce(function(accumulator, item, index, array) {
  // ...
}, [initial]);
```


<h3 style="font-size: 20px">4. JavaScript Array Map :green_book::black_nib:</h3>

El método **arr.map** es uno de los métodos más comunes y ampliamente usados. Este método llama a la función para cada elemento del array y devuelve un array con los resultados. 

La sintaxis es:
```javascript
let result = arr.map(function(item, index, array) {
  // devuelve el nuevo valor en lugar de item
});
```

Ejemplo: 
``` javascript
const array1 = [1, 4, 9, 16];
// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]
```

## :date: Tuesday exercises
<h3 style="font-size: 20px">1. Expresiones Regulares o REGEX</h3>

Las expresiones regulares son una forma de describir patrones en datos de tipo string. Estas forman un lenguaje pequeño e independiente que es parte de JavaScript y de muchos otros lenguajes y sistemas. Son una poderosa herramienta para inspeccionar y procesar cadenas. 

Una expresión regular es un tipo de objeto. Puede ser construido con el constructor **RegExp** o escrito como un valor literal al envolver un patrón en caracteres de barras diagonales **(/)**.

```javascript
let re1 = new RegExp("abc");
let re2 = /abc/;
```

:link:**Rescurso:** https://eloquentjs-es.thedojo.mx/09_regexp.html

<h3 style="font-size: 20px">1. Replace</h3>

El método replace() busca, reemplaza y devuelve una nueva cadena con las coincidencias de un patrón reemplazadas por algo. :wink: La navaja suiza para buscar y reemplazar. 

Podemos usarlo sin expresiones regulares, para buscar y reemplazar una sub-cadena:
```javascript 	
// reemplazar guion por dos puntos
alert('12-34-56'.replace("-", ":")) // 12:34-56
``` 

El patrón puede ser una cadena o RegExp, y el reemplazo puede ser una cadena o una función llamada para cada coincidencia. Si el patrón es una cadena, solo se reemplazará la primera aparición. La cadena original se deja sin cambios.
```javascript 	
// reemplazar todos los guiones por dos puntos
alert( '12-34-56'.replace( /-/g, ":" ) )  // 12:34:56
``` 
	
:link:**Recursos:** https://es.javascript.info/regexp-methods


## :anger:EXTRA 

- :white_check_mark: Simple Validation Of A Username exercise
- :white_check_mark: Get Number From String exercise
- :white_check_mark: String Cleaning exercise
- :white_check_mark: Password Validation exercise


