docker run -p 3375:2375 -v /var/run/docker.sock -d shipyard/docker-proxy
# Paso a paso
Este paso  a paso requiere tener un conocimiento previo acerca de dockers.
## 1.-Montar jenkins 
A traves de docker compose montar Jenkins,y dentro de Jenkins consultar la version de linux e instalar dockers dentro de la maquina. Al mismo tiempo montar SonarQube, 
a traves de docker compose usuario default admin
docker exec -it -u root container bash te da acceso a superusuario
instalar sudo dentro de jenkins
https://docs.docker.com/engine/install/debian/--> Instala docker en jenkins
sudo chmod 666 /var/run/docker.sock
## 2.- Instalar Plugins
Dentro del administrador de Jenkins instalar el plugin Sonar scanner. Entrar al container de jenkins e instalar SonarScaner por comandos.