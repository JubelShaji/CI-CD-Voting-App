# Start from the official Jenkins LTS image
FROM jenkins/jenkins:lts

# Switch to root to install packages
USER root

# Install dependencies
RUN apt-get update && apt-get install -y \
    curl \
    git \
    sudo \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

# Install kubectl
RUN curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" \
    && chmod +x kubectl \
    && mv kubectl /usr/local/bin/

# Switch back to jenkins user
USER jenkins

# Expose Jenkins ports
EXPOSE 8080 50000
