# Build a JAR File
FROM maven:3.6.3-jdk-8-slim AS stage1
WORKDIR /home/app
COPY . /home/app/
RUN mvn -f /home/app/pom.xml clean package

# Create an Image
FROM openjdk:8-jdk-alpine
EXPOSE 5000
COPY --from=stage1 /home/app/target/hello-world-java.jar hello-world-java.jar
ENTRYPOINT ["sh", "-c", "java -jar /hello-world-java.jar"]



# Summary of above lines of code, we are using 2 stages of build
# first stage build jar, second stage build image using jar file
# build base image from maven
# mention working directory
# copy all files from current directory to working directory
# create jar file

# create image
# build base image from maven
# expose port 
# copy jar file from home/app/target folder to hello-world-java.jar
# execute the jar file