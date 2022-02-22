# Running WebGoat as a container

The following statement can be used to pull and run webgoat as a container:

`docker run -d -p 8080:8080 -p 9090:9090 -e TZ=Europe/Amsterdam --name webgoat webgoat/goatandwolf`{{execute}}

Check to see the status of the container:
`docker ps`{{execute}}

Inspect the logs:
`docker logs webgoat`{{execute}}

Wait until you see the message:
Undertow started on port(s) 8080 (http) with context path '/WebGoat'

