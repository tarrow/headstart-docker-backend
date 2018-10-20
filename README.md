## Example usage

First install docker, then build the image

```
cd <path/to/headstart-docker-backend>
docker build -t headstart ./
```

This takes some time ~10min.

Run the image

```
docker run --rm -d -it --name=headstart -p 8080:80 -v <path/to/headstart/repo/>:/var/www/html/ headstart:latest
```

Now you can got to localhost:8080 and test Headstart.

See running containers

```
docker ps
```

Enter container shell

```
docker exec -it headstart bash
```

Follow server logs

```
docker logs headstart --follow
```

Kill a running container

```
docker kill headstart
```
