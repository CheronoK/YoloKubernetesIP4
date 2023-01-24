FROM node:19-alpine

#Setting the app directory backend
WORKDIR /backend

#Copy both app packages i.e package.json AND package-lock.json
COPY package*.json ./

#Install app dependencies
RUN npm install

#Copy the backend app source 
COPY ./ /backend/

#Starting the app
CMD ["npm", "start"]