# specify a parent image
FROM node:17-alpine


#to install nodemon globally to keep track of changes to the code
RUN npm install -g nodemon


# specify the working directory
WORKDIR /app


#copy the file for faster runtime (layer caching)
COPY package.json .


# to add all the dependencies
RUN npm install



# copy all the source files
COPY . .



# required for docker desktop port mapping
EXPOSE 4000


#specify command to be run only when the container based on this image is run
CMD ["npm", "run", "dev"]