# Project Setup and Docker Instructions

## Node.js Setup

### Install Node.js
- **Node.js**: A JavaScript runtime built on Chrome's V8 JavaScript engine.
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
   - **npm**: Node Package Manager, used to install project dependencies.
3. Run the application:
    ```sh
    node index.js
    ```
   - **node**: Command to run Node.js scripts.

## Docker Commands

### Build and Run a Docker Container
- **Docker**: A platform for developing, shipping, and running applications in containers.
- Build a Docker container with the name `test_app`:
    ```sh
    docker build . -t test_app
    ```
   - **docker build**: Creates a Docker image from a Dockerfile.
   - **-t**: Tags the image with a name.

- Run the container `test_app` on port 3000:
    ```sh
    docker run -p 3000:3000 test_app
    ```
   - **docker run**: Runs a command in a new container.
   - **-p**: Maps a port on the host to a port in the container.

### List Docker Images
- List all the Docker images:
    ```sh
    docker images
    ```
   - **docker images**: Lists all images on the Docker host.

### Pull Docker Image
- Pull a Docker image from Docker Hub:
    ```sh
    docker pull <image_name>
    ```
   - **docker pull**: Downloads an image from a Docker registry.

### Create and Use Docker Volume
- **Docker Volume**: A persistent data storage mechanism.
- Create a Docker volume:
    ```sh
    docker volume create volume_database
    ```
   - **docker volume create**: Creates a new volume.

- Run a Docker container with a volume:
    ```sh
    docker run -v volume_database:/data/db -p 27027:27017 mongo
    ```
   - **-v**: Mounts a volume to the container.

### Create and Use Docker Network
- **Docker Network**: A virtual network for connecting Docker containers.
- Create a Docker network:
    ```sh
    docker network create ntw_name
    ```
   - **docker network create**: Creates a new network.

- Run a Docker container on a network:
    ```sh
    docker run -p 3000:3000 --name backend --network ntw_name <image_tag>
    ```
   - **--network**: Connects a container to a network.

### Run Docker Container with Environment Variables
- **Environment Variable**: A variable that is set outside of the program and can affect the way it runs.
- Run a Docker container with an environment variable:
    ```sh
    docker run -p 3000:3000 -e MONGO_URI=something <image_tag>
    ```
   - **-e**: Sets an environment variable.

### Build and Run Docker Image for Production
- **Production Build**: An optimized build for deployment.
- Build a production Docker image:
    ```sh
    docker build . --target production -t app:prod
    ```
   - **--target**: Specifies the build stage.

- Run the production Docker image:
    ```sh
    docker run app:prod
    ```

### Mount Local Directory to Docker Container
- **Volume Mount**: Links a local directory to a directory in the container.
- Run a Docker container with a volume mounted to the local directory:
    ```sh
    docker run -v .:/usr/src/app app:dev
    ```

### Run Multiple Services with Docker Compose
- **Docker Compose**: A tool for defining and running multi-container Docker applications.
- Use Docker Compose to run all services:
    ```sh
    docker-compose up
    ```

### Pull and Run Docker Images on AWS EC2
- **AWS EC2**: Amazon Web Services Elastic Compute Cloud, a web service that provides resizable compute capacity in the cloud.
- Refer to this [gist](https://gist.github.com/ogre-yoga/04c6cc817e9f95ee788b3893db93fa3a) for instructions on how to pull and run Docker images on an AWS EC2 machine.

---

Feel free to reach out if you have any questions or need further assistance!
