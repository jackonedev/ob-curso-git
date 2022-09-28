# Clase 7

## GIT WORKFLOW

    Se crean las siguientes branches:
    - main
    - hotfixes
    - release branches
    - develop
    - feature branches

        >> main Tag 0.1

        >> develop: el grueso del desarrollo continuo

        >> feature branches: características: autenticacion de usuarios (rama login), registro auditorias (rama audit), siempre se fusiona con la rama develop

        >> branches release: preparar una salida a producción. bug fixed only - lo que arreglamos en la rama release lo fusionamos a la rama develop (cherry pick). Cuando release es estable: listo, fusionamos release en main, y tageamos

        >> hotfixes: se crean cuando hay un bug en la rama master. Apenas se corrige se fusiona con main y se tagea


## instalar gitflow 
`(-43:50)`

<h3><u>Iniciar un repositorio con flow</u></h3>
> git flow init<br />
git flow feature list<br />
<><br />
git flow feature start <name>: <i>creo login.php</i><br />
git add login.php<br />
git commit login.php -m "version inicial"<br />
git flow feature finish <name><br />
<>

<br />
<h3><u>pasar a la version 0.1</u></h3>
> git flow release start 0.1: <i>modificamos los ficheros para listos para produccion</i><br />
git flow release finish 0.1

<br />
<h3><u>hotfix</u></h3>
> git flow hotfix start hotfix_1:<i> modificamos los ficheros para listos para produccion</i><br />
git flow hotfix finish hotfix_1


`(-25:50)`

> rm -rf gitflow-*

`(-24:33)`

## instalando gitflow en ubuntu

`(-23:00)`

## instalando gitflow en windows

    ingresamos a gitbash

    IMPORTANTE EJEMPLO!

`(-11:53)`

    borro todo

> rm -rf * .git