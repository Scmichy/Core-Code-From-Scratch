# :tada: Week Challenges 1 


Aquí se encontraran los ejercicios designados a cada semana, organizados por día.

---
# :large_blue_circle: Tuesday exercises
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

<span style="background-color:green">Nota:</span>
*La principal diferencia, es que el lenguaje compilado requiere un paso adicional antes de ser ejecutado, **la compilación**, para convierte el código a lenguaje de máquina. En cambio, el lenguaje interpretado, es convertido a medida que es ejecutado.*

## :large_blue_circle:**2. Is Java compiled or interpreted, or both?**
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

# :large_blue_circle: Wednesday Exercises
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
# :large_blue_circle: Thursday Excercise
## **1. Print special numbers exercise**
---

## **2. Bad Code Exercise**
___

## **3. Bad Code 2 Exercise**
___
<mark>Marked text</mark>
<span style="background-color:green">Marked text</span>
<mark style="background-color: lightpink">Marked text</mark>
==higlight==