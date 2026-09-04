# 🐳 Docker Capstone Project — Flask App Containerization

A simple **Flask web application containerized using Docker** as part of a Docker Capstone Project.

This project demonstrates how to package a Flask application with all its dependencies into a Docker container, making the application easy to build, run, and deploy consistently across different environments.

---

## 📌 Project Overview

The main objective of this project is to understand and implement the fundamentals of **Docker containerization** with a Python Flask application.

Instead of installing Python, dependencies, and other required components directly on the host machine, the Flask application runs inside an isolated Docker container.

### Key Concepts Covered

* Flask application development
* Dockerfile creation
* Docker image building
* Docker container management
* Port mapping
* Python dependency management
* Containerized application deployment
* Docker image optimization basics

---

## 🏗️ Project Architecture

```text
                    ┌─────────────────────┐
                    │      User / Browser │
                    └──────────┬──────────┘
                               │
                               │ HTTP :5000
                               ▼
                    ┌─────────────────────┐
                    │    Docker Host      │
                    │                     │
                    │  ┌───────────────┐  │
                    │  │ Flask         │  │
                    │  │ Application   │  │
                    │  │               │  │
                    │  │ Python +      │  │
                    │  │ Dependencies  │  │
                    │  └───────────────┘  │
                    │       Container      │
                    └─────────────────────┘
```

---

## 📂 Project Structure

```text
flask-docker-project/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md
```

---

## 🛠️ Technologies Used

| Technology   | Purpose                   |
| ------------ | ------------------------- |
| 🐍 Python    | Application development   |
| 🌶️ Flask    | Web framework             |
| 🐳 Docker    | Containerization          |
| 📦 pip       | Python package management |
| 🌐 HTML/HTTP | Web application interface |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <YOUR-REPOSITORY-URL>
cd docker-flask-capstone
```

---

### 2. Build the Docker Image

Run the following command from the project directory:

```bash
docker build -t flask-docker-app .
```

This command creates a Docker image named:

```text
flask-docker-app
```

---

### 3. Run the Docker Container

```bash
docker run -d -p 5000:5000 --name flask-container flask-docker-app
```

Explanation:

* `-d` → Runs the container in detached mode
* `-p 5000:5000` → Maps host port `5000` to container port `5000`
* `--name flask-container` → Assigns a name to the container
* `flask-docker-app` → Docker image name

---

### 4. Access the Application

Open your browser and visit:

```text
http://localhost:5000
```

If everything is configured correctly, the Flask application should be available in your browser.

---

## 🐳 Useful Docker Commands

### View Running Containers

```bash
docker ps
```

### View All Containers

```bash
docker ps -a
```

### View Docker Images

```bash
docker images
```

### Stop the Container

```bash
docker stop flask-container
```

### Start the Container Again

```bash
docker start flask-container
```

### Remove the Container

```bash
docker rm flask-container
```

### Remove the Docker Image

```bash
docker rmi flask-docker-app
```

### View Container Logs

```bash
docker logs flask-container
```

---

## 🔧 Running the Application Without Docker

If you want to run the Flask application directly on your local machine:

### Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Linux/macOS:

```bash
source venv/bin/activate
```

On Windows:

```bash
venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Flask Application

```bash
python app.py
```

Then open:

```text
http://localhost:5000
```

---

## 📦 Requirements

Example `requirements.txt`:

```text
Flask
```

Additional dependencies can be added according to the application's requirements.

---

## 🔐 Environment Variables

If the application uses environment variables, they should **not be hard-coded** into the source code.

For example:

```bash
docker run -d \
  -p 5000:5000 \
  -e FLASK_ENV=production \
  --name flask-container \
  flask-docker-app
```

For sensitive information such as API keys, passwords, and secrets, use environment variables or a secrets-management solution.

---

## 🧹 .dockerignore

A `.dockerignore` file helps prevent unnecessary files from being copied into the Docker image.

Example:

```text
venv/
__pycache__/
*.pyc
.git/
.gitignore
.env
README.md
```

---

## 🎯 Learning Outcomes

After completing this project, you should understand:

* How Docker containers work
* How to write a basic Dockerfile
* How to create a Docker image
* How to run a Flask application inside a container
* How Docker port mapping works
* How to manage containers and images
* Why containerization is useful for application deployment
* How Docker provides consistency between development and production environments

---

## 🚀 Future Improvements

This project can be extended further by adding:

* Docker Compose
* Nginx as a reverse proxy
* PostgreSQL/MySQL database
* Redis caching
* Health checks
* Multi-stage Docker builds
* Non-root Docker user
* CI/CD pipeline using GitHub Actions
* Cloud deployment using AWS, Azure, or GCP
* Container image scanning and security checks

---

## 🧪 Testing

After starting the container, verify that it is running:

```bash
docker ps
```

Then test the application:

```bash
curl http://localhost:5000
```

You can also open the application directly in a web browser.

---

## 📸 Application Preview

Add screenshots of your Flask application here.

```text
screenshots/
├── home.png
└── docker-container.png
```

Example:

![Flask App Screenshot](screenshots/home.png)

---

## 🏆 Project Highlights

✅ Flask application containerized with Docker
✅ Dockerfile created for reproducible builds
✅ Dependencies managed using `requirements.txt`
✅ Application exposed through Docker port mapping
✅ Container lifecycle managed using Docker CLI
✅ Project structured for easy deployment

---

## 👨‍💻 Author

**Your Name**

* GitHub: `wasique-19`
* LinkedIn: `Wasique Khan`

---

## 📄 License

This project is created for **educational and learning purposes** as part of a Docker Capstone Project.

---

⭐ If you found this project useful, consider giving the repository a star!

