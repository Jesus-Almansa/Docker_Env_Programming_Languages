# Use an official Alpine image as the base for a lighter Linux environment
FROM alpine:latest

# Install necessary packages for building C++ programs
RUN apk update && \
    apk add --no-cache build-base cmake gdb

# Set the working directory inside the container
WORKDIR /usr/src/app

# Command to compile the C++ files using g++
# RUN g++ -o app main.cpp

# Default shell command so the container starts interactively, giving you more options
CMD ["sh", "-c", "cd /usr/src/app && /bin/sh"]
