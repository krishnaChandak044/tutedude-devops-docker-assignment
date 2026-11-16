# Docker Compose full stack

A Node.js/Express frontend and Python/Flask backend run in separate containers on a private Compose network. The browser reaches port 3000; Express proxies `/api/health` to Flask through service name `backend`.

## Run locally
1. Install Docker with the Compose plugin.
2. Copy `.env.example` to `.env`; set your Docker Hub username.
3. Run `docker compose up --build -d`.
4. Open `http://localhost:3000` and select **Check backend**.
5. Inspect with `docker compose ps` and `docker compose logs --tail=50`. Stop with `docker compose down`.

## Publish images
After signing in to Docker Hub, set `DOCKERHUB_USER`, run `docker login`, then `docker compose build` and `docker compose push`. This tags `tutedude-node-frontend:1.0` and `tutedude-flask-backend:1.0`. GitHub repository: https://github.com/krishnaChandak044/tutedude-devops-docker-assignment. Docker Hub images are published under `krishna04chandak/tutedude-node-frontend:1.0` and `krishna04chandak/tutedude-flask-backend:1.0`. No credentials are included. The `evidence/` folder lists genuine runtime screenshots to add before portal submission.
