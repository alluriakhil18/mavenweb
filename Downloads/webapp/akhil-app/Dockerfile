# Use Tomcat as the base image
FROM tomcat:9.0

# Remove default apps
RUN rm -rf /usr/local/tomcat/webapps/*

# Copy your WAR file and name it akhil-app.war to preserve the context path
COPY target/akhil-app.war /usr/local/tomcat/webapps/akhil-app.war

# Expose port 9091
EXPOSE 9091

# Change Tomcat port from 8080 to 9091
RUN sed -i 's/8080/9091/g' /usr/local/tomcat/conf/server.xml

# Start Tomcat
CMD ["catalina.sh", "run"]
