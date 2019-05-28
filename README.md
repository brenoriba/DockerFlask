# Docker + Flask: a simple tutorial

## Setup

Download and install Docker for Desktop:
```
https://www.docker.com/get-started
```

Build our docker image:
```
docker build -t docker_flask:latest .
```

Run container:
```
docker run -d -p 5000:5000 docker_flask:latest
```

However this has a few pieces I think are important. First thing is -d which detatches from the run. This means you won’t see any output. You can remove the -d if you would like to see the run process.

Next is -p which specifies the port it is going to run on. In out app.py file we used app.run(debug=True, host=’0.0.0.0') so we needed to specify which port when using flask run , which above you can see I used 5000.

Open on browser:

```
http://127.0.0.1:5000/
```

## Useful commands

Check created docker images:
```
docker images
```

Check running images:
```
docker ps
```

Kill a container:

```
docker kill <CONTAINER ID>
```