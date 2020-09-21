FROM openjdk:14-jdk-alpine
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar
ENV CONFIG_SERVER ''
ENV CONSUL_HOST ''
EXPOSE 8888
ENTRYPOINT ["java","-jar", "-Dspring.profiles.active=prod", "-Dservice_springcloud_configserver=${CONFIG_SERVER}","-Dservice_springcloud_consul_host=${CONSUL_HOST}","/app.jar"]

#docker build -t eshop-config-server .

#docker run -p 8888:8888  -e CONFIG_SERVER=https://github.com/liuziyuan/eshop-springcloud-containers -e CONSUL_HOST=host.docker.internal eshop-config-server