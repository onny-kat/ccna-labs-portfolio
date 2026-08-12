Building a lightweight system monitoring bot running in an Alpine container that generates structured logs or sends status alerts.

	Tech Stack: Alpine Linux, Docker, Shell Scripting (POSIX `sh`), Nginx, Git
	Key Accomplishments: 
		### Buld lightweight Docker container image using Alpine Linux.
		### Scripted automated deployment pipelines using Dockerfiles and shell automation scripts.
		### Managed virtual networking, port forwarding, and container service isolation.


```
#!/bin/sh 
# Alpine System Health Monitor 

# 1. Gather System Metrics 
TIMESTAMP=$(date "+%Y-%m-%d %H:%M:%S") 
MEM_FREE=$(free -m | awk '/Mem:/ { print $4 }') 
DISK_USAGE=$(df -h / | awk 'NR==2 { print $5 }') 

# 2. Define Thresholds MEM_THRESHOLD=200 

# 3. Format Output 
LOG_MSG="[$TIMESTAMP] Free Mem: ${MEM_FREE}MB | Disk Usage: ${DISK_USAGE}" 

# 4. Check Threshold & Alert 
if [ "$MEM_FREE" -lt "$MEM_THRESHOLD" ]; then LOG_MSG="$LOG_MSG | STATUS: WARNING (Low Memory)" 

else LOG_MSG="$LOG_MSG | STATUS: OK" 
fi 

# 5. Output to Terminal AND Append to Log File echo "$LOG_MSG" | tee -a /app/system_health.log

```

Execute and test the script 
```
# Give the script permission to run as a program, then execute it manually:
chmod +x monitor.sh 
./monitor.sh

# Check the log file
cat system_health.log
```

Set Up Cron Automation (Crontab)
