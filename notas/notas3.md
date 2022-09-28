# CLASE 3

## 1- creando un repositorio

>cd miapp<br />
git init .<br />
git add . <b><i>or</i></b> git add src<br />
git config --system <b><i>or</i></b> --global <b><i>or</i></b> --local:<i> para modificar</i><br />
git config --list --global <b><i>or</i></b> --local:<i> para chequear</i>

	el fichero que modificamos está en .git

> cat .git/config <br />
cat $HOME/.gitconfig:<i> es el --global </i><br />
cat /etc/gitconfig:<i> es el --local</i>

<br />
<h3><u>Como cambiar el config</u></h3>

> git config --global user.name "Un string"

	El user.name de local es el que uso para hacer commit en el repositorio actual,
	el user.name del global es cuando queremos hacer commit en repositorios externos

<br />

<h3><u>Como hacer un commit por terminal</u></h3>

> git commit -a: <i>commitear todo</i> <br />
press i: para insertar comentario <br />
press ESQ: para salir de i <br />
press :wq: para salir (write and quit) <br />

<br />

	post2
> rm -rf .git:<i> meter todo en git</i>

----------------------------
<br />

## 2- creando un repositorio --bare

> cd Repositorio<br />
git init --bare aplicacion: <i>aparecen cosas adicionales para contener informacion de git que no va a ser la carpeta donde trabajemos</i>

	Metodología de trabajo:
		1- Teniendo un directorio "miapp" que contiene repositorio existente
		2- vamos al directorio de windows, 
		3- cambio el nobmre de "miapp" a "miapp.origin",
		4- clono el bare bajo el nombre "miapp"

> cd miapp.origin <br />
git clone ../Repositorio/aplicacion miapp <br />
cd miapp: <i>puedo ver funciones nuevas.</i>

	CONCLUSION:
		A partir de ahora tengo un git dentro de mi repositorio, un git local

`(-46:00)`

	ejemplo 2:
	Crear un repositorio fuera de mi carpeta

> git init --bare miapp

	Luego lo clonamos a una carpeta donde queremos trabajar con ellos


`(-37:43) y entramos en VSCode`

`(-29:40) vemos el tema del conflicto, gana el primer push`

`-20:00`
	
	- git tower:
		git-tower.com
	- git kraken
	- TortoiseGit: ideal para windows
--------------
<br />

## 3- Etiquetas: git tag
	Se definen como versiones de commit sintacticas

> git tag -a: <i>etiquetas gordas: contienen ciertos metadatos. Autor de la etiqueta, email del autor, y fecha de la etiqueta.</i><br />
git tag:<i> etiquetas ligeras: contienen menos informacion</i>

	proyectos opensources usamos -a, para projectos locales usamos -a

<h3><u>Publicar Tag</u></h3>

> git tag -a v1.0: <i>puedo agregar el numero de version del commit o dejarlo vacio</i><br />
git commit -am "Version 1.0"<br />
git push origin v1.0
>> git branch -l: <i>para ver las ramas existentes</i><br />
git checkout v1.0: <i>Para retomar desde la etiqueta</i>


`(-12:22)` 
	
	prueba el software Fork y muestra la etiqueta, si querés ver el estado de un commit tag

`(-7:30)`

	Como hacer para volver a una version del pasado:
	copiamos los primeros digitos de la firma del commit

	git revert ###### -- (mirar notas 6 - conflictos)

	está mal visto modificar el histórico

	Como hacer para eliminar un fichero:
	
	git rm filename.ft
	git commit -am "elimino el fichero"
	
	
	git reset --hard : Acá podemos ver que recuperamos un fichero eliminado pero no commitiado (!)


