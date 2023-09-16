FROM debian:stable-slim

ENV TZ="Europe/Ljubljana"

# Add packages
RUN apt-get clean
RUN apt-get update
RUN apt-get -y install tzdata
RUN echo "Europe/Ljubljana" | tee /etc/timezone

# Install nodejs
COPY setup_18.sh /
RUN chmod +x setup_18.sh
RUN ./setup_18.sh
RUN apt-get update
RUN apt-get install -y -f nodejs

