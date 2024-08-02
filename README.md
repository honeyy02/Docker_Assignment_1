# Docker_Assignment_1

### Build the Docker image from the docker command:

1. **Build the Docker Image**
    - **docker build -t assignment-1 .**  : This command builds a Docker image from your Dockerfile and tags it as `assignment-1`. The `.` specifies that the Dockerfile is in the current directory.
    
2. **Create a Docker Volume**
3. **docker volume create my-volume** : This creates a Docker volume named `my-volume`. Volumes are used to persist data and share it between containers.
    
4. **Run the Docker Container with Volume**
       **docker run --name my-maven-app -d -p 8080:8080 -v my-volume:/app/target assignment-1**

- **`-name my-maven-app`**: Names the container `my-maven-app`.
- **`d`**: Runs the container in detached mode (in the background).
- **`p 8080:8080`**: Maps port 8080 on your host to port 8080 on the container.
- **`v my-volume:/app/target`**: Mounts the `my-volume` volume to the `/app/target` directory in the container. This means any files created in `/app/target` (e.g., the JAR file) are stored in `my-volume`.
- **`assignment-1`**: Specifies the image to use for the container.
