# :hammer::raised_hands: Week Challenges 3
> *"Siempre parece imposible... hasta que se hace"* 
>***- Nelson Mandela***

## :date: Monday exercises
<h3 style="font-size: 20px">1. Who Likes It? exercise</h3>
 :scroll: **Description:** Probablemente conozcas el sistema de "me gusta" :+1: de Facebook y otras páginas. Las personas pueden "gustar" publicaciones de blog, imágenes u otros elementos. Queremos crear el texto que debe mostrarse junto a dicho elemento.

Implemente la función que toma una matriz que contiene los nombres de las personas a las que les gusta un artículo. Debe devolver el texto de la pantalla como se muestra en los ejemplos:

[]                                -->  "no one likes this"

["Peter"]                         -->  "Peter likes this"

["Jacob", "Alex"]                 -->  "Jacob and Alex like this"

["Max", "John", "Mark"]           -->  "Max, John and Mark like this"

["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"

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

:pushpin::paperclip: **NOTES:** Se resolvió este ejercicio utilizando ***if...else*** anidado, que permite ejecutar una sentencia en base a una condicion especificada, es decir, una decision. 


## :date: Tuesday exercises

## :date: Wednesday exercises

## :date: Thursday exercises