FROM ubuntu

WORKDIR /app
RUN apt-get update && apt-get install openjdk-21-jre -y
COPY  *.jar . 
#CMD [ "java -jar sprbootprobe-0.0.1-SNAPSHOT.jar" ]
#CMD ["java -jar sprbootprobe-0.0.1-SNAPSHOT.jar"]
#CMD ["/bin/bash","-c","java -jar sprbootprobe-0.0.1-SNAPSHOT.jar"]
CMD ["sh","-c","java -jar sprbootprobe-0.0.1-SNAPSHOT.jar"]
EXPOSE 8080