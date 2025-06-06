# 🖥️ System Monitoring with Netdata 

## 📌 Objective
Deploy Netdata using Docker to monitor system and application performance in real time.

## 🛠️ Tools Used
- **Netdata** (open-source monitoring platform)
- **Docker** 

## 🚀 Setup Instructions

1. **Run Netdata in Docker**(Make sure Docker is installed):
   ```bash
   docker run -d --name=netdata -p 19999:19999 --cap-add SYS_PTRACE \
     -v netdataconfig:/etc/netdata \
     -v netdatalib:/var/lib/netdata \
     -v netdatacache:/var/cache/netdata \
     -v /etc/passwd:/host/etc/passwd:ro \
     -v /etc/group:/host/etc/group:ro \
     -v /proc:/host/proc:ro \
     -v /sys:/host/sys:ro \
     -v /etc/os-release:/host/etc/os-release:ro \
     netdata/netdata
2. Access Dashboard:
  Open your browser and go to 👉 http://localhost:19999
