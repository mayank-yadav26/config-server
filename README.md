# Config Server

This is a Spring Cloud Config Server application. It serves configuration files from a remote Git repository to client applications.

## Features
- Centralized configuration management
- Supports multiple profiles and labels
- Git-based configuration repository

## Prerequisites
- Java 17+
- Maven

## Setup
1. Update `src/main/resources/application.properties` to set the config server port and Git repo URL.
2. Build the project:
   ```bash
   mvn clean package
   ```
3. Run the server:
   ```bash
   java -jar target/config-server-1.0.0.jar
   ```

## Usage
- The server exposes endpoints like:
  - `http://localhost:8889/{application}/{profile}`
- Ensure your Git repo contains config files for each client (e.g., `config-client.yml`).

## Troubleshooting
- If clients receive 404 errors, check the repo for missing config files and verify the server is running.

## License
MIT
