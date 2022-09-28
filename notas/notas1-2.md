# Clase 1:

## Control de versiones:
	que es?
	tipo de sistemas de control de versiones
		1. local
		2. centralizados
		3. distribuido



## 1. local
	Creo carpeta con fecha
	complicado para trabajar en equipo

	Sistema de control de versiones RCS
		diff: <comando> herramienta que te muestra la diferencia entre dos ficheros

## 2. centralizados
	2.1 evolucion del rcs: CVS
	2.2 SUBVERSION (SVN)
	como se utilizan?
		2.1
		en windows, funciones *Tortoise
		cvs -d usuario@servidor.carpeta checkout -P src(rama)
		es seguro, se utiliza en firewalls, routers
		funcionó de forma exclusiva hasta 2010, hay una web donde están los codigos de "emule"
		2.2
		amigable, branch, tag

## 3. distribuido
	git:
		ventajas: en local + servidor
		historial de confirmaciones: ver cambios que han habido 
		commit = confirmacion

> cd prueba-git <br />
git init .  <br />
echo hola > mensaje  <br />
git add mensaje  <br />
git commit -am "commit 1"  <br />
<><br />
git log  (NOTA: los cambios no están en un servidor)<br /> 
cd .git <br />
ls -altr<br />
find .  (NOTA: objects: codigo fuente)<br />
cat index<br />
strings index<br />
<><br />
cd ..<br />
touch nuevo_fichero<br />
git add nuevo_fichero<br />
git commit nuevo_fichero -m "meto nuevo fichero"<br />
git log<br />
<>


## 4. GitHub:

	Para conectar con el servidor utilizamos GITHUB, GITLAB, BITBUCKET, ...:

	Creado el repositorio, tenemos opciones. 
	Los Pull requests los vemos en el workflow
	Solapa insights: ver la actividad de mi repositorio
	wiki: documentar el uso de mi programa
	<>
	Cuando ya tenemos el repositorio git local
	
> git remote add origin <url.config.git><br />
cat .git/config (NOTA: chequear aparicion)

	Convención de nombres de ramas actualizadas:
		- master:main
		- slaves:replicas
		- masters:primary
		- slaves:secondary

-----

# CLASE 2

	Clonar un repositorio

> docker run --name repo alpine/git clone https://github.com/docker/getting-started.git <br />
docker cp repo:/git/getting_started/ .


	Crear una imagen

> cd getting-started<br />
docker build -t docker101tutorial .


	Ejecutar el contenedor

> docker run -dp 80:80 --name docker-tutorial docker101tutorial


	Compartir imagen

> docker tag docker101tutorial /docker101tutorial<br />
docker push /docker101tutorial


	Ingresar a la imagen

> http://localhost/tutorial/