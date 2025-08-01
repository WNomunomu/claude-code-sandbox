FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install Java 17
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends openjdk-17-jdk

# Install Gradle
RUN wget -q https://services.gradle.org/distributions/gradle-8.4-bin.zip \
    && unzip -q gradle-8.4-bin.zip -d /opt \
    && rm gradle-8.4-bin.zip \
    && ln -s /opt/gradle-8.4/bin/gradle /usr/local/bin/gradle

# Set JAVA_HOME
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64