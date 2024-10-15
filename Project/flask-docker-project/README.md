# Flask Docker Project

This project showcases how I built and ran a simple "Hello, World!" web application using Flask and Python. I then containerized the application using Docker to make deployment easier. This project demonstrates my skills in web development and containerization.

## Overview

The project is divided into two main phases:

1. **Building the Flask Application**
2. **Containerizing the Application with Docker**

### Technologies I Used

- **Python 3**
- **Flask**
- **Docker**
- **Visual Studio Code**

## Part 1: Building the Flask Application

### Steps I took

1. **Installed Python**
    
   I first checked if Python was installed on my system by running:
    
    ```bash
    python3 --version
    
    ```
    
2. **Installed Flask**
    
    After confirming Python was installed, I used pip to install Flask:
    
    ```bash
    pip3 install flask
    
    ```
    
3. **Set Up the Project Directory**
I created a directory for the project and navigated into it:
    
    ```bash
    mkdir hello_flask
    cd hello_flask
    ```
    
4. **Created the Application File**
I created the app.py file to start writing my Flask application:
    
    ```bash
    touch [app.py]
    ```
    
5. **Wrote the Flask Application**
I opened app.py and added the following code:
    
    ```python
    from flask import Flask
    
    app = Flask(**name**)
    
    @app.route('/')
    def hello_world():
    		return '<h1 style="font-size: 100px;">Hello, World!</h1>'
    		
    if **name** == '**main**':
    		app.run(host='0.0.0.0', port=5002)
    
    ```
I adjusted the text to be larger using HTML and inline CSS to make the message stand out.

6. **Ran the Application**
I ran the application locally using:
    
    ```bash
    python3 [app.py](http://app.py/)
    ```
    
7. **Accessed the Application**
With the Flask server running, I opened my browser and navigated to:
[http://localhost:5002]
I saw the "Hello, World!" message displayed in large text as expected.


![Hello, world picture]()

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

