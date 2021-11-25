FROM ubuntu
WORKDIR /app
RUN apt-get update -y
RUN apt-get install maven -y
COPY . .
EXPOSE 8761
RUN mvn clean install 
RUN java -jar spring-boot-cloud-eureka-server/target/eureka-server.jar
