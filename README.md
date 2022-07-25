# :tada: Week Challenges 1 


Aquí se encontraran los ejercicios designados a cada semana, organizados por día.

---
# :date: Tuesday exercises
## **1. Lenguajes sde programación compilados e Interpretados** 

Los *compiladores* e *intérpretes* son programas que convierten el código que escribimos a **lenguaje de máquina**, para que lo entienda la computadora. Los lenguajes de programación se puede clasificar en dos tipos, según su naturaleza: El ***lenguaje interpretado*** y  el ***lenguaje compilado***.  
Por ejemplo ***C, C++ y Go*** son lenguajes de programación compilados, mientras que ***JavaScript, Python y Ruby*** son lenguajes interpretados. 

¿Cuál es la diferencia y sus ventajas/desventajas?


| Compiled language | Interpreted language | 
| :----------------- |:-------------| 
| Genera un archivo binario no modificable (ejecutable) | Se escribe en un lenguaje definido y modificable en cada momento
| Las instrucciones se envían directamente al procesador, ya traducidas.      |  Las instrucciones se traducen antes de llegar.      
| Se requiere de un paso extra para que se ejecute el código fuente | El código fuente se ejecuta a través de un solo comando      
| Se ejecuta más rápido. | Se tarda en ejecutar, porque debeb de traducir todo cada vez     | 
| El programa se ejecuta en ciertos equipos o sistemas operativos | El programa funciona en todas las máquinas y sistemas      
| Los errores de compilación impiden que se compile el código. |  Los errores son visibles cuando se inicia el programa    
| Ejemplos: C, C++, Delphi, Go | Ejemplos: Python, Javascript, Ruby, Perl, PHP     

:pushpin: **Nota:**
*La principal diferencia, es que el lenguaje compilado requiere un paso adicional antes de ser ejecutado, **la compilación**, para convierte el código a lenguaje de máquina. En cambio, el lenguaje interpretado, es convertido a medida que es ejecutado.*

## **2. Is Java compiled or interpreted, or both?** 
Por su parte Java es un lenguaje paculiar, porque se compila el código fuente a un lenguaje intermedio llamado **bytecode**, que después es interpretado. Esto con propósito de tener un lenguaje compilado que se pudiera ejecutar sin necesidad de crear varios archivos ejecutables. 

## **3. Pseudocode Currency Converter exercise**
```
START
 
In_dolares <-- INPUT
val_bitcoin <-- 0,000043 INPUT
Conversión < -- In_dólares * val_bitcoin
PRINT Conversión <-- OUTPUT
END
```
## 4.
Three or more...

# :calendar: Wednesday Exercises
## **1. My date of birth the Matrix**

Date: 2003

1 | 1 | 0 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | 1 |
--- | --- | --- |--- | --- | --- | --- | --- | --- | --- | --- 

## **2. MIMPS Exercises**
Código para ejecutar la suma de 2 números ingresados por el usuario:
```assembly
.data
	      number1: .asciiz "\nIngrese el primer numero: "
	      number2: .asciiz "\nIngrese el segundo numero: "
  .text
        main:  
              li $v0, 4	    # avisa que va a imprimir
              la $a0, number1	# prepara lo que va a imprimir
              syscall		# lo manda a imprimir
              
              # le dice a la computadora que espere la entrada del ususario
              li $v0, 5	
              syscall 
              
              # almacena la entrada en un espacio seguro $t0, $t1, $t2...
               move $t0, $v0 
               
              # mismo bloque de intrucciones para los otra entrada
              li $v0, 4
              la $a0, number2
              syscall

              li $v0, 5
              syscall

              move $t1, $v0  
             # realiza la suma en el espacio de memoria $t2
              add  $t2, $t0, $t1

              # bloque final, imprime en pantalla el resultado de la suma
              li $v0, 1
              move $a0, $t2
              syscall
```

Código para que despliegue mi nombre:
```assembly
  .data
        message: .asciiz "\nCindy Saminez\n"
  .text
        main:
              li $v0, 4
              la $a0, message
              syscall
```
# :calendar: Thursday Excercise
## **1. Print special numbers exercise** :1234:
---
<b style="background-color: lightblue; color:black">Loop solution FOR:</b>

```javascript
let str = '';
console.log("Inicia Ccilo For");
for (let i = 0; i <= 100; i=i+2) {  
  str = str + i + ", ";
}
console.log(str);
console.log("fin de la iteracion");
```

<b style="background-color: lightblue; color:black">Loop solution WHILE:</b>

```javascript
//Este bucle, pregunta de primero y luego itera
let n = 0; //contador

console.log("inicio de ciclo While");
while (n <= 100) { //comparacion lógica
  console.log(n); //imprime 
  n += 2; //aumenta
}
console.log("Fin");
```
<b style="background-color: lightblue; color:black">Loop solution DO-WHILE:</b>

```javascript
//Este bucle primero hace y luego pregunta
let i = 0;
console.log("Inicio del Ciclo Do-While");
do {
  console.log(i); //accion
  i += 2; //aumenta 2
} while (i <=100); //comparacion lógica
console.log("FIn");
```

## **2. Bad Code Exercise** :x:
___
What is the error in the code? 
```JAVASCRIPT
var cond = false;

if ((cond = true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```
<b style="background-color: lightgreen; color:black">Answer:</b> :pencil2:

El error es simple, en la comparacion lógica de la iteración, está usando un signo **"="**, el cual se utiliza para ***asignar un valor***, en lugar de **"=="** que es el utilizado para ***una comparacion***, sin olvidar que también existe **"==="** para una ***comparación estricta***.

Correct Code :heavy_check_mark:
```javascript
var cond = false;
if ((cond == true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

## **3. Bad Code 2 Exercise** :x:
Correct the code, so that it follows the following logic and works correctly:

*If the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, it should show the following message : "This issue is almost special." if none of the given conditions are met display the following message: "Only a regular number"*

```javascript
var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
if (n < 1000) {
  console.log('');
} else {
  console.log('Just a regular number');
}
if (n % 10 == 0) {
  console.log('This number is multiple of 10');
}
```
Correct Code :heavy_check_mark:

```javascript
var n = 200; //variable para la comparacion 

//Condicional, verifica si la variable es igual a 100
if (n == 100) {
  //si es igual a 100, imprime en consola que es un especial
  console.log('¡Este es un número especial!');
} else if ((n < 1000) && (n%10==0)){ //si no lo es
	// se verifica si es multiplo de 10
          console.log('Este es casi un número especial');
        }else{ 
        	console.log('Es un número regular');
          //no es multiplo de 10
```
:pushpin: **note:** pruebe cambiando el valor de la variable **"n"** para verificar si se cumplen las diferentes opciones.
___
<mark>Marked text</mark>
<span style="background-color:green">Marked text</span>
<mark style="background-color: lightpink">Marked text</mark>
