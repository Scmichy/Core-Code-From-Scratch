# :smiley_cat::high_brightness: Week Challenges 4
> *"Para tener éxito tu deseo de alcanzarlo debe ser mayor que tu miedo al fracaso"* 
>***- Bill Cosby***

## :date: Monday exercises
<h3 style="font-size: 20px">1. For of loop</h3>

Los objetos iterables son una generalización de arrays. Es un concepto que permite que cualquier objeto pueda ser utilizado en un bucle **for..of**. La sentencia sentencia for...of ejecuta un bloque de código para cada elemento de un objeto iterable, por ejemplo, las cadenas o strings. 
Muchos operadores y métodos se basan en la iterabilidad. Si un objeto no es técnicamente una matriz, pero representa una colección (lista, conjunto) de algo, entonces el uso de la sintaxis for..of es una gran forma de recorrerlo. 

Sintaxis 
```javascript 
for (variable of iterable)
  statement
```

<h3 style="font-size: 20px">2. JavaScript Array Filter</h3>

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


<h3 style="font-size: 20px">3. JavaScript Array Reduce</h3>

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


<h3 style="font-size: 20px">4. JavaScript Array Map</h3>
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
<h3 style="font-size: 20px">1. Simple Pig Latin exercise</h3>

## :date: Wednesday exercise
<h3 style="font-size: 20px">1. Simple Pig Latin exercise</h3>

## :date: Thursday exercises
<h3 style="font-size: 20px">1. Simple Pig Latin exercise</h3>