# Kubernetes Intermediate Training

## Signup for Cloudyga

- Create an account at https://cloudyuga.guru
- Attempt Pre-tests
    - https://cloudyuga.guru/site_quizzes/basic-containers-docker
    - https://cloudyuga.guru/site_quizzes/basic-kubernetes
- Sign up for the Docker Course 
    - https://cloudyuga.guru/courses/container-fundamentals-with-docker
    - Use coupon code "FKDOCKER" to enroll for free 

## Commands

```
 sudo apt update
 sudo apt install docker.io
```

```
 sudo docker container ls
```

```
 sudo docker container run -i -t alpine sh
 ```
 
 ```
  sudo docker container ls
  sudo docker container ls -a
  sudo docker container run --name web -d nginx:alpine
    sudo docker container inspect web
  ```
 
 ```
  sudo docker container run -i -t --name myalpine alpine sh
  
  Ctrl + p + q
  ```
  ```
  sudo docker container diff myalpine
  sudo docker container commit myalpine  myimage  
   sudo docker container run -i -t myimage:latest sh
  ```
  
  
 ```
 mkdir workshop
 cd workshop 
 cat Dockerfile
 $ cat Dockerfile
   FROM alpine:latest
   RUN date > file
 ```
 
```
 sudo docker image build -t myimage:dockerfile .
 ```
 
 ```
 mkdir src
 touch src/f1

 $ cat Dockerfile
 FROM alpine:latest
RUN date > file
COPY src /tmp
 ```
 
 https://docs.docker.com/engine/reference/builder/
 
```
 $ cat Dockerfile
FROM alpine:latest
RUN date > file
COPY src /tmp
CMD ["/bin/ls", "/tmp"]
```

```
 cat Dockerfile
FROM alpine:latest
RUN date > file
COPY src /tmp
ENTRYPOINT ["/bin/ls", "/tmp"]
```


```
 sudo docker network create myn
```

```
$ sudo docker container run -d --net=mynet --name=backend  nginx:alpine
```

```
$ sudo docker container run -d -p 8080:80 nginx
```