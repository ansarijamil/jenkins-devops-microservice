FROM node:8.16.1-alpine
WORKDIR /app
#COPY package.json /app
COPY . /app
RUN npm install
EXPOSE 5000
COPY . /app
CMD node index.js

#ENTRYPOINT ["node", "index.js"]
#COPY package.json /app



#  summary of above code 
#   build base image from node:8.16
#   make /app as working directory
#   copy all files from current directory to /app
#   build the application
#   expose the port 5000 
#   run the application
#   this way of creating image is not efficient, because most of the time there will change in code
#   and not in the depedencies. so here when we change any line in code and re create image then it 
#   will re run all the steps after the code change step. i.e step 4, 5, 6. and this is time consuming


#   Lets make the image creation efficient by layer chaching
#   we are adding  COPY package.json /app  in 3rd step, so that the dependency file will be added 
#   before we build the code
#   and moving   COPY . /app to step 7, so that when we start building application, code change
#   will be picked up efficiently.

