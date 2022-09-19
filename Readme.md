# Se crea la rama "first-development" de esa forma se procede a ajustar la consigna del ejercicio 4 de introducci�n a la programaci�n, a contenidos visto en el curso de Python y de Git. 

Adem�s busco empezar a implementar conocimientos te�ricos de un libro que estoy leyendo llamado "Clean Code". 

# Enunciado del ejercicio

0) En tu propia rama del proyecto deber�s desarrollar esto, y luego hacer merge a la rama main

1) Crear un paquete en Paquete en Python para albergar los objetos que vamos a crear para la consigna propuesta.

2) Crear un objeto "ObjetoIf" que, usando un if, compare si la variable "numeroIf" es positivo, negativo, o cero. Usar __str__

3) Crear un objeto "ObjectoWhile" que, usando un while, este bucle tendr� que tener la variable "numeroWhile" sea inferior a 3, el bloque de codigo debera:
    - Incrementar el valor de la variable en uno cada vez que se ejecute
    - Mostrarlo por pantalla
    crear tu propio metodo con el decorador @classmethod usar cls para definir la clase y anidarlo con __str__

4) Crear un objeto que haga lo mismo que el ejercicio 3, pero solo lo haga una vez

5) Crear un objeto iterable, que usado for, crea un objeto "NumeroFor", esta variable tendr� como valor 0, y su condici�n ser� que la variable sea igual o menor que 3, se ir� incrementando en 1 su valor cada vez que se ejecute y deber� mostrarse por pantalla. Usar "collections" __iter__ y __next__. Podrias usar Context Manager para que despu�s de 3 return None

6) Crear un objeto que funcione como switch, debera retornar la variable estacion, debe haber un caso para cada estaci�n del a�o, y una definida por default en caso que el valor de la variable no sea una estacion.