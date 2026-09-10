# Linux Server Hardening

A comprehensive enterprise-style Linux server hardening project built on **Ubuntu Server 24.04.3 LTS**.

This project demonstrates the practical implementation of modern Linux security controls using a layered **Defense-in-Depth** approach. The objective was not only to secure the operating system, but also to validate each security control through hands-on testing and documentation.

---

# Project Overview

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

# Security Controls Implemented

## System Hardening

- Operating system updates
- UFW firewall configuration
- AppArmor verification
- Kernel hardening with sysctl
- Protection against SYN Flood attacks
- Reverse Path Filtering
- ICMP Redirect protection
- Source Routing protection

---

## Boot Security

- GRUB password protection
- Secure bootloader configuration

---

## Account Security

- Password complexity enforcement
- Password history
- Password expiration
- Account inactivity lock
- Account lockout after failed authentication
- Least Privilege implementation
- Sudo hardening
- UID 0 verification
- Passwordless account verification

---

## SSH Security

- Ed25519 key authentication
- Password authentication disabled
- Root login disabled
- Restricted SSH users
- Session timeout configuration
- SSH tunnel restrictions
- Public key authentication only
- Cloud-init override protection

---

## Network Security

### UFW

- Default deny policy
- Restricted SSH access
- Trusted IP allow-list

### iptables

- Default DROP policy
- Stateful firewall
- Loopback protection
- Restricted SSH access

### Fail2Ban

- Automatic brute-force detection
- Dynamic IP banning
- SSH protection

---

## Storage Security

- Dedicated encrypted security partition
- LUKS Full Disk Encryption
- Secure mount options
- Automatic encrypted volume mounting
- ext4 filesystem

Mount hardening includes:

- noexec
- nosuid
- nodev
- acl
- nofail

---

## Access Control

- Access Control Lists (ACL)
- User-based permission management
- Principle of Least Privilege

---

## Monitoring & Detection

- Linux Audit Framework (auditd)
- File Integrity Monitoring
- User activity monitoring
- Permission change auditing
- Sudo auditing
- Critical event logging

---

## Vulnerability Assessment

The hardened server was validated using **Nessus Essentials Vulnerability Scanner**.

The assessment confirmed a significantly reduced attack surface.

Additional mitigation included:

- ICMP Timestamp Response protection
- Information disclosure reduction
- Network fingerprinting mitigation

---

# Technologies

- Ubuntu Server 24.04.3 LTS
- VMware Workstation
- OpenSSH
- UFW
- iptables
- Fail2Ban
- LUKS
- ext4
- ACL
- AppArmor
- auditd
- PAM
- sysctl
- GRUB
- Nessus Essentials

---

# Skills Demonstrated

- Linux System Administration
- Linux Hardening
- Enterprise Security
- Secure Remote Administration
- Firewall Configuration
- Encryption
- Access Control
- Privileged Access Management
- Security Monitoring
- Vulnerability Management
- Security Documentation

---

# Validation

Each security control implemented in this project was verified through practical testing.

Validation includes:

- Authentication testing
- Firewall testing
- SSH security verification
- Fail2Ban attack simulation
- ACL permission validation
- LUKS encrypted storage validation
- Auditd event verification
- Nessus vulnerability scanning

---

# Repository Contents

```
Linux-Server-Hardening.pdf
README.md
screenshots/
```

---

# Security Approach

This project follows the **Defense-in-Depth** security model by combining multiple complementary security layers:

- Prevention
- Hardening
- Access Control
- Monitoring
- Detection
- Validation

The objective is to minimize the attack surface while maintaining secure and manageable system administration.

---

# Author

**Shlomi Green**

Cybersecurity | Linux Security | SOC | System Administration

---

> **Disclaimer**
>
> This project was developed in an isolated virtual laboratory environment for educational purposes. All configurations, testing activities, and security validations were performed on systems owned and controlled by the author.
