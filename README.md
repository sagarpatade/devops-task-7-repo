# Task 7 – Monitor System Resources Using Netdata

## 📌 Objective
Install **Netdata** using Docker to monitor system and application performance metrics in real time.

---

## 🛠 Tools Used
- **Docker** – For containerized deployment
- **Netdata** – Open-source monitoring tool
- **Web Browser** – To access the Netdata dashboard

---

## 🚀 Steps Performed

### 1. Pulled & Ran the Netdata Container
```bash
docker run -d --name=netdata -p 19999:19999 --cap-add SYS_PTRACE --security-opt apparmor=unconfined netdata/netdata
2. Verified Container Running
CONTAINER ID   IMAGE                                                     COMMAND               STATUS                                   PORTS
d2dd13005d661f9f25325927d15ff24d713014408dd7be87802c28f567d1e21e       netdata/netdata   "/usr/sbin/run.sh"       Up 2 minutes    0.0.0.0:19999->19999/tcp
3. Accessed Netdata Dashboard
Opened a browser and visited:
http://localhost:19999
Or, if needed:
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' netdata
Then open:
http://172.17.0.2:19999
📊 Monitored Metrics
CPU usage per core

Memory usage

Disk I/O

Network traffic

Docker container statistics

System load averages

📷 Screenshots

