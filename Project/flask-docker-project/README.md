# Flask Docker Project

This project demonstrates how to build and run a simple "Hello, World!" web application using Flask and Python. The application is containerized using Docker for ease of deployment.

## Overview

The project is divided into two main phases:

1. **Building the Flask Application**
2. **Containerizing the Application with Docker**

### Technologies Used

- **Python 3**
- **Flask**
- **Docker**
- **Visual Studio Code**

## Part 1: Building the Flask Application

### Steps

1. **Install Python**
    
    Make sure Python is installed on your system:
    
    ```bash
    python3 --version
    
    ```
    
2. **Install Flask**
    
    Install Flask using `pip`:
    
    ```bash
    pip3 install flask
    
    ```
    
3. **Set Up Project Directory**
Create a directory for the project and navigate into it:
    
    ```bash
    mkdir hello_flask
    cd hello_flask
    ```
    
4. **Create the Application File**
Create the [app.py](http://app.py/) file:
    
    ```bash
    touch [app.py](http://app.py/)
    ```
    
5. **Write the Flask Application**
Open [app.py](http://app.py/) and add the following code:
    
    ```python
    from flask import Flask
    
    app = Flask(**name**)
    
    @app.route('/')
    def hello_world():
    		return '<h1 style="font-size: 100px;">Hello, World!</h1>'
    		
    if **name** == '**main**':
    		app.run(host='0.0.0.0', port=5002)
    
    ```
    
6. **Run the Application**
Run the application locally:
    
    ```bash
    python3 [app.py](http://app.py/)
    ```
    
7. **Access the Application**
Open your browser and go to:
[http://localhost:5002](http://localhost:5002/)

## Part 2: Containerizing the Application
Steps
1. **Create a Dockerfile**
In the hello_flask directory:

```bash
touch Dockerfile
```

2. **Write the Dockerfile**
Add the following contents:

```docker
Dockerfile
FROM python:3.8-slim
WORKDIR /app
COPY . .
RUN pip install flask
EXPOSE 5002
CMD ["python", "[app.py](http://app.py/)"]
```

3. **Build the Docker Image**
Build the image using the following command:

```bash
bash
docker build -t hello-flask .
```

4. **Run the Docker Container**
Run the container with:

```bash
bash
docker run -d -p 5002:5002 hello-flask
```

5. **Check the Container Status**
Verify the container is running:

```bash
bash
docker ps
```

6. **Stop the Container**
Stop the container using its ID:

```bash
bash
docker stop <container_id>
```

## What’s Next?
The next phase involves deploying this Dockerized application on a cloud platform for production. Stay tuned for updates!

## Conclusion
This project highlights my understanding of Flask, Docker, and basic containerization concepts. The simplicity of the application ensures the focus remains on building, running, and deploying the application efficiently.

### Connect with Me
GitHub
LinkedIn

