FROM maven:3.8.6-openjdk-11
RUN chmod +x /usr/local/bin/mvn-entrypoint.sh
WORKDIR /app
COPY pom.xml ./
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
CMD [ "mvn","clean","package" ]
