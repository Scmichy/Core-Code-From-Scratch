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
- :link: [Link resource](/src/weeks/Themes/README.md/#)

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

- :link: [Link resource](/src/weeks/Themes/README.md/#if_else)

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
<h3 style="font-size: 20px">1. Simple Pig Latin exercise</h3>

:scroll: **Description:** Mueva la primera letra de cada palabra al final de la misma, luego agregue "ay" al final de la palabra. Deje los signos de puntuación intactos

Ejemplos:
```
pigIt('Pig latin is cool'); // igPay atinlay siay oolcay
pigIt('Hello world !');     // elloHay orldway !
```
Code Solution :ballot_box_with_check:
```javascript
function pigIt(str) {
  var newWord;
  var punMarks = [
    //arreglo de signos de puntuacion que se tendrán que avadir
    ".",
    ",",
    ":",
    ";",
    "[",
    "]",
    "...",
    "¿",
    "?",
    "¡",
    "!",
    "(",
    ")",
    "{",
    "}",
    "-",
  ];

  str = str.split(" "); //separar el string
  var size = str.length;
  for (let i = 0; i < size; i++) {
    //recorre el string
    if (punMarks.indexOf(str[i]) < 0) //verificamos si el índice del valor actual se encuentra en el array de signos de puntuacion.
      newWord = str[i].slice(1) + str[i].substring(0, 1) + "ay";
    // si no se encuentra, modifica la palabra con las condiciones dadas
    else continue;  // si, si está en el array, continua con el siguiente valor
    str[i] = newWord; //se guardan los cambios
  }

  return str.join(" "); // se modifica el array para que retorne como string con espacios validos
}
console.log(pigIt("Hello world !")); //test
```
:pushpin::paperclip: **NOTES:** 
- El método substring(indiceA, indiceB) devuelve un subconjunto de un String. Es decir, que extrae caracteres desde indiceA hasta indiceB sin incluirlo.
- Array.join() es un métod que une todos los elementos de una matriz en una cadena y la devuelve.
- El método split("") divide un String en un array de cadenas con separación en subcadenas. 
- .indexOf() es un metodo que compara el elemento dado con elementos array, y retorna el primer indice si encuentra coincidencia o -1 si el elemento no esta presente.
- :link: [Link resource](/src/weeks/Themes/README.md)

<h3 style="font-size: 20px">2. Counting Duplicates exercise</h3>

:scroll: **Description:** Escriba una función que devuelva el recuento de caracteres alfabéticos y dígitos numéricos distintos que no distinguen entre mayúsculas y minúsculas que aparecen más de una vez en la cadena de entrada. Se puede suponer que la cadena de entrada contiene solo letras (tanto mayúsculas como minúsculas) y dígitos numéricos.

Example
```
"abcde" -> 0 # no characters repeats more than once
"aabbcde" -> 2 # 'a' and 'b'
"aabBcde" -> 2 # 'a' occurs twice and 'b' twice (`b` and `B`)
"indivisibility" -> 1 # 'i' occurs six times
"Indivisibilities" -> 2 # 'i' occurs seven times and 's' occurs twice
"aA11" -> 2 # 'a' and '1'
"ABBA" -> 2 # 'A' and 'B' each occur twice
```
Code Solution :ballot_box_with_check:
```javascript
function duplicateCount(text) {
  var count = 0;
  var valAnte = "";
  var cadena = text.toLowerCase().split("").sort();
  // convert to lowercase, convert to array and write and sort from smallest to largest according to ASCII code

  if (cadena == "") return 0; //if empty string, return 0 repeated

  for (let i = cadena.length - 1; i >= 0; i--) {
    // recorre el array
    if (cadena[i] === cadena[i - 1] || cadena[i] === cadena[i + 1]) {
      // val equal to previous or next val
      if (valAnte !== cadena[i]) {
        //if the value is different from previous val, it is a new repeated val
        valAnte = cadena[i]; //toma el val del actual para que se cuente 1 vez el val repetido
        count++; // aumenta contador de letras repetidas y no cuantas veces se repite
      }
    }
  }
  return count; // retorna el contador con los valores repetidos
}
console.log(duplicateCount("Indivisibilities"));  //test
```
:pushpin::paperclip: **NOTES:** 
- .toLowerCase(), este método devuelve el valor en minúsculas de la cadena dada.
- El método .sort() ordena y devuelve los elementos de un array, por de fecto los ordena según su codigo ASCII. 
- :link: [Link resource](/src/weeks/Themes/README.md)

<h3 style="font-size: 20px">3. Decode The Morse Code exercise</h3>

:scroll: **Description:** En esta kata debes de   implementar un decodificador de código Morse simple. El código Morse codifica cada carácter como una secuencia de "puntos" y "guiones". El código Morse no distingue entre mayúsculas y minúsculas, tradicionalmente se utilizan letras mayúsculas. Cuando el mensaje está escrito en código Morse, se usa un solo espacio para separar los códigos de los caracteres y 3 espacios para separar las palabras. 

For example:
```
A se codifica como --> "·−"
Q se codifica como --> "−−·−"
1 se codifica como --> "·−−−−."

decodeMorse('.... . -.--   .--- ..- -.. .')
//should return "HEY JUDE"
```
NOTA: Los espacios adicionales antes o después del código no tienen significado y deben ignorarse.

Code Solution :ballot_box_with_check:
```javascript
function decodeMorse(morseCode) {
  morseCode = morseCode.trim().split(""); //elimino los espacios de los extremos y divido los elemntos en el array
  var newString = []; // para intruducir mi string traducido
  var words = ""; // recopila un conjunto de caracteres para traducir una letra

  for (let i = 0; i < morseCode.length; i++) {
    //recorre cada elemento del array
    if (morseCode[i] !== " ") {
      // si se topa con un caracter diferente de ' ' -> espacio
      words += morseCode[i]; // agrega el caracter que formará una letra
    }
    if (morseCode[i] == " " && morseCode[i - 1] !== " ") {
      //si se topa con un caracter y un  ' '
      newString += MORSE_CODE[words]; //setraduce el conjunto de caracteres anteriores
      words = ""; // se setea la variable para que se introduzcan nuesvos caracteres
    }
    if (
      // si se encuentra con 3 espacios
      morseCode[i] == " " &&
      morseCode[i + 1] == " " &&
      morseCode[i - 1] == " "
    )
      newString += " "; // se agrega un espacio a nuestro string
  }
  newString += MORSE_CODE[words]; // se asegura de que se agregue la ultima letra traducida
  return newString; // retorna el string traducido
}
console.log(decodeMorse("  .... . -.--   .--- ..- -.. .   ")); //TEST
```

## :date: Wednesday exercises
<h3 style="font-size: 20px">1. Valid Parentheses exercise</h3>

Escribe una función que tome una cadena de paréntesis y determine si el orden de los paréntesis es válido. La función debe devolver verdadero si la cadena es válida y falso si no es válida.

Examples:
```
"()"              =>  true
")(()))"          =>  false
"("               =>  false
"(())((()())())"  =>  true
```
```javascript
todavía no hay solucion :(
```

<h3 style="font-size: 20px">2. Convert String To Camel Case exercise</h3>

:scroll: **Description:** Complete el método/función para que convierta las palabras delimitadas por guiones/guiones bajos en mayúsculas y minúsculas. La primera palabra dentro de la salida debe estar en mayúsculas solo si la palabra original estaba en mayúsculas (conocido como Upper Camel Case, también conocido como caso Pascal).

Ejemplos
```
"the-stealth-warrior" se convierte en "the Stealth Warrior"
"The_Stealth_Warrior" se convierte en "The_Stealth_Warrior"
```
Code Solution :ballot_box_with_check:
```javascript
function toCamelCase(str) {
  var ant, letter;
  var string = str.split("").map((p) => {
    //map en lugar del for
    ant == "-" || ant == "_" ? (letter = p.toUpperCase()) : (letter = p);
    //si el val anterior es igual a '-' o '_' --> se convierte el val a mayuscula
    // si no, el val se mantiene igual
    ant = p; // el val anterior ahora es el val actual
    return letter;
  });
  return string.join("").replace(/_|-/g, ""); //se realiza para eliminar '_', '-'
}
console.log(toCamelCase("the-stealth-warrior")); //test
```

<h3 style="font-size: 20px">3. Unique In Order exercise</h3>

:scroll: **Description:** Implemente la función unique_in_order que toma como argumento una secuencia y devuelve una lista de elementos sin ningún elemento con el mismo valor uno al lado del otro y conservando el orden original de los elementos.

For example:
```
uniqueInOrder('AAAABBBCCDAABBB') == ['A', 'B', 'C', 'D', 'A', 'B']
uniqueInOrder('ABBCcAD')         == ['A', 'B', 'C', 'c', 'A', 'D']
uniqueInOrder([1,2,2,3,3])       == [1,2,3]
```
Code Solution :ballot_box_with_check:
```javascript
var uniqueInOrder = (iterable) => {
  var res;
  var copyIter = [...iterable]; //se crea una copia de los parametros

  res = copyIter.filter((w, i) => w != iterable[i + 1]);
  // se filtran cada elemnto de la copia, para comparar con el elemnto próximo de los parametros
  return res; //se retorna el array con los elementos unicos
};

//  tests
console.log(uniqueInOrder("AAAABBBCCDAABBB"));
console.log(uniqueInOrder([1, 2, 2, 3, 3]));
```

## :date: Thursday exercises

<h3 style="font-size: 20px">1. Fold an array
</h3>

:scroll: **Description:** En este kata, debe escribir un método que doble una matriz determinada de números enteros por el medio x veces. La matriz siempre contendrá números y nunca será nula. El parámetro run indica cuántas ejecuciones de plegado tiene que hacer su método.

si el conteo de números es impar, el número del medio se mantendrá. De lo contrario, el punto de plegado está entre los números del medio, por lo que todos los números se sumarían de alguna manera.

Si se pliega una matriz con un elemento, permanece como la misma matriz.La matriz de entrada no debe modificarse.

Un ejemplo dice más que mil palabras:
```
Fold 1-times:
[1,2,3,4,5] -> [6,6,3]

A little visualization (NOT for the algorithm but for the idea of folding):

 Step 1         Step 2        Step 3       Step 4       Step5
                     5/           5|         5\          
                    4/            4|          4\      
1 2 3 4 5      1 2 3/         1 2 3|       1 2 3\       6 6 3
----*----      ----*          ----*        ----*        ----*


Fold 2-times:
[1,2,3,4,5] -> [9,6]
```
Code Solution :ballot_box_with_check:
```javascript
function foldArray(array, runs) {
  var newArray = [...array];
  var count = 0;
  var middle = 0;
  var middleArray, restOfArray, sum, size;
  // mientras el contador sea diferente del numero de vueltas, se realiza...
  while (count !== runs) {
    if (newArray.length == 1) return newArray; //se retorna el mismo array, si contiene un elemento
    middle = Math.round(newArray.length / 2); //parte el array a la mitad...
    middleArray = newArray.slice(0, middle); // y crea un array
    restOfArray = newArray.slice(middle); // con los elemntos restantes, crea otro array
    sizeRA = restOfArray.length; //tamaño del array anterior
    //se modifica el array partido, sumandole los elementos del array restante
    newArray = middleArray.map((x, i) => {
      //map para sumarle a cada elemento
      restOfArray[sizeRA - 1 - i] == undefined //si el elemento no existe en el  array restante
        ? (sum = x + 0) //se le suma 0 al elemento
        : (sum = x + restOfArray[sizeRA - 1 - i]); //si no se le suma el elemento restante
      return sum;
    });
    count++; //aumenta contador
  }
  return newArray; //resultado
}
console.log(foldArray([-9, 9, -8, 8, 66, 23], 1));
```


<h3 style="font-size: 20px">2. Encrypt This! exercise</h3>

:scroll: **Description:** Este kata crear mensajes secretos que puedan ser descifrados. 
1. Su mensaje es una cadena que contiene palabras separadas por espacios.
2, Debe encriptar cada palabra en el mensaje usando las siguientes reglas:
  - La primera letra debe convertirse a su código ASCII.
  - La segunda letra debe ser intercambiada con la última letra
3. Manteniéndolo simple: no hay caracteres especiales en la entrada.

Examples:
```
encryptThis("Hello") === "72olle"
encryptThis("good") === "103doo"
encryptThis("hello world") === "104olle 119drlo"
```
Code Solution :ballot_box_with_check:
```javascript
var encryptThis = (text) => {
  var words = text.split(" ").map((w) => {
    //separo los elemnots del array y recorro cada uno
    if (w.length == 1) return w.charCodeAt(0); // si solo es una letra, retorno su código ASCII
    if (w.length == 2) return w.charCodeAt(0) + w[1]; // retorno el código ASCII del 1ro y el 2do val
    return w.charCodeAt(0) + w[w.length - 1] + w.slice(2, w.length - 1) + w[1];
    // si el elemento tiene 3 o mas letras, retorno con las condiciones anteriores.
  });
  return words.join(" ");
};
console.log(encryptThis("H"));
console.log(encryptThis("He"));
console.log(encryptThis("good"));
console.log(encryptThis("hello world"));
```
<h3 style="font-size: 20px">3. Core Challenge #1
</h3>

***Mission Statement*** :earth_americas::rocket:

> ¡Hola! soy Cindy, una desarrolladora principiante. Me involucrado tanto en la electrónica como en la robótica, pudiendo contribuir en proyectos combinando mis habilidades en hardware y software. Quiero crecer como desarrolladora de software para crear soluciones innovadoras, así como también, colaborar en empresas de servicios IT. Me considero una persona indagadora y comprometida con la mejora continua.
