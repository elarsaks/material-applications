## express app

Access with browser http://localhost:8080

## Deployment

Deployed application: https://go-blockchain-wallet-server.onrender.com

Pipeline summary:
- Push to main triggers GitHub Actions
- Workflow builds Docker image from express-app/Dockerfile
- Workflow logs in to Docker Hub and pushes <dockerhub-username>/material-applications:latest
- Workflow triggers cloud deployment using Render deploy hook
- Cloud service pulls latest image and serves the updated version
