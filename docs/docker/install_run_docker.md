#### Commands to run on the VM Instance

1. Install Docker

```
$ sudo apt-get install docker.io
```

2. Pull nginx image

```
$ sudo docker pull nginx:1.10.0
```

3. Check Docker images

```
$ sudo docker images 

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
nginx               1.10.0              16666ff3a57f        3 years ago         183MB

```

4. Run the first instance

```
$ sudo docker run -d nginx:1.10.0
```

5. check that it's up and running

```
$ sudo docker ps

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
370f8462ba56        nginx:1.10.0        "nginx -g 'daemon of…"   5 seconds ago       Up 4 seconds        80/tcp, 443/tcp     thirsty_hugle

```

6. Run a different version of nginx (if it's not available on your machine locally then docker will automatically pull it and then create a docker instance)

```
sudo docker run -d nginx:1.9.3
```

7. Check how many instances are running

```
$ sudo docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
3d3d3bcf8b5d        nginx:1.9.3         "nginx -g 'daemon of…"   20 seconds ago      Up 19 seconds       80/tcp, 443/tcp     infallible_goodall
370f8462ba56        nginx:1.10.0        "nginx -g 'daemon of…"   42 seconds ago      Up 41 seconds       80/tcp, 443/tcp     thirsty_hugle

$ sudo docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
nginx               1.10.0              16666ff3a57f        3 years ago         183MB
nginx               1.9.3               ea4b88a656c9        4 years ago         133MB

```

What's with the container names?
If you don't specify a name, Docker gives a container a random name, such as "stoic_williams," "sharp_bartik" etc
 
These are generated from a list of adjectives and names of famous scientists and hackers. https://github.com/moby/moby/blob/master/pkg/namesgenerator/names-generator.go