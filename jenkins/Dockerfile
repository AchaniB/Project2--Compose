FROM jenkins/jenkins:lts-jdk17

USER root

# Install Docker CLI inside the Jenkins container
RUN apt-get update && apt-get install -y docker.io

USER jenkins
