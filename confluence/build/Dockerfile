FROM cptactionhank/atlassian-confluence:7.8.1
COPY ./atlassian-agent.jar /opt/atlassian-agent/atlassian-agent.jar
ENV JAVA_OPTS="-javaagent:/opt/atlassian-agent/atlassian-agent.jar"
