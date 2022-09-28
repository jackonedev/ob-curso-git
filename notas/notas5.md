# Clase 5

## ETIQUETAS

    Crear etiqueta
> git tag -a v1.1 -m "Version 1.1" (#commit-id.head())<br />

    Publicar la etiqueta server-side:
> git push origin v1.1

    Para ver el nombre del remote "origin"
> cat .git/config:

`(-35:00)`

## GITIGNORE
    .gitignore: recordar de commitear primero y luego va a ignorar los archivos incluidos
    
    Forma de lectura
    
        - #: no lee la linea
        - *blabla: todo lo que termine con blabla
        - blabla*: todo lo que arranque con blabla
        - !blabla: negación de blabla, si está incluido lo excluye
        - doc/cosas: excluye la carpeta cosas
        - doc/cosas/: excluye el contenido de la carpeta cosas

        - cosas/*.mp[3|4]: acepta regex

        - */bin/*: todas las carpetas bin de todos los subdirectorios
        - bin/: el directorio bin de la carpeta main
        - **/

## Trabajar con varios remotes

> git remote add github https://github.com/jackonedev<br />
git remote add gitlab https://gitlab.com/AgustinSt1990<br />
git push github


## Gitear un proyecto

> git init .<br />
git switch -c main<br />
git remote add origin (#url.git)<br />
git add .<br />
git commit -m "Meto todo en git"<br />
git config user.name<br />
git config user.email<br />
git push -u origin main<br />
