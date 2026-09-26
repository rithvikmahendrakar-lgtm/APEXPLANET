# Task-1: Foundations of Cybersecurity & Environment Setup

## Overview
This directory contains the deliverables and documentation for **Task-1** of the ApexPlanet Cybersecurity & Ethical Hacking Internship[cite: 1]. It covers core cybersecurity principles, lab setup, Linux CLI navigation, networking basics, and cryptography fundamentals[cite: 1].

---

## 1. Cybersecurity Fundamentals
* **CIA Triad:**
  * **Confidentiality:** Ensuring data is accessible only to authorized users.
  * **Integrity:** Safeguarding accuracy and completeness of information from unauthorized modifications.
  * **Availability:** Ensuring timely and reliable access to data and systems for authorized parties.
* **Threat Types Explored:** Phishing, Malware, DDoS, SQL Injection, Brute Force, and Ransomware[cite: 1].
* **Attack Vectors:** Social Engineering, Wireless Attacks, and Insider Threats[cite: 1].

---

## 2. Lab Environment Setup
* **Hypervisor:** VirtualBox / VMware Workstation[cite: 1].
* **Attacker Machine:** Kali Linux[cite: 1].
* **Target Machine:** Metasploitable2 / DVWA[cite: 1].
* **Network Configuration:** Host-Only Isolated Network for safe testing[cite: 1].

---

## 3. Cryptography Hands-On Execution
### AES-256 Symmetric Encryption (OpenSSL)
\\\ash
# 1. Create a secret file
echo "Task 1 Cryptography Demo" > secret.txt

# 2. Encrypt using AES-256
openssl enc -aes-256-cbc -pbkdf2 -salt -in secret.txt -out secret.enc

# 3. Decrypt back
openssl enc -d -aes-256-cbc -pbkdf2 -in secret.enc -out decrypted.txt

# 4. Read the decrypted file
cat decrypted.txt
\\\

### Execution Screenshots
![Terminal Output 1](./screenshot1.jpeg)
![Terminal Output 2](./screenshot2.jpeg)

---

## 4. Linux & Networking Cheat-Sheet

| Command | Category | Description |
| :--- | :--- | :--- |
| \pwd\ | File System | Print current working directory |
| \ls -la\ | File System | List all files including hidden ones with permissions |
| \cd <dir>\ | File System | Change directory |
| \chmod 755 <file>\ | Permissions | Change file read/write/execute permissions |
| \chown user:group\ | Permissions | Change file owner and group |
| \sudo apt update\ | Package Mgr | Update repository package lists |
| \ip a\ / \ifconfig\ | Networking | Display network interface details and IP address |
| \ping -c 4 <ip>\ | Networking | Send ICMP ECHO_REQUEST packets to check connectivity |
| \
etstat -tunlp\ | Networking | Display active listening ports and connections |
| \	raceroute <ip>\ | Networking | Trace the network route to a remote target |

---

## 5. Tool Familiarization
* **Wireshark:** Captured ICMP and HTTP packet flows on the isolated interface[cite: 1].
* **Nmap:** Verified target reachability and open ports[cite: 1].
* **Burp Suite:** Tested proxy setup for web traffic interception[cite: 1].
