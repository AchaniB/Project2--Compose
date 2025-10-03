# Use your custom Node 16 Alpine image as the base
FROM achani99/node-docker:16-alpine

USER root

# Install dependencies for Jenkins & Docker CLI
RUN apk add --no-cache openjdk17 curl bash git \
    && curl -fsSL https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz | tar -xz -C /usr/local/bin --strip-components=1 docker/docker \
    && npm install -g snyk

# Add Jenkins
RUN curl -fsSL https://get.jenkins.io/war-stable/2.462.2/jenkins.war -o /usr/share/jenkins.war

# Create Jenkins user
RUN adduser -D jenkins && mkdir -p /var/jenkins_home && chown -R jenkins:jenkins /var/jenkins_home

ENV JENKINS_HOME=/var/jenkins_home

# Expose ports
EXPOSE 8080 50000

USER jenkins

ENTRYPOINT ["java", "-jar", "/usr/share/jenkins.war"]

