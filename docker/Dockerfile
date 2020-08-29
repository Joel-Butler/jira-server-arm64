FROM ubuntu:20.04
CMD sudo apt-get update
CMD sudo apt-get install libmariadb-java openjdk-8-jre-headless mariadb-client wget
CMD adduser jira
CMD mkir -p /opt/atlassian/jira
CMD adduser jira -q --disabled-password --gecos ""
WORKDIR /opt/atlassian/jira
# copy Jira into platform

CMD mkdir -p /var/atlassian/application-data/jira
#set permissions
CMD chown -R jira:jira /var/atlassian
CMD chown -R jira:jira /opt/atlassian/jira
ENV JIRA_HOME=/var/atlassian/application-data/jira
ENV JIRA_INSTALL_DIR=/opt/atlassian/jira
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-arm64/jre
