FROM alpine

WORKDIR /app
RUN apk add --no-cache openjdk21-jre 
COPY  *.jar . 
#CMD [ "java -jar sprbootprobe-0.0.1-SNAPSHOT.jar" ]
#CMD ["java -jar sprbootprobe-0.0.1-SNAPSHOT.jar"]
#CMD ["/bin/bash","-c","java -jar sprbootprobe-0.0.1-SNAPSHOT.jar"]
CMD ["sh","-c","java -jar sprbootprobe-0.0.1-SNAPSHOT.jar"]
EXPOSE 8080
