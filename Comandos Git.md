#Comprobar Versión Instalada
	git --version

#Vincular una carpeta con un repositorio git
	git --init

	/***Este comando se ejecuta 1 sola vez por cada proyecto, de forma oculta
	creara un repositorio y se debe ejecutar dentro de la carpeta que queremos vincular***/

#Ver el seguimiento de cada archivo
	git status -s

	/***Con este comando vemos en que status se encuentra cada archivo***/
	Si el archivo tiene 2 signos de interrogación (??) significa que no ha sido añadido aun al area temporal.

#Añadir archivos al Area Temporal
	-> git add nombre_del_archivo

	/***Con este comando se añaden archivos al Area Temporal, luego de esta area pasan al area de Repositorio Local para luego (si queremos) pasar al area de Repositorio Web***/
	Los archivos añadidos al Area Temporal apareceran con una letra (A) delante (la A significa Añadido). Luego de ejecutar el comando git add nombre_del_archivo. Podemos verificar que se agregó correctamente con el comando git status -s

	-> git add . 
	(con este comando agregamos TODOS los archivos de la carpeta del Area Temporal)

#Guardar una copia del o los archivos que queremos respaldar
	git commit -m "Aquí se escribe un mensaje referente al archivo o los archivos agregados"


#Subir el repositorio a Github.com
	1. Lo primero es entrar a nuestra cuenta Github y crear el repositorio donde subiremos nuestro proyecto
	este repositorio puede ser publico o privado. Por lo general es privado es un sistema para alguna empresa.

	2. Luego de esto una vez ejecutados los comandos:
		-> git init (Se ejecuta 1 sola vez dentro de la carpeta del proyecto)
		-> git add .
		-> git commit -m "Comentarios importantes para identificar la versión"
	
	**CUANDO ES UN REPOSITORIO PÚBLICO
	3. Apuntamos el proyecto al repositorio en la nube
		-> git remote add origin "https://github.com/CarlosCastle/MIREPOSITORIO.git"
		-> git push -u origin master

		/*** Si aparece este mensaje: fatal: remote origin already exists
		Ejecutas:

		-> git remote rm origin

	**CUANDO ES UN REPOSITORIO PRIVADO
		Apuntamos el proyecto al repositorio en la nube
		-> git remote add origin git@github.com:CarlosCastle/prueba.git
		-> git push -u origin master

		/*** Si aparece este mensaje: fatal: remote origin already exists
		Ejecutas:

		-> git remote rm origin

#Volver a una version Anterior del proyecto
	1. Para volver a una Versión Anterior lo primero que debemos hacer es listar nuestro commit para identificar la versión a la que queremos retroceder
		-> git log --oneline

	2. Luego que vemos el listado de commint nos fijamos en el ID de la versión a la que queremos volver y copiamos su ID
		-> git reset --hard ID
		Ejemplo: git reset --hard 3419ed75

#Clonar un repositorio
	-> git clone https://github.com/CarlosCastle/MIREPOSITORIO.git

#CLONAR RAMA DE UN REPOSITORIO
	-> git clone https://github.com/CarlosCastle/comandos_git -b nombrerama --single-branch

	¡Dios es bueno!
	¡Dios es Grande y Poderoso!

