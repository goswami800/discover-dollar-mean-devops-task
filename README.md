In this DevOps task, you need to build and deploy a full-stack CRUD application using the MEAN stack (MongoDB, Express, Angular 15, and Node.js). The backend will be developed with Node.js and Express to provide REST APIs, connecting to a MongoDB database. The frontend will be an Angular application utilizing HTTPClient for communication.  

The application will manage a collection of tutorials, where each tutorial includes an ID, title, description, and published status. Users will be able to create, retrieve, update, and delete tutorials. Additionally, a search box will allow users to find tutorials by title.

## Project setup

### Node.js Server

cd backend

npm install

You can update the MongoDB credentials by modifying the `db.config.js` file located in `app/config/`.

Run `node server.js`

### Angular Client

cd frontend

npm install

Run `ng serve --port 8081`

You can modify the `src/app/services/tutorial.service.ts` file to adjust how the frontend interacts with the backend.

Navigate to `http://localhost:8081/`

# 🚀 Discover Dollar – MEAN DevOps Assignment

This repository contains my solution for the **DevOps Engineer Intern** technical assignment from **Discover Dollar**.

The task was to:

- Containerize a full-stack **MEAN** (MongoDB, Express, Angular, Node.js) application  
- Deploy it on a cloud **Ubuntu VM (AWS EC2)** using **Docker Compose**  
- Configure **MongoDB** as database (via Docker)  
- Set up **NGINX** as a reverse proxy exposing everything on **port 80**  
- Implement a **CI/CD pipeline** (GitHub Actions) that:
  - Builds Docker images on every push  
  - Pushes them to **Docker Hub**  
  - Automatically deploys latest changes to the EC2 VM  

---

## 🧱 Tech Stack

**Application:**

- **Frontend:** Angular (MEAN app frontend)
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (using Docker image)

**DevOps / Infra:**

- **Docker & Docker Compose**
- **Docker Hub** (image registry)
- **GitHub Actions** (CI/CD)
- **AWS EC2** (Ubuntu 24.04 LTS VM)
- **NGINX** (reverse proxy on port 80)
- **SSH** for remote deployment

---

## 📂 Project Structure

```bash
.
├── backend/                 # Node.js + Express + Mongoose API
│   ├── Dockerfile
│   └── ...
├── frontend/                # Angular frontend
│   ├── Dockerfile
│   └── ...
├── nginx/
│   └── default.conf         # NGINX reverse proxy config
├── docker-compose.yaml      # Multi-container setup (frontend, backend, mongo, nginx)
└── .github/
    └── workflows/
        └── cicd.yml         # GitHub Actions CI/CD pipeline
