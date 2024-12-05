# Ubuntu Shell Commands Documentation

| **Command**                                   | **Description**                                                        |
|-----------------------------------------------|------------------------------------------------------------------------|
| `scp /path/to/file user@server:/path/to/destination` | Copy file from local to server.                                        |
| `df -h`                                       | Check the amount of free space.                                        |
| `sudo ufw status`                             | Check the status of the firewall.                                      |
| `sudo ufw allow from remote_IP_address to any port 3306` | Allow external IP to access port 3306.                                |
| `scp user@remote_host:remote_file local_file` | Download file from remote to local.                                    |
| `scp local_file user@remote_host:remote_file` | Upload file from local to remote.                                      |
| `service elasticsearch restart`              | Restart the Elasticsearch service.                                     |
| `sudo -s`                                     | Log in as root.                                                        |
| `cat /proc/<process_id>/maps`                 | Show the current virtual memory usage of a Linux process.              |
| `ip r`                                        | Display IP of the server.                                              |
| `lsof -i :9000`                               | List the process running on port 9000.                                 |
| `journalctl -u minio.service -n 100 --no-pager` | List the last 100 logs for a specific service.                         |
| `sudo resize2fs /dev/disk/by-id/scsi-0DO_example` | Resize a volume.                                                      |
| `ps -ax | grep myprocessname`                 | Search processes by name.                                              |
| `kill -9 PROCESS_ID`                          | Kill a process by its PID.                                             |