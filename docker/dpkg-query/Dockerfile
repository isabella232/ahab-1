# maybe go back to "latest" after "jammy" is stable
#FROM ubuntu:latest
FROM ubuntu:focal

WORKDIR /ahab-docker

RUN apt-get update && apt-get -y install python3-pip

COPY ahab .

# Spit out these just for easier debugging
RUN dpkg-query --show --showformat='${Package} ${Version}\n'

# Deprecated
RUN dpkg-query --show --showformat='${Package} ${Version}\n' | ./ahab chase --os debian
# New way
RUN dpkg-query --show --showformat='${Package} ${Version}\n' | ./ahab chase --package-manager dpkg
