Summary of Automation Setup:

1. Dockerfile to set up the environment.
2. app.py containing the Flask application.
3. Git for version control.
4. Docker volume to mount the project directory into the container, allowing changes to be automatically reflected.

Build the Docker Image
docker build -t hello-world-webapp .

Run the Docker Container
docker run -d -p 8080:8080 hello-world-webapp

Automate Updates with Docker
To automatically reflect changes in the running Docker container, use Docker volumes to mount the project directory into the container.

Stop the Running Container:
First, stop the currently running container.

docker stop <container_id>

Run the Container with a Volume:
Run the container with a volume that points to your project directory.
docker run -d -p 8080:8080 -v $(pwd):/app hello-world-webapp


Verification
Access http://localhost:8080 in your web browser. You should see "Hello Universe".
