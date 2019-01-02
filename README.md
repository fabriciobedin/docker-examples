### Add Docker in CMDER
+ 1º Open CMDER
+ 2º Menu -> Settings / Win + Alt + P
+ 3º Add new task in Startup -> Tasks
+ 4º Past the directory of the docker in task parameters \
`/dir "C:\Program Files\Docker Toolbox"`
+ 5º Past the arguments of the docker in Commands - Params \
`"C:\Program Files\Git\bin\bash.exe" --login -i -new_console:C:"C:\Program Files\Docker Toolbox\docker-quickstart-terminal.ico" "C:\Program Files\Docker Toolbox\start.sh"`
+ 6º Save and enjoy :)

### Commands
__`docker run -ti --rm --name example -p 8080:8080 -v ~Desktop/example --net=network_name ubuntu bash`__
  
| Argument                 | Description                                                                                      |
| ------------------------ | -----------------------------------------------------------------------------------              |
| -ti                      | Iterative mode, it leaves you know about what is happening while docker is running.              |
| -rm                      | Remove files after stop container.                                                               |
| --name container_name    | Name of the container.                                                                           |
| -p 8080:80               | Map TCP port 80 in the container to port 8080 on the Docker host.                                |
| -p 192.168.1.100:8080:80 | Map TCP port 80 in the container to port 8080 on the Docker host for con. to host 192.168.1.100. |
| -p 8080:80/udp           | Map UDP port 80 in the container to port 8080 on the Docker host.                                |
| -v ~Desktop/example      | Create ephemeral volume.                                                                         |
| -v ~Desktop/ex:/example  | Create persistent volume.                                                                        |
| --net=network_name       | Use one common network shared between other containers. (docker network create network_name)     |
| -c "lose /etc/password"  | Open console in especific path.                                                                  |
| --volumes-from cont_name | Get the same volumes of especific container.                                                     | 
| ubuntu                   | Name of the image. (see all images in https://hub.docker.com/)                                   |
| bash                     | Open bash console while the container is running.                                                |


| Command                   | Description                                                                                      |
| ------------------------- | -----------------------------------------------------------------------------------              |
| docker info               | List all the informations about the containers.                                                  |
| docker ps                 | List all containers running.                                                                     |
| docker ps -a              | List all containers running and stopped.                                                         |
| docker attach cont_name   | Open container.                                                                                  |
| docker logs cont_name     | See all the logs information about one especific container.                                      |
| docker kill cont_name     | Stop container.                                                                                  |
| docker rm cont_name       | Remove container.                                                                                |
| docker rmi image-name:tag | Remove image by name.                                                                            |
| docker rmi image-id       | Remove image by id.                                                                              |
| docker network create ex  | Create a new network.                                                                            |
