# Clase 4 Parte 1

## git reset, git diff, git bisect, git blame



> cd miapp<br />
git init .<br />
git status<br />

> touch mifichero.txt<br />
git add mifichero.txt<br />
git commit -am "meto mifichero.txt"<br />
git log --oneline: <i>Para ver donde quiero retroceder*</i><br />

> echo mensaje > mifichero2.txt<br />
echo otromensaje > mifichero3.txt<br />
git commit -am "meto mifichero2.txt y mifichero3.txt"<br />

<h3><u>git reset</u></h3>

> git reset --soft HEAD~(#i):<i> apuntar el HEAD a (#i) commits para atras*</i> <br />
git reset --hard HEAD~(#i): <i>apuntar el HEAD a (#i) commits para atras*: no solo movimos la historia, elimina los cambios hechos dentro de git.</i>

> git reset --hard: <i>retorna al HEAD</i>

<h3><u>git diff</u></h3>

> git diff: <i>muestra la diferencia entre la copia de trabajo (carpeta) y el repo local (subcarpeta .git)</i>

<h3><u>git bisect</u></h3>

    git bisect: corregir si algun commit ha podido romper algo
    git commit -am "Texto"
    git commit -am ""...
    ...

> git log --oneline: <i>vemos los commits, buscamos el bueno </i><br />
git bisect start<br />
git bisect good (#commit): <i>el key del commit bueno</i><br />
git bisect bad (#commit): <i>el key del commit malo. Tener en cuenta las "revisiones". Por default dejarlo en blanco considera el útlimo como el malo*</i>

<h3><u>git blame</u></h3>

    git blame: quien ha hecho qué.
    es pesado a nivel disco duro

> git blame mifichero.txt: <i>dentro de este fichero, quien introdijo, cuando, qué cambio.</i>

`(-1:55:00)`