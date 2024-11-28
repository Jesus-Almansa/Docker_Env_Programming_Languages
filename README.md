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
   By default, the container runs the `app` executable generated from the `main.cpp` file. To run it:
   ```sh
   docker-compose run cpp_app ./app
   ```

### File Structure
- **cpp/**: Contains the C++ environment configuration.
  - `Dockerfile`: Docker image setup for C++ development.
  - `docker-compose.yml`: Defines the services and container behavior.
  - `main.cpp`: Sample C++ file to get started.

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
  - `app.py`: Sample Python script to get started.

## Contributing
We welcome contributions from the community to expand the number of languages supported! If you have experience with Docker and want to add a new development environment, follow these steps:

1. **Fork the repository**.
2. **Create a new folder** for the language (e.g., `python/`, `java/`).
3. **Add a Dockerfile** and necessary setup files for that language.
4. **Create a Pull Request** with a descriptive message of the new environment.

### Contribution Guidelines
- Please follow the folder naming convention (`language/`) to maintain consistency.
- Ensure the Dockerfile installs all essential tools and compilers for the respective language.
- Write clear instructions in a `README.md` file within the language folder so new users can easily follow along.

## Future Plans
We are planning to add containerized development environments for:
- **Java**: Configured with Maven and JDK for enterprise-level development.
- **JavaScript/Node.js**: Ready for full-stack development with Node.js and npm.
- **Rust**: For systems programming enthusiasts.

If you have ideas or suggestions for other languages or improvements, please create an issue in the repository.

## License
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

## Contact
Feel free to reach out if you have questions or feedback:
- **GitHub Issues**: Use the issue tracker for bugs and feature requests.
- **Email**: your-email@example.com

Happy coding!

---

We hope this repository becomes a valuable resource for developers looking for easily configurable and portable development environments. Together, we can build a versatile toolkit for everyone!
```

Feel free to copy and adjust the content as needed! Let me know if there's anything else you'd like to add or modify.