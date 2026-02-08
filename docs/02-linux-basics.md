# 02: Linux Basics - Users, Packages, Filesystem

## System Baseline



## Package Management
sudo apt update
sudo apt upgrade -y

## User & Group Management
sudo useradd -m -s /bin/bash labuser
echo "labuser:linuxlab123" | sudo chpasswd
sudo usermod -aG sudo labuser
id labuser




## Key Skills Demonstrated
- Package updates via apt
- User creation (`-m -s`), password, sudo group
- `chown`/`chmod` permissions
- `id`/`getent` verification


