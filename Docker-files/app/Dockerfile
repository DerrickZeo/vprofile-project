FROM maven:3.9.9-eclipse-temurin-21-jammy AS BUILD_IMAAGE
RUN git clone https://github.com/DerrickZeo/vprofile-project.git
RUN cd vprofile-project && git checkout main && mvn install

FROM tomcat:10-jdk21
LABEL "project"="vprofile"
LABEL "Author"="Derrick"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD [ "catalina.sh", "run" ]
