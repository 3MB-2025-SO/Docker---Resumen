# # Ver contenedores
`docker ps`: ver contenedores corriendo 
	-a : ver contenedores totales

`docker run`: ejecutar un contenedor
	-ti : ejecutarse en primer plano 
	-d: ejecutarse en segundo plano
	
	--name: Darle nombre al contenedor
	--rm: Crea el contendor efimero. Usar CASI siempre

	-v : montar un directorio del sistema al contenedor 
		directorio_host:directorio_contenedor


`docker rm`: borramos contenedores
	-f : forzamos el borrado


`docker image ls`: Lista imagenes
