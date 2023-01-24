FROM node:19-alpine

#Setting the app directory client
WORKDIR /client

#Copy both package.json AND package-lock.json
COPY package*.json ./

#Install app dependencies
RUN npm install

#Copy the client app source 
COPY . /client/

#Starting the app
CMD ["npm", "start"]