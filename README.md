
 - Install Node.js
 - cd into folder
 - npm install
 - node index.js

## Some Docker commands:
 - docker build . -t test_app
    -- it will create a container with the name test_app

 - docker run -p 3000:3000 test_app
    -- it will run the container test_app on port 3000

 - docker images
    -- it lists all the images 

 - docker pull
    -- it pulls the docker image from docker hub
   
 - docker volume create volume_database
 - docker run -v volume_database:/data/db -p 27027:27017 mongo
    -- it runs the docker image along with creating a volume
    

## pull and run docker images on aws ec2 machine
https://gist.github.com/ogre-yoga/04c6cc817e9f95ee788b3893db93fa3a
