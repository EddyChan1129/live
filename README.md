# 📝 ToDoList App (Spring Boot + PostgreSQL + Docker)

This is a simple backend **ToDoList API** built with:

- ✅ Spring Boot (Java 17)
- 🐘 PostgreSQL (via Docker)
- 🐳 Docker + Docker Compose

It supports full **CRUD operations** (Create, Read, Update, Delete) via REST API.

---

## 🚀 Quick Start (No Need to Install Java or Docker Locally)

**Recommended method:** Use [Docker Playground](https://labs.play-with-docker.com/)  
You don’t need to install Java, Spring Boot, or Docker on your computer.

### Steps:

```bash
git clone https://github.com/EddyChan1129/live.git
cd live
docker-compose up --build -d
````

This will start:

* The Spring Boot app on `localhost:8080`
* The PostgreSQL database on `localhost:5432`

---

## 🧪 Test the API using `curl`

### ✅ 1. Get all todos

```bash
curl http://localhost:8080/api/todos
```

---

### ➕ 2. Create a new todo

```bash
curl -X POST http://localhost:8080/api/todos \
  -H "Content-Type: application/json" \
  -d '{"title": "Buy milk", "completed": false}'
```

---

### ✏️ 3. Update a todo

```bash
curl -X PUT http://localhost:8080/api/todos/1 \
  -H "Content-Type: application/json" \
  -d '{"title": "Buy chocolate", "completed": true}'
```

---

### ❌ 4. Delete a todo

```bash
curl -X DELETE http://localhost:8080/api/todos/1
```

---

## 📁 Project Structure

| File/Folder          | Purpose                                                  |
| -------------------- | -------------------------------------------------------- |
| `Dockerfile`         | Defines how to build the Spring Boot app                 |
| `docker-compose.yml` | Runs both the app and PostgreSQL                         |
| `src/`               | Java source code for the app (models, controllers, etc.) |

---

## ⚙️ Tech Stack

* Java 17 with Spring Boot
* PostgreSQL 12
* Maven for build
* Docker for environment management

---