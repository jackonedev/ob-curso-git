# Clase 4 - Parte 2
## Ramas de git
`(-1:55:00)`

    Ramas: Historiales de confirmaciones paralelos, que no se cruzan entre ellos
        - ramas para corregir un error

>cd miapp<br />
git branch:<i> mostrar ramas actuales*</i><br />
git status<br />
>>git branch (#feature): <i>crear rama #feature: debe tener un commit antes al menos</i><br />
<b><i>or</i></b><br>
git checkout -b (#feature): <i>cambia a la rama feature y si no existe la crea</i>


    git checkout (#feature):para cambiar de rama*

    #git checkout main:para commitear la rama main*


<h3><u>Crear rama desde un commit previmente existene</u></h3>

> git log --oneline: <i>selecciono commit id</i><br />
git branch nueva-rama #commit-id


<br/>
<h3><u>Crear una rama de otra rama</u></h3>

> git checkout feature-demo<br />
git checkout -b (#feature) feature-demo: <i>desde feature-demo sale la rama feature</i>


<br/>

## Trabajar con branches remotes
> git pull origin NOMBRE_DE_LA_RAMA: <i>repositorio remoto de github, gitlab</i><br />
git checkout NOMBRE_DE_LA_RAMA

<br />

# 2. git merge, git rebase
`(-1:27:00)`
<h3><u>Trabajando con repositorios remotos, unificando las ramas</u></h3>

    Convención:
        - repositorios compartidos(publicos): git merge
        - repositorios para nosotros mismos: git rebase
            
            touch master2.txt: crea un fichero llamado master2.txt


<h3><u>git merge</u></h3>

> git merge (#feature):<i> la rama master fusiona la rama feature con metodo pass forward/freeway merge: 1. historial plano 2. cuando ya hay commits posteriores*</i><br />
git commit -am "Hago merge"


<h3><u>Git rebase</u></h3>
    
    es hacer un merge sin alterar el historial de confirmaciones*

> git rebase feature<br />
:wq<br />
git log --oneline --graph









