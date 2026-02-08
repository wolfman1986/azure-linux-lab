# Azure Linux Lab: Basic Ubuntu Admin Demo

[![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=azure&logoColor=white)](https://azure.microsoft.com/)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)](https://ubuntu.com/)

## Overview
This repo documents a hands-on Azure lab demonstrating basic Linux (Ubuntu 22.04 LTS) administration skills:
- Azure IaaS: VM provisioning, SSH key auth, NSG hardening.
- Ubuntu basics: users, packages, services, filesystem, networking, troubleshooting.
- Deploy a simple nginx web server with UFW firewall.

**Skills shown:** Azure portal deployment, secure SSH access, systemd management, basic security hardening. [web:22][web:27]

## Lab Modules
1. [Azure VM Setup (SSH keys, NSG)](docs/01-azure-setup.md)
2. [Linux Basics (users, packages, files)](docs/02-linux-basics.md)
3. [Services & Networking (nginx, UFW)](docs/03-services-networking.md)

## Prerequisites
- Free Azure subscription (sign up at [azure.microsoft.com/free](https://azure.microsoft.com/free)).
- SSH client (Windows: OpenSSH in PowerShell; macOS/Linux: built-in).
- Lab cost: ~$0.02/hour for B1s VM (delete when done).

## Architecture
nternet (your IP only) --> NSG (SSH:22) --> Ubuntu VM (nginx:80 local only)


## Teardown
Run `az group delete --name <rg-name>` or delete via portal to avoid charges.

---
*Built step-by-step for cybersecurity portfolio. Author: yourusername*
