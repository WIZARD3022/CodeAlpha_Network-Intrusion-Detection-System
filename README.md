# CodeAlpha_Network-Intrusion-Detection-System
In the project we are going to use snort tool to monitor suspicious activity performed in the network .
## Step-by-step Procedure: -
1. Open terminal and write the command.
   ```
   sudo apt update
   ```
2. Now for installation of snort tool write command
   ```
   sudo apt install snort
   ```
   press y and then enter if asked.
3. On the pop up box change the 16 to 24 and click ok button.
4. Now check the current ip address of your machine with command.
   ```
   ifconfig
   ```
5. Now write command
   ```
   sudo nano /etc/snort/snort.conf
   ```
6. In the file scroll down to ipvar HOME_NET any and change this <any> with your current ip address.
7. Now write the command.
   ```
   sudo snort -T -c /etc/snort/snort.conf -i <network_type>
   ```
   this <network_type> is also found with ip. such it can be eth0, eth1, etc.
8.  Now the successfully validated is showing and if not make confirm the last steps.
9.  Now write the command.
   ```
   sudo snort -A console -q -u snort -g snort -c /etc/snort/snort.conf -i <network_type>
   ```
10. Now your network monitering is started and if any on attack on your machine it display attack type and attacker ip address.
## About: -
A Network Intrusion Detection System (NIDS) is a security tool used to monitor and analyze network traffic for signs of unauthorized access, suspicious activity, or policy violations. NIDS works by inspecting incoming and outgoing network packets and comparing them against a database of known attack signatures or by identifying anomalies that may indicate malicious activity.
## Tool Used: -
Snort is one of the most popular and widely-used NIDS. It operates in various modes, including packet sniffing, logging, and intrusion detection.
