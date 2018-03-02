#
# Scala and sbt Dockerfile
#
# https://github.com/hseeberger/scala-sbt
#

# Pull base image
FROM openjdk:8u151
MAINTAINER Sawyer LIN <sawyer.lin@gmail.com>

# Env variables
ENV SBT_VERSION 0.13.13

# Scala expects this file
RUN touch /usr/lib/jvm/java-8-openjdk-amd64/release

# Install sbt
RUN \
  curl -L -o sbt-$SBT_VERSION.deb https://dl.bintray.com/sbt/debian/sbt-$SBT_VERSION.deb && \
  dpkg -i sbt-$SBT_VERSION.deb && \
  rm sbt-$SBT_VERSION.deb && \
  apt-get update && \
  apt-get install sbt && \
  sbt sbtVersion

VOLUME ["/app"]

# Define working directory
WORKDIR /app

ENTRYPOINT ["sbt"]
CMD ["--version"]
