FROM eclipse-temurin:11-jdk
RUN apt-get update && apt-get install -y wget tar && rm -rf /var/lib/apt/lists/*
WORKDIR /opt/atlassian
RUN wget https://product-downloads.atlassian.com/software/jira/downloads/atlassian-servicedesk-5.15.0.tar.gz \
    -O jsm.tar.gz && \
    tar -xvzf jsm.tar.gz && \
    mv atlassian-jira-servicedesk-* jira && \
    rm jsm.tar.gz
EXPOSE 8080
CMD ["/opt/atlassian/jira/bin/start-jira.sh", "-fg"]
