# Multi-Language Development Environments

This repository provides ready-to-use, containerized development environments for a variety of programming languages. Whether you are starting a new project or experimenting with different languages, this repository aims to simplify the setup process so you can get started quickly without the hassle of manually configuring each environment.

## Purpose
The main goal of this repository is to offer a consistent and simple way to set up and use development environments for multiple programming languages using Docker. Each environment is isolated, allowing developers to work in a clean and predictable setting, independent of the host system's configuration.

## Available Languages
- [x] C++
- [x] Python

## C++ Development Environment
The C++ environment is designed to make it easy to compile, debug, and run C++ applications without worrying about system dependencies or compiler setups. Below, you will find the steps to use the Docker-based C++ development setup.

### Getting Started with C++

1. **Clone the Repository** 
   ```sh
   git clone https://github.com/yourusername/Docker_Env_Programming_Languages.git
   cd Docker_Env_Programming_Languages/cpp
   ```

2. **Build and Run the Docker Container**  
   The Docker environment for C++ uses `g++` and includes tools like `cmake` and `gdb` for compiling and debugging C++ applications.
   ```sh
   docker-compose up --build
   ```

3. **Modify Your Code**  
   Add or modify your C++ files in the `cpp/` directory. The Docker container mounts this folder, so any changes made locally are automatically available inside the container.

4. **Run Your Code**  
   To compile cpp programs you have to run a command similar to this one
   
   ```bash
   g++ -o app app.cpp
   ```
    The **`-o`** flag in the g++ command stands for **`output file`**. It allows you to specify the name of the output executable file after compilation. To run it:
   ```sh
   ./app
   ```
5. **Running on VSCode** 
    In order to run your code on the IDE, install C/C++ Runner extension

### File Structure
- **cpp/**: Contains the C++ environment configuration.
  - `Dockerfile`: Docker image setup for C++ development.
  - `docker-compose.yml`: Defines the services and container behavior.

## Python Development Environment
The Python environment is designed to facilitate development for general-purpose scripts, data science, and web applications, using popular tools and libraries. Below are the steps to get started with the Python Docker environment.

### Getting Started with Python

1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/Docker_Env_Programming_Languages.git
   cd Docker_Env_Programming_Languages/python
   ```

2. **Build and Run the Docker Container**  
   The Docker environment for Python uses `python:latest` and includes commonly used libraries like `pip`, `virtualenv`, and other tools for various purposes.
   ```sh
   docker-compose up --build
   ```

3. **Modify Your Code**  
   Add or modify your Python scripts in the `python/` directory. The Docker container mounts this folder, making it easy to develop and test code continuously.

4. **Run Your Code**  
   By default, you can enter the container and run any Python script interactively:
   ```sh
   docker-compose run python_app python your_script.py
   ```

### File Structure
- **python/**: Contains the Python environment configuration.
  - `Dockerfile`: Docker image setup for Python development.
  - `docker-compose.yml`: Defines the services and container behavior.