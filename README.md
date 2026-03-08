# Docker Practice: Nginx and Redis with Docker Compose

This is a simple project to learn how to use **Docker Compose** to run multiple containers together. I built this infrastructure on **Zorin OS** using my **Asus TUF A15** laptop. It includes a web server, a database, and a management tool.

---

##  Project Structure

This project runs three different services:

* **Web Server (Nginx):** It serves my `index.html` file. I used a **volume** so I can update the website without restarting the container.
<img width="1764" height="1080" alt="8080" src="https://github.com/user-attachments/assets/9a33db44-6d02-4de9-890f-98fd09b67a57" />

* **Database (Redis):** A fast, key-value database to store information.

* **Redis Commander:** A web interface that helps me see and manage the data inside Redis easily.
<img width="1764" height="1080" alt="8081" src="https://github.com/user-attachments/assets/ad280492-cc9a-4cb9-bade-15462c25e049" />

---

##  Key Features

* **Data Persistence:** I connected the container to a folder on my computer called `redis-data`. This means my data is safe even if I stop or delete the containers.
* **Resource Limits:** I limited the **CPU** and **RAM** usage for each container. This keeps the system stable and prevents the containers from using too much of my laptop's power.
* **Docker Networking:** All services can talk to each other automatically using their service names.

---

##  How to Run

1.  Clone this repository to your computer.
2.  Open your terminal in the project folder.
3.  Start the project with this command:
    ```bash
    docker compose up -d
    ```
4.  Open your browser and visit:
    * **Website:** `http://localhost:8080`
    * **Redis Tool:** `http://localhost:8081`

---
