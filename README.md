# DoS-Attack-Simulation-and-Detection-using-Snort
Developed a controlled virtual lab environment to simulate and detect Denial-of-Service (DoS) attacks using Snort as a Network Intrusion Detection System (NIDS). Custom detection rules were implemented to identify ICMP and TCP SYN flood activities generated from an attacker machine, with real-time alert monitoring via the command-line interface.

## Disclaimer
This project was conducted strictly in a controlled and isolated lab environment for educational purposes only.

## Lab Environment
- **Attacker Machine:** Kali Linux  
- **Target Machine:** Ubuntu Server  
- **Tool:** Snort (NIDS), Traffic Simulation Tools (e.g., DDoS Ripper, Raven-Storm)  
- **Network Type:** Host-only / Isolated Network  

## Analysis Flow

<b>1. Lab Setup</b><br>
This stage presents the configuration of a virtual penetration testing environment. The Kali Linux machine acts as the attacker with IP address **192.168.56.102**, while the Ubuntu server functions as the target system with IP address **192.168.56.103**.

Both systems are connected within the same isolated network (**192.168.56.0/24**), enabling direct communication between attacker and target. This setup allows safe simulation of attack scenarios and evaluation of intrusion detection mechanisms such as Snort.

<br>

<b>2. ICMP Flood Simulation</b><br>
An ICMP flood attack is initiated from the attacker machine targeting the Ubuntu server. A high volume of ICMP packets is transmitted within a short time frame, simulating a Denial-of-Service (DoS) condition by overwhelming the target with continuous requests.

This scenario is used to generate abnormal traffic behavior for analysis and detection.

<br>

<b>3. ICMP Flood Detection</b><br>
Snort detects the ICMP flood activity based on custom rules. Alerts are triggered due to excessive ICMP traffic originating from the attacker (**192.168.56.102**) and targeting the server (**192.168.56.103**).

This demonstrates Snort’s capability to monitor network traffic in real time and identify abnormal patterns indicative of a potential DoS attack.

<br>

<b>4. TCP SYN Flood Simulation</b><br>
A TCP SYN flood attack is launched from the attacker machine targeting the Ubuntu server on port 80. A large number of SYN packets are sent to initiate incomplete TCP handshakes, consuming system resources and preventing legitimate connections.

This simulates a service disruption scenario typical of a DoS attack.

<br>

<b>5. TCP SYN Flood Detection</b><br>
Snort detects the SYN flood attack by identifying repeated TCP connection attempts with high frequency and varying source ports. Alerts are generated based on custom rules designed to flag excessive SYN packets within a short time interval.

This highlights Snort’s effectiveness as a Network Intrusion Detection System (NIDS) in analyzing TCP traffic patterns and detecting potential DoS attacks in real time.
