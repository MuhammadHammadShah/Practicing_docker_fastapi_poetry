# Prerequisite
1. Docker
2. Plugin IDE (VScode) `devcontainer`

## Remote Explorer (at left side bar):
1. Open Foler in Container
  - pre-defined container Configuration Defination.
  - Dockerfile `we select this one`.

###  + new terminal - vs code

## GIFT  
```
linux > python + poetry + codebase live +++++++
```

poetry install 

poetry run uvicorn helloworld.main:app --reload

# "First code"
`#version of our project
version: '1.0.0'
#name of our porject
name : "fastapi"
#main work or service starts from here
services:
#our service name
  api:
#we want to build something
    build: 
    #where the dockerfile is placed as we are building a docker image
      context: ./     #its here outside the compose.yaml
      dockerfile: Dockerfile #named as Dockerfile
    #my container name is:
    container_name: myfastapicontainer
#we can create our own container with commands
    #expose is used for selection of ports 
    ports:
      - 8000:8000   #expose container port 8000 to host port 8000
# " - " is used here syntax for array in json it is used as "[]" but in yaml it is used as "indentation hypan indentation" --> "  -  "`