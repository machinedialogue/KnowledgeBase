netstat -aon | findstr :8082

tasklist /fi "PID eq <PID from netstat>"
