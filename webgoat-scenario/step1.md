# Running WebGoat as a container

The following statement can be used to pull and run webgoat as a container:

`docker run -d -p 8080:8080 -p 9090:9090 -e TZ=Europe/Amsterdam --name webgoat webgoat/goatandwolf`{{execute}}

# Check the status
Check to see the status of the container:
`docker ps`{{execute}}

Wait for the ports to become available:

`timeout 30 bash -c 'until printf "" 2>>/dev/null >>/dev/tcp/localhost/8080; do sleep 1; done'`{{execute}}

Or check that the ports are used by:

`netstat -na|grep 0.0.0.0 |grep LIST`{{execute}}

Inspect the logs:
`docker logs webgoat`{{execute}}

Wait until you see the message:
Undertow started on port(s) 8080 (http) with context path '/WebGoat'

# Explore the gui

Open the WebGoat UI:

Use the link next to the terminal or this one: [WebGoat](https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/WebGoat)
