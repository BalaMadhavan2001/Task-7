# TASK 7: Monitor System Resources Using Netdata

## 🎯 Objective
Install **Netdata** and visualize system and application performance metrics on an **EC2 Ubuntu Instance** using Docker.

---

## 🛠 Tools Used
- **Netdata** (Free, open-source monitoring tool)
- **Docker**
- **AWS EC2 (Ubuntu Instance)**

---

## 📌 Steps to Run

### 1. Install Docker
```bash
sudo apt update -y
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker

Run Netdata via Docker

sudo docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata


Netdata logs are available at:

sudo docker exec -it netdata ls /var/log/netdata
sudo docker exec -it netdata cat /var/log/netdata/error.log

## 📸 Screenshot

![Netdata Dashboard] (Screenshot 2025-08-24 105111.png)

![Netdata Dashboard] (



