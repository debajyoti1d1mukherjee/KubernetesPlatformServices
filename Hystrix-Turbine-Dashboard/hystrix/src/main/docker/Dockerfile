FROM java:8-alpine
VOLUME /hystrix.jar
ADD hystrix.jar app.jar
RUN sh -c 'touch app.jar'
EXPOSE 8090
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-Dspring.profiles.active=docker","-jar","/app.jar"]
