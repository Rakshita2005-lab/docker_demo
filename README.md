# docker_demo

# Dockerized Portfolio Website Deployment

## Project Overview
This project demonstrates how to deploy a simple static portfolio website using Docker and Nginx. The website is packaged into a Docker image and runs inside a container, making deployment simple, portable, and consistent across different environments.

## Technologies Used
- **HTML5** – Website structure
- **CSS3** – Styling and responsive design
- **JavaScript** – Interactive functionality
- **Docker** – Application containerization
- **Nginx** – Web server for hosting static files

## Project Structure

```text
docker-portfolio/
│
├── index.html
├── style.css
├── Dockerfile
└── README.md
```

## Prerequisites

Before running this project, install:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Git](https://git-scm.com/)
- A web browser

## Dockerfile

```dockerfile
FROM nginx:alpine

COPY . /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the project directory

```bash
cd docker-portfolio
```

### 3. Build the Docker image

```bash
docker build -t my-portfolio .
```

### 4. Run the Docker container

```bash
docker run -d -p 8080:80 --name portfolio my-portfolio
```

### 5. Access the website

Open your browser and visit:

```text
http://localhost:8080
```

Your portfolio website will now run inside a Docker container.

## Useful Docker Commands

| Command | Description |
|---|---|
| `docker images` | List Docker images |
| `docker ps` | View running containers |
| `docker ps -a` | View all containers |
| `docker stop portfolio` | Stop the container |
| `docker start portfolio` | Start the container |
| `docker logs portfolio` | View container logs |
| `docker rm -f portfolio` | Remove the container |
| `docker rmi my-portfolio` | Remove the image |

## Key Learning Outcomes

- Understanding Docker and containerization.
- Creating a Dockerfile.
- Building and managing Docker images.
- Running applications inside Docker containers.
- Understanding port mapping.
- Hosting static websites using Nginx.
- Deploying applications in an isolated environment.

## Future Enhancements

- Add GitHub Actions for automated Docker image builds.
- Push Docker images to Docker Hub.
- Deploy the container to a cloud platform.
- Add a custom domain and HTTPS support.

## Author

**Rakshita Pramod Handage**

Computer Science and Engineering Student

- GitHub: https://github.com/Rakshita2005-lab

## License

This project is open-source and available for learning and educational purposes.
