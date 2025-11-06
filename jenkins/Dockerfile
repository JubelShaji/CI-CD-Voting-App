FROM jenkins/jenkins:lts

USER root
# Install curl and Kaniko
RUN apt-get update && apt-get install -y curl ca-certificates && \
    curl -L https://github.com/GoogleContainerTools/kaniko/releases/download/v1.23.2/executor_linux_amd64 \
      -o /usr/local/bin/kaniko && \
    chmod +x /usr/local/bin/kaniko && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

USER jenkins

