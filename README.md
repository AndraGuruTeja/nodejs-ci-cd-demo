# Node.js CI/CD Demo

This project demonstrates a simple Node.js application with automated CI/CD using GitHub Actions and Docker Hub.

## Getting Started

### Prerequisites
- Node.js (v20 or later)
- Docker

### Clone the Repository
```bash
git clone https://github.com/AndraGuruTeja/nodejs-ci-cd-demo.git
cd nodejs-ci-cd-demo
```

### Run Locally
Install dependencies and start the server:
```bash
npm install
node server.js
```
The app will run on [http://localhost:3000](http://localhost:3000).


### Run with Docker
You can pull and run the public Docker image directly (no credentials needed):
```bash
docker pull teja5654/nodejs-ci-cd-demo:latest
docker run -d -p 3000:3000 teja5654/nodejs-ci-cd-demo:latest
```

## GitHub Actions CI/CD Flow

Every push to the `main` branch triggers a GitHub Actions workflow that:
1. Checks out the code
2. Sets up Node.js
3. Installs dependencies
4. Builds a Docker image
5. Logs in to Docker Hub
6. Pushes the image to Docker Hub

### Setup Docker Hub Secrets
To enable automatic Docker image pushes, add these secrets to your GitHub repository:
- `DOCKER_USERNAME`: Your Docker Hub username
- `DOCKER_PASSWORD`: Your Docker Hub password or access token

Go to **Settings > Secrets and variables > Actions** in your GitHub repo to add them.

## License
MIT
