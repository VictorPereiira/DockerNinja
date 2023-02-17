<h1 align = "center">DockerNinja</h1>

<div align="center">  
   <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/victorpereiira/DockerNinja">
   <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/victorpereiira/DockerNinja">
</div>


<p align = "center">
    <a href="#about">About</a>   |
    <a href="#content">Content</a>   |
    <a href="#how-to-contribute">How to contribute</a>   
</p>

<p align = "center">
   <img src="https://user-images.githubusercontent.com/64560823/212745252-a22d645c-6908-418c-806d-7df9b11e8d09.png">
</p>

<div align="center">
    Translate for
    <a href="./github/readme_pt-br.md">PT-BR</a>
</div>


## About
🐱‍👤DockerNinja - Our DockerVerse discoverys. from [StudyVerse](https://github.com/VictorPereiira/StudyVerse)


## Project Targets

### Docker Study

1. To learning how to create a DockerFile.
    1. Docker Image
2. To learning how to work with Docker CLI.
    1. Docker Container.
    2. Docker Network.
    3. Docker Volume.
3. To learning how to work with Docker Compose.

### DockerNinja Github Repository

1. Take notes of docker study.
2. Create Docker Cheatsheet.
3. Create Docker Challenges.

### DockerTools

1. 

## The Ninja Mode
```markdown
$Group1 = <image> || <container> ||  <network>

// Combo
docker inspect <image_id> ||  <container_id>         -> Display infomation.
docker <$Group1>  prune                              -> Remove unused elements.
```

## Content

### What its?

1. In the Docker File
    1. What is the difference between `ADD` and  `COPY` ?
    2. What is the difference between `ENV` and  `ARG` ?
    3. What is the difference between  `RUN` , `CMD`and  `ENTRYPOINT` ?
    4. How to work Volume Bind Mounts ?

- To do
    - [ ]  Push a image to Docker Hub
    - [ ]  Push a image to AWS ECS
    - [ ]  Search what is `docker attach`
    - [ ]  Search how to update `docker conatiner`
    - [ ]  Seach hw to work with a `docker user`
    - [ ]  Complete docker compose study
    - [ ]  Search info notes

### How to do

1. How to create a dockerfile.
2. How to work with docker images.
3. How to work with docker containers.
4. How to work with docker network.
5. How to work with docker volume.
6. How to work with docker arguments and env.
7. How to work with docker users.
8. How to work with docker compose.

- How to create a dockerfile.
    
    ```docker
    FROM <image>
    LABEL <metadada>
    
    WORKDIR <path>
    ENV <key> <value>
    ARG <key>=<value>
    
    RUN useradd -ms /bin/bash <user_name>
    USER <user_name>
    
    COPY || ADD <currenty_paht/file> <dentination>
    EXPOSE <port>
    CMD ["<service>", "<action>"]
    ```
    

- How to work with docker images.
    
    ```markdown
    docker build <context>                         -> Create a image from dockerFile.
    docker docker images                           -> List images.
    docker inspect <image_id>                      -> Display infomation.
    docker history <image_id>                      -> Display history.
    ...                                            -> Update atributes.
    docker rmi (<image_id> || <image_repository>)  -> Remove.
    docker image prune                             -> Remove unused images.
    
    docker pull   -> Pull an image from a registry.
    docker push   -> Push an image to a registry.
    ```
    

- How to work with docker containers.
    
    ```markdown
    docker run -d --name <container_name> -p <port> <image_id>  -> Create a container
    
    docker ps -a                   -> List containers.
    docker update <container_id>   -> ...
    docker rename <new_name>       -> Rename.
    docker rm <container_id>       -> Remove.
    docker container prune         -> Remove unused containers.
    
    docker inpect <container_id>   -> Display information.
    docker logs <container_id>     -> Display logs.
    docker diff <container_id>     -> Inspect changes.
    docker stats <container_id>    -> Display statistics.
    docker top  <container_id>     -> Display process.
    
    docker start <container_id>     -> Start.
    docker restart <container_id>   -> Restart.
    docker pause <container_id>     -> Pause.
    docker unpase <container_id>    -> Unpause.
    docker stop <container_id>      -> Stop.
    docker kill                    -> Kill running containers.
    
    docker exec -it <container_id> bash || sh   -> Access a container.
    docker attach                               -> ...
    docker commit <container_id>                -> New image container's changes.
    docker port <empty> ||<container_id>        -> Mapping ports.
    ```
    

- How to work with docker network.
    
    ```markdown
    docker network create  -> Create.
    
    docker newtowk ls            -> List Networks.
    docker inpect <network_id>   -> Display information.
    docker rm <network_id>       -> Remove.
    docker network prune         -> Remove unused networks.
    
    docker run -d  -it --name <container_name> -p <port> --network <network> <image> <cmd>
    
    docker network (<connect> || <disconect>) <network_id> <conatiner_id> -> Connect or Disoconect.
    ```
    
- How to work with docker volume.
    
    ```markdown
    docker volume create <volume_name>   -> Create.
    
    docker container run -d --name <name> -v <volume_name>:<target> <image>
    
    docker volume ls              -> List Networks.
    docker inpect <volume_name>   -> Display information.
    docker rm <volume_name>       -> Remove.
    docker volume prune           -> Remove unused networks.
    
    /var/lib/docker/volumes/               -> Linux Storage location.
    c:\ProgramData\Docker\windowsfilter\   -> Windows Storage location.
    ```
    
- How to work with docker arguments and env.
    
    ```markdown
    --build-arg <key>=<value>   -> Build-Time Variable.
    --env <key>=<value>         -> Build-Time Enviroment Variable.
    ```
    
- How to work with docker users.
    
    ```markdown
    content here...
    ```
    

- How to work with docker compose.
    
    ```markdown
    docker-compose --version   -> Get docker compose version.
    
    docker-compose build      -> Build Services.
    docker-compose up -d      -> Create and Start containers.
    docker-compose create     -> Create containers for a service.
    docker-compose ls         -> List services containers.
    docker-compse ps          -> ...
    docker-compose images     -> List images used by the created containers.
    docker-compose rm         -> Remove unused service containers.
    
    docker-compose events   -> Real Time events.
    docker-compose top      -> Display the running processes
    docker-compose logs     -> Display logs.
    
    docker-compose start     -> Start.
    docker-compose stop      -> Stop.
    docker-compose restart   -> Restart.
    docker-compose pause     -> Pause.
    docker-compose unpause   -> Unpase.
    docker-compose kill      -> Kill
    docker-compose down      -> Stop and remove containers, networks.
    
    docker-compose exec
    docker-compose port
    docker-compose pull
    docker-compose push
    ```
    

### Notes

`ONBUILD`

`HEALTHCHECK`

`SHELL`

## How to contribute
- Make a fork;
- Create a branch with your feature: `git checkout -b my-feature`;
- Commit changes: `git commit -m "feat: my new feature`;
- Make a push to your branch: `git push origin my-feature`.

<p>After meging your receipt request to done, you can delete a branch from yours.</p>

#
<p align = "center">
    Made by 👨🏾‍💻
    <a href="https://github.com/VictorPereiira">VictorPereira</a>
</p>


