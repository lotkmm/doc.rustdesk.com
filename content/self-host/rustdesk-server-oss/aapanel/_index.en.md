---
title: aaPanel
weight: 40
---
aaPanel(Applicable versions 7.0.11 and above) Deployment guidelines
## Precondition
Go to [aaPanel official website] ( https://www.aapanel.com/new/download.html ), Select the script to download and install
(Skip this step if you already have it installed)

## Deployment

#### Step 1:
Log in to aaPanel and click Docker in the menu bar, first time you will be prompted to install the Docker and Docker Compose services, click Install Now.
    If it is already installed, please ignore it.

#### Step 2:
After the installation is complete, find `RustDesk` in One-Click Install and click install


#### Step 3:
configure basic information such as the domain name and port to complete the installation

- Name: App name, default 'RustDesk- random characters'
- Version selection: default '1.1.11'
- Allow external access: Please check
-Port: By default, hbbs listens to 21115(tcp), 21116(tcp/udp), 21118(tcp), and hbbr listens to 21117(tcp), 21119(tcp). Be sure to open these ports in the firewall. Please note that 21116 requires both TCP and UDP to be enabled. Among them, 21115 is hbbs for NAT type test, 21116/UDP is hbbs for ID registration and heartbeat service, 21116/TCP is hbbs for TCP hole-punching and connection service, 21117 is hbbr for relay service, and 21118 and 21119 are for web client support. If you do not need web client (21118,21119) support, the corresponding port can not be opened.
- CPU core limit: 0 is unlimited and can be modified as needed
- Memory limit: 0 is unlimited and can be modified as needed

#### Step 4:
aaPanel will automatically initialize the app after submission, which will take about '1-3' minutes, and you'll be ready to use once it's done.
