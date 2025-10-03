FROM jenkins/jenkins:lts-jdk17

USER root

# Install Docker CLI, Git, curl
RUN apt-get update && \
    apt-get install -y docker.io git curl && \
    apt-get clean

USER jenkins
