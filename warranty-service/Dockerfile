FROM openjdk:11-jdk

VOLUME /tmp

ENV PORT=8180
EXPOSE 8180

ADD build/libs/warranty-service.jar warranty-service.jar

RUN bash -c 'touch /warranty-service.jar'

ENTRYPOINT ["java","-Dserver.port=${PORT:-8180}","-Djava.security.egd=file:/dev/./urandom","-XX:+UseContainerSupport","-Xmx512m","-Xms128m","-jar","/warranty-service.jar"]