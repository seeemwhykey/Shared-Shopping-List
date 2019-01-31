# Docker-Compose
Build the docker images with

    docker-compose build

Start the docker images with

    docker-compose up
Point your browser to http://localhost:8080

Stop the docker images with
    docker-compose down

# Docker
Instead of using docker-compose you can also create and start the images separately
## Backend
### Build the image
    cd server
    docker build -t todolist-backend .

### Start the image
    docker run -p 3000:8080 --name todolist-backend todolist-backend

## Frontend
### Build the image
    cd ToDoList
    docker build -t todolist .

### Start the image
    docker run -p 8080:8080 --name todolist todolist

Point your browser to http://localhost:8080


# Publish images to Docker Hub
Register Account for hub.docker.com and then:

    docker login
    docker tag todolist <dockerHubName>/todolist
    docker push todolist <dockerHubName>/todolist

    docker tag todolist-backend <dockerHubName>/todolist-backend
    docker push todolist-backend <dockerHubName>/todolist-backend

