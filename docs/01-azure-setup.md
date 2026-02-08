# 01: Azure VM Setup + Secure SSH Access

## Architecture
Internet (My IP → SSH/22 only) ── NSG ── Ubuntu 24.04 VM (48.192.9.212)


## Resources Deployed
| Type | Name | Region | Size/Cost |
|------|------|--------|-----------|
| Resource Group | `rg-azure-linux-lab` | West US 2 | - |
| SSH Key Pair | `ssh-azure-linux-lab-v2` | West US 2 | RSA 2048 |
| Virtual Machine | `vm-azure-linux-lab` | West US 2 | B1ls (~$0.004/hr) [web:22] |
| VNet | `vnet-azure-linux-lab` | West US 2 | - |
| Public IP | `pip-azure-linux-lab` | West US 2 | Static |

## Security: NSG Rule
- **Name**: `SSH-from-my-IP` (Priority 100)
- Source: **My IP**
- Port: **22/TCP** → Allow [web:22]

## Windows SSH Setup
C:\temp\ssh-azure-linux-lab-v2.pem
icacls ssh-azure-linux-lab-v2.pem /inheritance:r /grant ashto:R
ssh -i .\ssh-azure-linux-lab-v2.pem azureuser@48.192.9.212


## Troubleshooting (Real-world)
1. **OneDrive sync broke permissions** → Moved to `C:\temp`.
2. **Portal v1 PEM permissions** → Regenerated `ssh-azure-linux-lab-v2`.
3. **VM rejected v2 key** → Portal **Reset password** > **Reset SSH public key** > Select v2.
4. VM restarted, SSH ✅.

**Cost so far:** ~$0.01. Delete RG when done.


