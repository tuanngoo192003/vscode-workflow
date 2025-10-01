# Use Eclipse Temurin JDK 21.0.3 on Alpine
FROM eclipse-temurin:21.0.3_9-jdk-alpine

# Install base development tools
RUN apk update && apk add --no-cache \
    maven \
    git \
    curl \
    wget \
    unzip \
    make \
    nano \
    vim \
    net-tools \
    iputils

# Set working directory
RUN mkdir -p /workspace
WORKDIR /workspace