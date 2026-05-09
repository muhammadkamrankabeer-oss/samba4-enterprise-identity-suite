# Samba4 Automated Enterprise Infrastructure
**An automated, production-ready Identity & Access Management (IAM) solution for small-to-mid-sized organizations.**

---

## 🚀 Overview
This project provides a fully automated deployment of a **Samba4 Active Directory Domain Controller** and **Debian Linux Clients**. It replaces expensive Windows Server licenses with a robust, open-source alternative capable of handling:
* **Centralized Authentication:** One username/password for all Linux workstations.
* **Automated Provisioning:** Rapid deployment of new clients via Ansible.
* **Enterprise Hardening:** Pre-configured security baselines (SSH, Firewalls, PAM).
* **Data Continuity:** Integrated user home-directory management and backup readiness.

## 🛠 Tech Stack
* **OS:** Debian 12 (Bookworm)
* **Identity:** Samba 4 AD-DC
* **Automation:** Ansible (Playbooks & Jinja2 Templates)
* **Virtualization:** Vagrant & VirtualBox
* **Security:** SSSD, Realmd, PAM, UFW

## 📦 Key Features
- [x] **Zero-Touch Domain Join:** Automated client renaming and AD integration based on network IP.
- [x] **Dynamic Hostname Logic:** PC naming convention (e.g., PC-21) handled via Ansible logic.
- [x] **Auto-Home Creation:** Automatic generation of local home directories upon first domain login.
- [x] **Hardened SSH:** Key-only authentication and secure service configuration.
- [ ] **Next Up (v2.0):** Real-time monitoring with Prometheus/Grafana and Automated SQL Backups.

## ⚙️ Quick Start
1. **Clone the Repo:** `git clone https://github.com/YOUR_USERNAME/samba4-automated-infrastructure`
2. **Launch Infrastructure:** `vagrant up`
3. **Run Automation:**
   ```bash
   ansible-playbook -i ansible/inventory/hosts.ini ansible/playbooks/join_clients.yml
