# Clase 4 Parte 3

## Git Stash: modo No molestar
`(-1:05:00)`

    Modo 1:
    Me creo una copia del directorio de trabajo, hago un hard reset y pierdo los cambios

    Modo 2: 
    directorio de trabajo limpio

<h3><u>Modo 2</u></h3>

> git stash: <i>crea un directorio limpio con ID*</i><br />
git status: <i>está stasheado*</i>

    Hago modificaciones, commiteo y luego:

>git stash apply:<i> luego puedo seguir trabajando*</i>
<br/>

<h3><u>Multiplestashes</u></h3>

> git stash list

    Limpiar los stash luego comiteados

> git stash clear

    Crear un stash con nombre

> git stash save "estoy creando el loggin"

`(-55:55)` revovinar
> git stash pop 

    Luego del apply va el clear
--------
<br />

## Cherry pick

    En vez de fusionar ramas completas, voy a fusionar commits concretos. Sirve para ir commiteando pasos anteriores al actual de la rama 

>git checkout ramaurgente<br />
git log: <i>busco el #id del commit</i><br />
git checkout master<br />
git cherry-pick #i<br />
<><br />
git log --oneline: <i>puedo seleccionar mas de uno</i><br />
git checkout main<br />
git cherry-pick #i1 #i2<br />
<><br />
git log --oneline: seleccionar un rango I<br />
git checkout main<br />
git cherry-pick #i1^..#i3: <i>los incluye</i><br />
<><br />
git cherry-pick --abort <br />
git cherry-pick --quit<br />
<><br />
git log --oneline: <i>seleccionar un rango II</i><br />
git checkout main<br />
git cherry-pick #i1..#i4: <i>los excluye</i><br />

    Sirve para emigrar de la Version 1.x a la version 2.0, porque sobre la nueva app le commiteas los commits del cherry-pick del v1.
--------
<br />

## WORKFLOW GIT
`(-41:00)`
    
    Es una convencion de trabajo

    1. Forma estandar

        update -> change -> review -> commit

    1.1 
        git fetch: chequea si hay cambios
        git pull: chequea si hay cambios y los trae

    1.2
        Trabajo en directorio de trabajo

    1.3
        git diff: que cambio no has enviado aun

    1.4
        git commit -am "cambios"


    2. Forking workflow: clonar un repositorio remoto, hacer cambios, y solicitar que meta los cambios

    2.1 Ir a github y buscar un repositorio


    2.2 Hacer un fork
        Fork: clonar el repositorio en mi cuenta de usuario

    2.3 Clonar en mi repositorio local

    2.4 Trabajar

    2.5 Hacer push a tu repositorio remoto

    2.6 En GitHub: Crear una pull request - Contribute - open pull request

    2.7 (La otra parte deberia hacer Merge Pull Request)



## Comportamiento de git

    local-side o server-side

    1) local-side
    
    hooks: ficheros escritos en un lenguaje de programación, pero que podamos ejecutar, donde estan? en el repo hooks, y los dir son .sample, si no fuera .sample se ejecutaria automaticamente

    ficheros hooks.__dir__:

        1ro. pre-commit
        2do. prepare-commit-msg: alterar el texto de los commits
        3ro. commit-msg: manipular el mensaje de commit : se quejaría que haya muchos cambios con la misma firma
            commit -s: incluye la firma
        4to. post-commit: enviar correos electrónicos
        5to. post-checkout


    2) scripts server-side
        PRE-RECEIVE
        UPDATE
        POST-RECEIVE: se ejecuta una vez se haya ejecutado los cambios. Que me envie un mail cuando se modifique.







































































