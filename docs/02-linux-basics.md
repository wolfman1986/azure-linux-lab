# 02: Linux Fundamentals - Ubuntu 24.04

## System Baseline
![System Info](photos/System%20Baseline.png)

## Package Updates
sudo apt update && sudo apt upgrade -y

![Apt Update](photos/update-upgrade.png)

## User & Permissions Management
**Create labuser + sudo:**

sudo useradd -m -s /bin/bash labuser
echo "labuser:linuxlab123" | sudo chpasswd
sudo usermod -aG sudo labuser

![User Management](photos/user-management.png)

**Isolation Demo:**

![Permissions Demo](photos/permissions-demo.png)

## Skills Demonstrated
- System inspection (`lsb_release`, `df`, `free`)
- Apt lifecycle (update/upgrade)
- User provisioning, sudo groups
- Filesystem isolation/permissions
