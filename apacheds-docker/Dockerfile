FROM openjdk:8-jdk-alpine
RUN apk add --no-cache bash
RUN mkdir /opt/apacheds
ADD https://archive.apache.org/dist/directory/apacheds/dist/2.0.0.AM25/apacheds-2.0.0.AM25.tar.gz /opt/apacheds/
RUN tar -xzf /opt/apacheds/apacheds-2.0.0.AM25.tar.gz -C /opt/apacheds
RUN rm /opt/apacheds/apacheds-2.0.0.AM25.tar.gz
RUN mv /opt/apacheds/apacheds-2.0.0.AM25 /opt/apacheds/default
EXPOSE 10389 10636
CMD ["/opt/apacheds/default/bin/apacheds.sh", "run"]