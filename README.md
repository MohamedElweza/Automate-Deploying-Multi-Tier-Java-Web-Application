# 🚀 Automating Multi-Tier Java Web Application Deployment On-Premises

## 📌 Project Overview
This project automates the deployment of a **multi-tier Java web application** on a local infrastructure using **Vagrant and VirtualBox**. Instead of manual configuration, we use **shell scripts** to set up each component efficiently.

## 🎯 Purpose
The goal of this project is to **automate** the installation and configuration process of each service, making deployments faster, repeatable, and less error-prone.

## 🔧 Tech Stack & Tools Used
| Tool          | Purpose                                         |
|--------------|-----------------------------------------------|
| **Vagrant**  | Automates virtual machine setup              |
| **VirtualBox** | Runs the virtual machines                   |
| **Shell Scripts** | Automates service configurations         |
| **Tomcat**   | Java application server                      |
| **Nginx**    | Reverse proxy and static content server      |
| **RabbitMQ** | Message broker for async communication       |
| **Memcached** | In-memory caching for performance           |
| **MySQL**    | Relational database for data storage        |

## 🏗️ Architecture
The project consists of **five virtual machines**, each running a specific service:
- **Web Server (Nginx)**
- **Application Server (Tomcat)**
- **Database Server (MySQL)**
- **Message Broker (RabbitMQ)**
- **Cache Server (Memcached)**

![Project Architecture](./architecture.gif)![2025-01-3114-44-13online-video-cutter com-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/719b8b15-fad0-4018-8e7c-6edbca9cc7b1)


## 📌 Setup Instructions

### 1️⃣ Prerequisites
Before you start, ensure you have:
- **Vagrant** installed → [Download Vagrant](https://www.vagrantup.com/downloads)
- **VirtualBox** installed → [Download VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- **Git Bash or any terminal**

### 2️⃣ Clone This Repository
```sh
$ git clone [https://github.com/MohamedElweza/Automate-Deploying-Multi-Tier-Java-Web-Application]
```

### 3️⃣ Start the Virtual Machines
Run the following command to create and start all VMs:
```sh
$ vagrant up
```
⏳ **Note:** This may take a few minutes as it sets up all services automatically.

### 4️⃣ Shell Scripts for Automation
Each service is installed and configured using dedicated scripts:

| Script               | Purpose                      |
|----------------------|----------------------------|
| **nginx_setup.sh**  | Installs & configures Nginx |
| **mysql_setup.sh**  | Sets up MySQL database      |
| **memcache_setup.sh** | Configures Memcached     |
| **tomcat_setup.sh** | Deploys Tomcat server      |
| **rabbitmq_setup.sh** | Configures RabbitMQ     |

If needed, you can manually run any script inside the VM:
```sh
$ vagrant ssh <vm-name>
$ sudo bash /vagrant/scripts/nginx_setup.sh
```

## 🔥 Testing & Validation
Once all services are running, verify the setup:
```sh
$ curl -I http://localhost
```
You should receive an HTTP **200 OK** response.

## 👨‍💻 Contributors
- **Mohamed Elweza**
- **Nader Ashour**

---

📌 **Follow this repository for updates!**
✅ If you found this useful, don't forget to **star ⭐ the repo**!

💬 Feel free to open issues or contribute to improve this setup!
