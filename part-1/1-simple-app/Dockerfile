# this is the node that you want to use 
FROM node:20
# this is is directory to tell the os
WORKDIR /usr/src/app
# you are coping this folder to the above dir
COPY . .
# to install node modules
RUN npm install
#port to run
EXPOSE 3000
# to run index.js --( RUN npm index.js  can also be used)
CMD ["node", "index.js"]



