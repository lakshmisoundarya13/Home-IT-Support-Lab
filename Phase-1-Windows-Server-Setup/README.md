# Phase 1 — Windows Server Setup

## Objective
Install and configure Windows Server 2019 as the foundation for the Domain Controller (DC01).

## Steps Completed

### 1. Created Virtual Machine in VirtualBox
- VM Name: DC01
- OS: Windows Server 2019 (64-bit)
- RAM: 2048 MB
- Storage: 40 GB
- Network Adapter 1: NAT (internet access)
- Network Adapter 2: Internal Network — labnetwork

### 2. Installed Windows Server 2019
- Downloaded Windows Server 2019 Evaluation ISO
- Selected: Windows Server 2019 Standard Evaluation (Desktop Experience)
- Performed clean custom installation on 40GB virtual disk

### 3. Renamed Server to DC01
- Opened Server Manager → Local Server
- Changed computer name from random name to DC01
- Restarted to apply changes

## Screenshots
| Screenshot | Description |
|---|---|
| 01-windows-server-desktop.png | Windows Server 2019 desktop after installation |
| 02-server-manager-dashboard.png | Server Manager dashboard |
| 03-dc01-local-server-properties.png | Local Server properties showing DC01 |

## Key Learning
Windows Server 2019 is the industry standard for enterprise Domain Controllers. 
Naming conventions like DC01 follow real enterprise IT standards used in companies worldwide.
