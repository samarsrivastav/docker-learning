# Project Setup and Docker Instructions

## Node.js Setup

### Install Node.js
- Download and install Node.js from [nodejs.org](https://nodejs.org/).

### Set Up Project
1. Navigate to your project folder:
    ```sh
    cd path/to/your/project/folder
    ```
2. Install project dependencies:
    ```sh
    npm install
    ```
3. Run the application:
    ```sh
    node index.js
    ```

## Docker Commands

### Build and Run a Docker Container
- Build a Docker container with the name `test_app`:
    ```sh
    docker build . -t test_app
    ```
- Run the container `test_app` on port 3000:
    ```sh
    docker run -p 3000:3000 test_app
    ```

### List Docker Images
- List all the Docker images:
    ```sh
    docker images
    ```

### Pull Docker Image
- Pull a Docker image from Docker Hub:
    ```sh
    docker pull <image_name>
    ```

### Create and Use Docker Volume
- Create a Docker volume:
    ```sh
    docker volume create volume_database
    ```
- Run a Docker container with a volume:
    ```sh
    docker run -v volume_database:/data/db -p 27027:27017 mongo
    ```

### Create and Use Docker Network
- Create a Docker network:
    ```sh
    docker network create ntw_name
    ```
- Run a Docker container on a network:
    ```sh
    docker run -p 3000:3000 --name backend --network ntw_name <image_tag>
    ```

### Run Docker Container with Environment Variables
- Run a Docker container with an environment variable:
    ```sh
    docker run -p 3000:3000 -e MONGO_URI=something <image_tag>
    ```

### Build and Run Docker Image for Production
- Build a production Docker image:
    ```sh
    docker build . --target production -t app:prod
    ```
- Run the production Docker image:
    ```sh
    docker run app:prod
    ```

### Mount Local Directory to Docker Container
- Run a Docker container with a volume mounted to the local directory:
    ```sh
    docker run -v .:/usr/src/app app:dev
    ```

### Run Multiple Services with Docker Compose
- Use Docker Compose to run all services:
    ```sh
    docker-compose up
    ```

### Pull and Run Docker Images on AWS EC2
- Refer to this [gist](https://gist.github.com/ogre-yoga/04c6cc817e9f95ee788b3893db93fa3a) for instructions on how to pull and run Docker images on an AWS EC2 machine.

---

Feel free to reach out if you have any questions or need further assistance!
