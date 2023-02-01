# xv2
V2 deploy in Docker

Add enviroment variables UUID

UUID=0e059fce-d6c8-4cc2-9e11-9efff358f8b9


docker build -t xv2 .     #crear imagen docker desde un archivo Dockerfile
docker ps                 #listar todos los contenedores
docker stop xv2           #parar contenedor 
docker exec -it <container name> sh       #terminal del contenedor
docker rmi <tu-imagen-id>           #forzar eliminacion de una imagen
docker rm -v container_name         #Eliminar un contenedor y su volumen
docker logs -f container_name       #ver logs del contenedor

docker run -d -p 3000:3000 -e PORT=3000 -e UUID=0e059fce-d6c8-4cc2-9e11-9efff358f8b9 xv2
#ejecutar una imagen con su variable de entorno
