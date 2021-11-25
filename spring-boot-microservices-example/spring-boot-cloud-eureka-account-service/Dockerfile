FROM ubuntu
WORKDIR /app
RUN apt-get update -y
RUN apt-get install maven -y
COPY . .
EXPOSE 8181
EXPOSE 8182
EXPOSE 8183
RUN mvn clean install 
RUN java -jar spring-boot-cloud-eureka-account-service/target/account-service.jar --server.port=8181
RUN java -jar spring-boot-cloud-eureka-account-service/target/account-service.jar --server.port=8182
RUN java -jar spring-boot-cloud-eureka-account-service/target/account-service.jar --server.port=8183
