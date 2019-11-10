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