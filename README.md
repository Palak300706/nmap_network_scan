Basic Network Scanning with Nmap

Introduction

Nmap (Network Mapper) is an open-source network scanning tool used for discovering hosts, identifying open ports, detecting running services, and performing network security analysis.

This project demonstrates a basic network scan performed on the localhost machine using Nmap in Kali Linux.

Objective

The objective of this task is to:
- Install Nmap
- Perform a network scan
- Identify open ports and services
- Analyze the significance of open ports

Tool Used

- Nmap

Installation

Nmap was installed using the following command:

sudo apt update
sudo apt install nmap -y

Command Used for Scanning


nmap localhost -oN nmap_scan_results.txt

Scan Output Summary

The scan was performed on localhost (127.0.0.1). The system was active and reachable.

The following open ports were identified:

1. Port 80 (HTTP)

State: Open
Service: HTTP

Explanation:

Port 80 is used for HTTP (HyperText Transfer Protocol), which is commonly used by web servers to deliver web pages and web applications.

Significance:

* Indicates that a web server is running
* Allows browser communication
* Commonly used for websites and web applications

Security Consideration:
If not properly secured, web servers may become vulnerable to attacks such as:

* SQL Injection
* Cross-Site Scripting (XSS)
* Directory Traversal

2. Port 3306 (MySQL)

State: Open
Service: MySQL

Explanation:

Port 3306 is the default port used by MySQL/MariaDB database servers.

Significance:

* Indicates a database service is running
* Used for database communication between applications and servers

Security Consideration:
Exposed database ports may lead to:

* Unauthorized database access
* Data theft
* Brute-force attacks

Proper authentication and firewall rules are important to secure database services.

Closed Ports

The scan reported that 998 TCP ports were closed. Closed ports reduce the attack surface because they do not accept incoming connections.

Scan Timing

The scan completed successfully in approximately 0.12 seconds, showing that the localhost system responded quickly.

Conclusion

The Nmap scan successfully identified active services running on the localhost machine. Open ports 80 and 3306 indicate that HTTP and MySQL services are active on the system.

Regular network scanning helps administrators:

* Identify exposed services
* Monitor network security
* Detect unnecessary open ports
* Reduce cybersecurity risks

Nmap is an essential tool for cybersecurity professionals and network administrators for performing security assessments and network analysis.
