# docker-practice  
docker images: lists all docker images  
docker run --name myapp_c1 myapp: create new container from image myapp with container name of myapp_c1  
docker run --name myapp_c2 -p 4000:4000 -d myapp: same as above but with port exposed on container (right) mapped to port on local machine (left) with detach flag to not block terminal  
docker ps: list running docker containers (add -a to see all containers, running and not running)
docker stop myapp_c1: stop contianer myapp_c1  
docker start myapp_c2: restart a stoppped container  
docker image rm myapp4: delete a docker image (-f to force remove even if being used by a container)  
docker container rm myapp4: delete a container  
docker system prune -a: remove all containers, images and volumes  
docker run --name myapp_c_nodemon -p 4000:4000 --rm -v C:\Users\chakk\Documents\Github\docker-practice\api:/app -v /app/node_modules myapp:nodemon: create volumes for live changes, second volume not mapped anywhere locally to make it persist
