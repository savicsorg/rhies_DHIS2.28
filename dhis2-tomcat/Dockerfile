FROM tomcat:8.5.46-jdk8-openjdk-slim


LABEL "Author"="Mamaodu Ben TRAORE - ben@savics.org"
LABEL description="DHIS2 webapp with tomcat 7 and jre8 for the RHIES project"


# dhis user setup
RUN useradd -d /opt/dhis2 -m cesarie -s /bin/bash
RUN echo "cesarie:dhis" | chpasswd
RUN mkdir -p /opt/dhis2/config


RUN rm -rf /usr/local/tomcat/webapps/ROOT


#Export to the image all the configurations files
COPY ./config/hibernate.properties /opt/dhis2/config/hibernate.properties
RUN chmod 0600 /opt/dhis2/config/hibernate.properties
COPY ./config/dhis.conf /opt/dhis2/config/dhis.conf
RUN chmod 0600 /opt/dhis2/config/dhis.conf

RUN echo "export JAVA_OPTS=$JAVA_OPTS\nexport DHIS2_HOME='/opt/dhis2/config'\nexport CATALINA_OPTS='-Xms1024M -Xmx2048M'" >> /usr/local/tomcat/bin/setenv.sh

#Export server.xml file into the image
COPY ./config/server.xml /usr/local/tomcat/config/server.xml

#Deploy dhis2.war into tomcat
#Be sure the dhis.war file is into the war/ directory
COPY ./war/dhis.war /usr/local/tomcat/webapps/ROOT.war


EXPOSE 8080


