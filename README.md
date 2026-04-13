# home-nas-infrastructure
Raspberry Pi + OpenMediaVault NAS with NFS, SMB, and rsync backups
# Home NAS Infrastructure (Raspberry Pi + OpenMediaVault)

## Overview

This project is a self-hosted Network Attached Storage (NAS) system built on Raspberry Pi hardware using OpenMediaVault. It provides centralized storage, file sharing, and backup capabilities across multiple Linux systems in a home network environment.

The system is designed to be lightweight, reliable, and accessible, while also serving as a platform for learning and managing real-world Linux infrastructure.

---

## Objectives

* Centralize data storage across multiple machines
* Enable reliable file sharing using NFS and SMB
* Implement efficient, incremental backup workflows
* Maintain a stable and recoverable storage environment
* Gain hands-on experience with Linux system administration and networking

---

## Hardware

* Raspberry Pi 4B (2GB RAM) running OpenMediaVault
* External USB storage (primary data drive)
* Network connection via Ethernet

---

## Software Stack

* OpenMediaVault (Debian-based NAS OS)
* NFS (primary file sharing protocol for Linux systems)
* SMB/CIFS (cross-platform file sharing)
* rsync (incremental file synchronization and backups)
* SSH (remote system administration)

---

## Network Configuration

* Static IP assigned to NAS: `192.168.12.245`

* Access via:

  * Web UI: `http://192.168.12.245`
  * SSH: `ssh user@192.168.12.245`

* Multi-client environment:

  * Arch-based system (Manjaro, Btrfs, encrypted SSD)
  * Debian-based system (Linux Mint)

---

## Storage & Filesystem

* Filesystem: EXT4 (NAS data drive)
* Mounted under `/srv` for shared access
* Organized shared directories for multi-system usage

---

## File Sharing

### NFS (Primary)

* Configured for Linux-to-Linux file sharing
* Mounted on client systems for direct filesystem access
* Used as a centralized “home directory”-style backend

### SMB (Secondary)

* Enabled for compatibility and fallback access
* Accessible across different operating systems

---

## Backup & Synchronization

* Incremental backups implemented using `rsync`
* Designed to push/pull updated data between NAS and client systems
* Reduces redundant data transfer and improves efficiency

---

## Key Features

* Centralized storage across multiple Linux machines
* Dual-protocol file sharing (NFS + SMB)
* Incremental backup system using rsync
* Persistent network configuration with static IP
* Remote management via SSH and web interface

---

## Troubleshooting & Lessons Learned

This project involved extensive real-world troubleshooting, including:

* Resolving network interface issues and restoring connectivity
* Diagnosing DHCP vs static IP conflicts
* Handling hostname and DNS/mDNS resolution problems
* Debugging NFS mount and permission issues
* Recovering system access after configuration changes
* Ensuring data integrity during transfers and updates

---

## Future Improvements

* Implement centralized DNS (e.g., Pi-hole or dnsmasq)
* Automate backup workflows with cron jobs
* Expand storage capacity with dedicated HDD
* Add monitoring and alerting for system health
* Improve redundancy and fault tolerance

---

## Summary

This project demonstrates practical experience in building and maintaining a Linux-based storage system, including networking, file sharing, and data management. It reflects hands-on system administration skills and the ability to troubleshoot and stabilize real-world infrastructure.

---
