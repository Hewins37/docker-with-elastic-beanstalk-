# Cloud Project Demo — Step by Step

A simple demo to run a static website with **Docker** and **Nginx**.

---

## Prerequisites
- Docker installed: [https://www.docker.com/get-started/](https://www.docker.com/get-started/)
- Optional: Docker Compose for easier management

---

## Step 1: Create Project Folder
```bash
cd ~/Desktop
mkdir Compute
cd Compute
touch Dockerfile index.html

#Step 2: Dockerfile

Open Dockerfile in a text editor and add:
FROM nginx:latest
COPY index.html /usr/share/nginx/html/
EXPOSE 80


Step 3: index.html

Open index.html and add a simple professional landing page, for example:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Cloud Project Demo</title>
</head>
<body>
  <h1>🚀 Cloud Project Demo</h1>
  <p>Static site served by Nginx in Docker</p>
</body>
</html>


(You can replace it later with a more complete HTML page.)

Step 4: Build and Run Docker Image
# Build Docker image
docker build -t my-web-app .

# Run container
docker run -d -p 80:80 my-web-app


Check in your browser: http://localhost

Step 5: Optional Docker Compose

Create docker-compose.yml:

version: '3.8'
services:
  nginx:
    image: nginx:latest
    ports:
      - "8080:80"
    volumes:
      - ./index.html:/usr/share/nginx/html/index.html:ro
    restart: unless-stopped


Run:

docker-compose up -d


Stop:

docker-compose down

Step 6: Cleanup
docker stop <container_id>
docker rm <container_id>



