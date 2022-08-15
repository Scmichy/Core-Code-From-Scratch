# :hammer::raised_hands: Week Challenges 3
> *"Siempre parece imposible... hasta que se hace"* 
>***- Nelson Mandela***

## :date: Monday exercises
<h3 style="font-size: 20px">1. Who Likes It? exercise</h3>

 :scroll: **Description:** Probablemente conozcas el sistema de "me gusta" :+1: de Facebook y otras páginas. Las personas pueden "gustar" publicaciones de blog, imágenes u otros elementos. Queremos crear el texto que debe mostrarse junto a dicho elemento.

Implemente la función que toma una matriz que contiene los nombres de las personas a las que les gusta un artículo. Debe devolver el texto de la pantalla como se muestra en los ejemplos:
```
[]                                -->  "no one likes this"
["Peter"]                         -->  "Peter likes this"
["Jacob", "Alex"]                 -->  "Jacob and Alex like this"
["Max", "John", "Mark"]           -->  "Max, John and Mark like this"
["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"
```
**Note:** Para 4 o más nombres, el número en "y otros 2" simplemente aumenta.

code solution :ballot_box_with_check:
```javascript
function likes(names) {
  let size = names.length;
  if (size == 0) return `no one likes this`;
  else if (size == 1) return `${names[0]} likes this`;
  else if (size == 2) return `${names[0]} and ${names[1]} like this`;
  else if (size == 3)
    return `${names[0]}, ${names[1]} and ${names[2]} like this`;
  else return `${names[0]}, ${names[1]} and ${size - 2} others like this`;
}
```

:pushpin::paperclip: **NOTES:** Se resolvió este ejercicio utilizando ***if...else*** anidado, para que ejecute una sentencia en base a una condición especificada, es decir, a cada caso del problema. 
- :link: [Link resource](/src/weeks/Themes/README.md)

<h3 style="font-size: 20px">2. Bit Counting exercise</h3>

:scroll: **Description:** Escribe una función que tome un número entero como entrada y devuelva el número de bits que son iguales a uno en la representación binaria de ese número. Puede garantizar que la entrada no es negativa.

Ejemplo: la representación binaria de 1234 es 10011010010, por lo que la función debería devolver 5 en este caso

Code Solution :ballot_box_with_check: 
```javascript
var countBits = (n) => {
  let bit = n.toString(2); //convierte el valor a base 2 (binario)
  let count_one = 0; //contador de numeros '1'

  for (let i = 0; i < bit.length; i++) {
    // recorre cada digito convertido
    if (bit[i] === "1") count_one++; // si el  digito es '1', aumenta el contador
  }
  return count_one; // retorna el valor del contador
};
console.log(countBits(1234)); //test
```
:pushpin::paperclip: **NOTES:** El método toString(2) retorna una cadena representando el código fuente de la función. En este caso, .toString(2) se retornará el valor de la cadena en base 2 (binario).

- :link: [Link resource](/src/weeks/Themes/README.md)

<h3 style="font-size: 20px">2. Your order, please exercise</h3>

:scroll: **Description:** Su tarea es ordenar una cadena dada. Cada palabra en la cadena contendrá un solo número. Este número es la posición que debe tener la palabra en el resultado.

Nota: Los números pueden ser del 1 al 9. Por lo tanto, 1 será la primera palabra (no 0).

Si la cadena de entrada está vacía, devuelve una cadena vacía. Las palabras en la cadena de entrada solo contendrán números consecutivos válidos.

Ejemplos
```
"is2 Thi1s T4est 3a"  -->  "Thi1s is2 3a T4est"
"4of Fo1r pe6ople g3ood th5e the2"  -->  "Fo1r the2 g3ood 4of th5e pe6ople"
""  -->  ""
```
Code Solution :ballot_box_with_check:

```javascript
function order(words) {
  words = words.split(" "); //Divide la cadena
  var arrayNew = [];
  var oneWord = "";

  if (words == "") return ""; //si la cadena es vacia, devuelve lo mismo

  for (let i = 0; i < words.length; i++) {
    //for para recorrer cada palabra de la cadena
    oneWord = words[i];
    for (let j = 0; j < oneWord.length; j++) {
      //for para dividir cada letra de las palabras
      var letra = parseInt(oneWord[j]); //cada letra se pasa a entero

      if (Number.isNaN(letra)) {
        // si es no es un numero
        continue; //pasa a la siguiente letra
      } else {
        //si es un numero
        arrayNew[letra - 1] = words[i];
        //En un nuevo array, se introduce la palabra en la posicion de la letra -1.
      }
    }
  }
  return arrayNew.join(" ");
}
console.log(order("is2 Thi1s T4est 3a"));
console.log(order("4of Fo1r pe6ople g3ood th5e the2"));
```
:pushpin::paperclip: **NOTES:** 
- El método Number.isNaN() determina si el valor pasado es NaN. (Not A Number). 
- parseInt()Convierte (parsea) un argumento de tipo cadena y devuelve un entero de la base especificada.

- :link: [Link resource](/src/weeks/Themes/README.md)

## :date: Tuesday exercises

## :date: Wednesday exercises

## :date: Thursday exercises