FROM #{java_11_alpine}#
USER #{alpine_user}#
ADD *.jar app.jar
EXPOSE 22
EXPOSE 22
ENV JAVA_OPTS="-XX:+UseContainerSupport -XX:MaxRAMPercentage=70 -Dcom.sun.management.jmxremote=false"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -Dspring.profiles.active=${profile} -jar app.jar" ]