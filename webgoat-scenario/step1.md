# Running WebGoat as a container

The following statement can be used to pull and run webgoat as a container:

`docker run -d -p 8080:8080 -p 9090:9090 -e TZ=Europe/Amsterdam webgoat/goatandwolf --name webgoat`{{execute}}

Check to see the status of the container:
`docker ps`{{execute}}

Inspect the logs:
`docker logs webgoat`{{execute}}
