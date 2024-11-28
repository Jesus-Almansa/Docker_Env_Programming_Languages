FROM alpine:latest

# Install necessary packages for building and running C++ programs
RUN apk update && \
    apk add --no-cache g++ cmake make gdb libstdc++ libc6-compat nano

WORKDIR /usr/src/app

CMD ["sh", "-c", "cd /usr/src/app && /bin/sh"]


# # Use an official Ubuntu image as the base
# FROM ubuntu:latest

# # Install necessary packages for building and running C++ programs
# RUN apt-get update && apt-get install -y build-essential gdb

# # Set the working directory inside the container
# WORKDIR /usr/src/app

# # Default shell command so the container starts interactively
# CMD ["sh", "-c", "cd /usr/src/app && /bin/sh"]
