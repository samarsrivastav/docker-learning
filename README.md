
 - Install Node.js
 - cd into folder
 - npm install
 - node index.js

## Some Docker commands:
 - ### docker build . -t test_app
    -- it will create a container with the name test_app

 - ### docker run -p 3000:3000 test_app
    -- it will run the container test_app on port 3000

 - ###  docker images
    -- it lists all the images 

 - ### docker pull
    -- it pulls the docker image from docker hub
   
 - ### docker volume create volume_database
 - ### docker run -v volume_database:/data/db -p 27027:27017 mongo
    -- it runs the docker image along with creating a volume

 - ### docker network create ntw_name
 - ### docker run -p 3000:3000 -- name backend -- network ntw_name <image_tag>


- ### docker run -p 3000:3000 -e MONGO_URI=something <image_tag>
  - this runs the image along with a env variable of name MONGO_URI and value something (this is fetched by calling " process.env.MONGO_URI,{} "

 - ### docker build . --target production -t app:prod
    - check the docker file of part-2/4th folder --> this will make the image of starting 4 line and the production part ignoring the middle
    - use docker run app:prod
    - 
 - ### using [ docker run -v .:/usr/src/app app:dev ]
    - this will make sure the editing of file (while running) will restart the docker container
    - this means that docker container file is mounted to the local machine and any change in the container will change the original file
 
## pull and run docker images on aws ec2 machine
https://gist.github.com/ogre-yoga/04c6cc817e9f95ee788b3893db93fa3a
