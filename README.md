# 🐧 Linux Server Hardening

![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04%20LTS-E95420?logo=ubuntu&logoColor=white)
![Security](https://img.shields.io/badge/Defense--in--Depth-Hardening-red)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A comprehensive enterprise-style Linux server hardening project built on **Ubuntu Server 24.04.3 LTS**.

This project demonstrates the practical implementation of modern Linux security controls using a layered **Defense-in-Depth** approach. The objective was not only to secure the operating system, but also to validate each security control through hands-on testing and documentation.

---

## 📖 Table of Contents

- [Project Overview](#project-overview)
- [Security Controls Implemented](#security-controls-implemented)
- [Technologies](#technologies)
- [Skills Demonstrated](#skills-demonstrated)
- [Validation](#validation)
- [Repository Contents](#repository-contents)
- [Security Approach](#security-approach)
- [Disclaimer](#disclaimer)

---

## Project Overview

The project covers the complete lifecycle of Linux server hardening, including:

- Operating System Hardening
- Kernel Security (sysctl)
- GRUB Boot Protection
- Password Policy Enforcement (PAM)
- SSH Hardening
- Firewall Configuration (UFW & iptables)
- Fail2Ban Intrusion Prevention
- Secure Storage with LUKS Encryption
- Secure Mount Options
- Access Control Lists (ACL)
- Linux Audit Framework (auditd)
- File Integrity & User Activity Monitoring
- Vulnerability Assessment with Nessus Essentials

Every implemented security mechanism was verified through practical testing to ensure the configuration operated as expected.

---

## Security Controls Implemented

### System Hardening
- Operating system updates
- UFW firewall configuration
- AppArmor verification
- Kernel hardening with sysctl
- Protection against SYN Flood attacks
- Reverse Path Filtering
- ICMP Redirect protection
- Source Routing protection

### Boot Security
- GRUB password protection
- Secure bootloader configuration

### Account Security
- Password complexity enforcement
- Password history and expiration
- Account inactivity lock
- Account lockout after failed authentication
- Least Privilege implementation
- Sudo hardening
- UID 0 and passwordless account verification

### SSH Security
- Ed25519 key authentication
- Password authentication disabled
- Root login disabled
- Restricted SSH users
- Session timeout configuration
- SSH tunnel restrictions
- Cloud-init override protection

### Network Security

**UFW:** default deny policy · restricted SSH access · trusted IP allow-list

**iptables:** default DROP policy · stateful firewall · loopback protection

**Fail2Ban:** automatic brute-force detection · dynamic IP banning · SSH protection

### Storage Security
- Dedicated encrypted security partition (LUKS Full Disk Encryption)
- Secure mount options: `noexec`, `nosuid`, `nodev`, `acl`, `nofail`
- Automatic encrypted volume mounting (ext4)

### Access Control
- Access Control Lists (ACL)
- User-based permission management
- Principle of Least Privilege

### Monitoring & Detection
- Linux Audit Framework (auditd)
- File integrity and user activity monitoring
- Permission change and sudo auditing
- Critical event logging

### Vulnerability Assessment

The hardened server was validated using **Nessus Essentials Vulnerability Scanner**, confirming a significantly reduced attack surface, including:
- ICMP Timestamp Response protection
- Information disclosure reduction
- Network fingerprinting mitigation

---

## Technologies

`Ubuntu Server 24.04.3 LTS` · `VMware Workstation` · `OpenSSH` · `UFW` · `iptables` · `Fail2Ban` · `LUKS` · `ext4` · `ACL` · `AppArmor` · `auditd` · `PAM` · `sysctl` · `GRUB` · `Nessus Essentials`

---

## Skills Demonstrated

`Linux System Administration` · `Linux Hardening` · `Enterprise Security` · `Secure Remote Administration` · `Firewall Configuration` · `Encryption` · `Access Control` · `Privileged Access Management` · `Security Monitoring` · `Vulnerability Management` · `Security Documentation`

---

## Validation

Each security control implemented in this project was verified through practical testing:

- Authentication testing
- Firewall testing
- SSH security verification
- Fail2Ban attack simulation
- ACL permission validation
- LUKS encrypted storage validation
- Auditd event verification
- Nessus vulnerability scanning

---

## Repository Contents

```
linux-server-hardening/
├── docs/
│   └── Linux-Server-Hardening.pdf   # Full project documentation
└── README.md
```

---

## Security Approach

This project follows the **Defense-in-Depth** security model by combining multiple complementary security layers:

`Prevention` → `Hardening` → `Access Control` → `Monitoring` → `Detection` → `Validation`

The objective is to minimize the attack surface while maintaining secure and manageable system administration.

---

## Author

**Shlomi Green**
Cybersecurity | Linux Security | SOC | System Administration

---

## Disclaimer

> This project was developed in an isolated virtual laboratory environment for educational purposes. All configurations, testing activities, and security validations were performed on systems owned and controlled by the author.
