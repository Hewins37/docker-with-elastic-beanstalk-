# Cloud Project Demo

A professional demonstration of deploying a static website using **Docker** and the official **Nginx** image.  
This repo is structured so anyone can reproduce the project step by step.

## Prerequisites
- Install Docker: [https://www.docker.com/get-started/](https://www.docker.com/get-started/)  
- Optional: Docker Compose for easier container management

## Step 1: Create Project Folder
Open your terminal and run:

cd ~/Desktop
mkdir Compute
cd Compute
touch Dockerfile index.html

## Step 2: Dockerfile

Open Dockerfile in a text editor and add the following:

FROM nginx:latest
COPY index.html /usr/share/nginx/html/
EXPOSE 80


This will use the official Nginx image and copy your index.html into the container.

## 🔹 Step 3: Create index.html

Open index.html in your text editor and add:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cloud Project Demo</title>
  <style>
    body { margin:0; font-family:"Segoe UI", Roboto, Helvetica, Arial, sans-serif; background:#f4f6f8; color:#333; line-height:1.6; }
    header { background:#0d6efd; color:#fff; padding:2rem; text-align:center; }
    header h1 { margin:0; font-size:2.5rem; }
    main { padding:2rem; max-width:900px; margin:auto; }
    .card { background:#fff; padding:1.5rem; margin:1rem 0; border-radius:10px; box-shadow:0 4px 10px rgba(0,0,0,0.05); }
    .card h2 { margin-top:0; color:#0d6efd; }
    footer { text-align:center; padding:1rem; background:#222; color:#bbb; margin-top:2rem; }
    a.button { display:inline-block; background:#0d6efd; color:white; padding:0.7rem 1.2rem; border-radius:6px; text-decoration:none; font-weight:bold; transition:background 0.3s; }
    a.button:hover { background:#084298; }
  </style>
</head>
<body>
  <header>
    <h1>🚀 Cloud Project Demo</h1>
    <p>Running Nginx in Docker to serve a professional static website</p>
  </header>

  <main>
    <div class="card">
      <h2>About this project</h2>
      <p>This is a demonstration of deploying a static website using <strong>Docker</strong> and the official <strong>Nginx</strong> image. Reproducible by anyone.</p>
    </div>

    <div class="card">
      <h2>Key Technologies</h2>
      <ul>
        <li>⚡ Docker & Docker Compose</li>
        <li>📦 Nginx (official image)</li>
        <li>☁️ Cloud deployment-ready structure</li>
      </ul>
    </div>

    <div class="card">
      <h2>Get Started</h2>
      <p>Clone the repo and run:</p>
      <pre><code>docker-compose up -d</code></pre>
      <p>Or directly with Docker:</p>
      <pre><code>docker build -t my-web-app .
docker run -d -p 80:80 my-web-app</code></pre>
      <p>Open: <a href="http://localhost" class="button">View Website</a></p>
    </div>
  </main>

  <footer>
    <p>Created by <strong>Your Name</strong> · <a href="https://github.com/YourUsername" style="color:#0d6efd;">GitHub</a></p>
  </footer>
</body>
</html>

## Step 4: Build & Run Docker Container
# Build Docker image
docker build -t my-web-app .

# Run container

docker run -d -p 80:80 my-web-app


Open your browser: http://localhost




## deletes yours recourses 

delete the bean stalk environement
stop the containers

GOOD!!!









