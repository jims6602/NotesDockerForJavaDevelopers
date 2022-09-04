# NotesDockerForJavaDevelopers

# Working with Containers and Images

## Creating Image 
```
$ docker pull mongo
```

## Look at the images
```
$ docker images -a
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
mongo               latest              4a3b93a299a7        4 days ago          394MB
```

## Start container
Note "-p" is setting the container port 27017 to local machine port 27017
```
$ docker run -p 27017:2717 -d mongo
```

## Look at the container
```
$ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                                NAMES
3976fa3d9284        mongo               "docker-entrypoint.s…"   50 seconds ago      Up 44 seconds       27017/tcp, 0.0.0.0:27017->2717/tcp   elastic_booth
