FROM ubuntu
WORKDIR /app
RUN apt-get update -y
RUN apt-get install maven -y
COPY . .
EXPOSE 8080
RUN mvn clean install 
RUN java -jar spring-boot-cloud-zuul-routing/target/zuul-router.jar --server.port=8080 
