docker ps: ver contenedores corriendo 
	-a : ver contenedores totales

docker run:
	-ti : ejecutarse en primer plano 
	-d: ejecutarse en segundo plano

	--name: Darle nombre al contenedor
	--rm: Crea el contendor efimero. Usar CASI siempre

	-v : montar un directorio del sistema al contenedor 
		directorio_host:directorio_contenedor

	-e: Inyectar variables de entorno al contenedor

	nombre_imagen:


docker rm: borramos contenedores
	-f : forzamos el borrado


docker image ls: Lista imagenes

docker exec: ejecutar un comando en un contenedor existente
	-ti o -d 
	docker exec -ti nombre_contenedor comando
	





docker run -ti --rm \
	--name rocky-linunxito \
	-v $(pwd):/datos \
	rockylinux:9



docker run -ti --rm \
	--platform=linux/amd64 \
	--name aplicacioncita \
	-v $(pwd):/var/www/html \
	-e DB_HOST="192.168.1.35" \
	-e DB_USER="root" \
	-e DB_PASS="1234" \
	-e DB_NAME="basesita" \
	-p 10500:80 \
	ggmartinez/php:8.3-apache


docker run -ti --rm \
	-e MYSQL_RANDOM_ROOT_PASSWORD=true \
	-e MYSQL_USER="jacinto" \
	-e MYSQL_PASSWORD="1234" \
	-e MYSQL_DATABASE="base" \
	--name mysql2 \
	-p 3307:3306 \
	mysql:8




docker run -ti --rm \
	-e MYSQL_RANDOM_ROOT_PASSWORD=true \
	-e MYSQL_USER="pepito" \
	-e MYSQL_PASSWORD="1234" \
	-e MYSQL_DATABASE="otra-base" \
	--name mysql3 \
	-p 3308:3306 \
	mysql:8


