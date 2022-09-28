# Clase 6
## Conflictos

Quizás conviene solucionarlos desde la plataforma de GitHub<br />
Cuando se genera el conflicto vemos que en el fichero que se genera primero aparecen multiples "="

    <<<<<<<<< HEAD
    Hola mundo bonito
    ============
    Hola mundo cruel, hace frio hoy
    >>>>>>>>> rama2
    adios personitas


    para elegir una version debo elegir entre:
    1) eliminar desde ============ hasta >>>>>rama2
    2) eliminar desde <<<<<<<<< HEAD hasta ============

    Como elijo la opcion 1 debo eliminar:
    <<<<<<<<<<< HEAD
    =========
    (todas las lineas hasta)
    >>>>>>>>>>> rama2

> git commit -am "Solvento el conflicto"


----
`(-1:50:00 )`

## Resolviendo conflictos en github

    ejemplo 2: (-1:46:00)

    git merge --abort : (-1:38:00)


## Prueba con gitlab
`(-1:19:00)`

-----
<br />

## git checkout, revert, amend, reset, clear
arrancamos a ver los commandos <br />
`(-1:00:00)`

<h3><u>Ver historico los commit</u></h3>
     
     de todas las branches
> git log --branches='*'<br />

    de la rama "rama"
> git log --branches='rama2'

    otros formatos de visualizacion para la rama actual
> git log --oneline<br />
git log --oneline --graph

<br />
<h3><u>git checkout</u></h3>
    
    sirve para ver el estado de un repositorio en un momento dado del tiempo


> git log --online: <i>selecciono</i><br />
git checkout (#i): <i>commit previo</i><br />
git checkout main: <i>para volver</i>


    detached HEAD: 
    
    Cuando mi commit principal está en otro sitio. estoy en otra parte de mi repositorio local. Cualquier modificación que haga va a ir a para al garbage de git, son commit huerfanos. 
    Para hacer eso, lo chequeo y luego creo una rama.

<h3><u>git revert</u></h3>

`(-45:00 )`
    
    Deshacer para atras todos los commits
    No se pierde la información, se hace un contra commit

>git revert (#i)<br />
git revert (#i1) (#i2) ... (#in)

<br />
<h3><u>git amend</u></h3>

`(-37:00)`

> git commit --amend: <i>para cambiar el mensaje del commit</i><br />
git commit --amend --reset-author: <i>previo se debe hacer config local user.name</i>

<br />
<h3><u>git clean</u></h3>

`(-34:00)`

    sirve para hacer limpieza. Se agarra de los que no estan en stage ni existen previamente
>git clean -n: <i>para ver que pasaria</i><br />
git clean -f: <i>lo elimina de verdad</i><br />
git clean -i: <i>modo interactivo, interfaz de texto, elegir que borramos y que no borramos. </i>

<br />
<h3><u>git reset</u></h3>

`(-28:00)`

> reset --soft<br />
reset --mixed:<i> staged area son los ficheros que pasaron por el git add</i><br />
reset --hard: <i>repo</i>

<br />
<h3><u>arboles de git</u></h3>

    1- head
    2- staging area: git ls-files --stage
    3- repositorio en si mismo

<h3><u>reset --hard: </u></h3>

    te lleva al estado donde estaba el último pull-commit

> git log --online:<i> selecciono commit id</i><br />
git reset --hard (#id):<i> no puedo hacer push</i><br />
git push -f: <i>para forzar</i>

<br />
<h3><u>reset --mixed <i>(default)</i></u></h3>

`(-17:30)`

    reset por defecto

> git reset: <i>elimina el staging area pero no elimina el fichero del directorio</i>

<br />
<h3><u>reset --soft</u></h3>

`(-12:00)`

    no elimina el staging area
    Nos mueve al commit y nos muestra el estado

> git commit -am "hola"<br />
git log --oneline<br />
git reset --soft (#i)

<br />
<h3><u>limpieza, tracing: </u></h3>

`(-9:45 )`

    no elimina los ficheros de los commits anteriores

> git rm mensaje.txt<br />
git status: <i> el fichero aparece eliminado</i><br />
git ls-files -s:<i> no aparece en stagin area</i><br />
git commit -am "elimino mensaje.txt"<br />
git push


































