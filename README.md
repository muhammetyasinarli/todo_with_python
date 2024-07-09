# FastAPI Todo App

## Project Structure

/todo_fast_api
/app
main.py # Your FastAPI application
Dockerfile # Defines how to build your FastAPI container
requirements.txt # Python dependencies
docker-compose.yml # Defines services, networks, and volumes for your containers


A typical FastAPI project structure includes the following components:

- **main.py**: The entry point of the application where you define your app instance and routes.
- **models.py**: Defines the data models that your application will use.
- **schemas.py**: Contains Pydantic models for request and response data validation.
- **database.py**: Manages database connections and sessions.
- **routers/**: A directory containing different routes as separate modules to organize your code better.

To create your file structure, run the following command:

```bash
mkdir -p routers && touch main.py models.py schemas.py database.py
```

Building the Docker Image
Build the Docker image with the following command:
```bash
docker build -t yourusername/fastapi-todo-app .
```

Pushing the Image to a Registry
First, log in to your Docker registry:
```bash
docker login
```
Then, push the image to the registry:
```bash
docker push yourusername/fastapi-todo-app
```
Deploying the API
```bash
To deploy the API, pull the image from the registry and run it:
```
docker pull yourusername/fastapi-todo-app
```bash
docker run -d -p 80:80 yourusername/fastapi-todo-app
```