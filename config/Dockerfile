FROM chainguard/jre:latest
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>

ADD ./target/config.jar /app/
CMD ["java", "-Xmx200m", "-jar", "/app/config.jar"]

HEALTHCHECK --interval=30s --timeout=30s CMD curl -f http://localhost:8888/actuator/health || exit 1

EXPOSE 8888