# How to replace Buffalo NAS Linux

## Introduction

This guide provides step-by-step instructions on how to replace the Linux operating system on a Buffalo Network Attached Storage (NAS) device. Before proceeding, ensure you have a functioning Buffalo NAS device and are connected to the same Local Area Network (LAN) as the device.

## Prerequisites

* Java Runtime Environment (JRE) installed on your computer.
* ACP_Commander tool downloaded from here.


## Procedure

### 1. Locate the Device on Your Network

Ensure your computer is connected to the same LAN as your Buffalo NAS device.

   ```bash
   java -jar acp_commander.jar -f
   ```
   This command will display the IP address of your NAS device.

   **Note**: If the command fails to find the device, check your router's firewall settings and ensure they are configured to allow the necessary traffic.

### 2. Establish a Connection to the NAS Device

   ```bash
   java -jar acp_commander.jar -t <ip_address> -pw <admin_password> -s
   ```

   Replace <ip_address> with the IP address of your NAS device, and <admin_password> with the admin password of your NAS device.

### 3. Configure Firewall Settings (Optional)
Ensure your firewall settings allow traffic on UDP port 22936, which is required for communication with the NAS device.

For Ubuntu users with Uncomplicated Firewall (UFW) installed, use the following command to allow traffic on this port:

   ```bash
   sudo ufw allow 22936/udp
   ```

## Resources

* [1] https://github.com/1000001101000/Debian_on_Buffalo/wiki/Preparing-Device-for-Debian-Install#prepare-the-device-for-the-install
* [2] https://github.com/rogers0/OpenLinkstation
* [3] https://sudonull.com/post/126620-Installing-Debian-Wheezy-on-Buffalo-Linkstation-Pro
* [4] https://wiki.slimdevices.com/index.php/NAS_Compatibility.html
* [5] https://forums.buffalotech.com/index.php?topic=35579.0
* 