<p align="center">
<img src="https://www.pngfind.com/pngs/m/36-364985_network-comptia-network-logo-hd-png-download.png" alt="Traffic Examination"/>
</p>

<h1>CompTIA Network+ Labs</h1>



<h2>Configuring a SOHO Router</h2>

- ### [Configuring a SOHO Router](https://youtu.be/klZqPhz97lU?si=oPs6IjTPHWI5errZ)

## Configuring and Diagnosing Router Settings with OpenWRT

### Overview

In this lab, the **Secure Shell (SSH)** protocol was used to connect to an OpenWRT router, a widely used open-source firmware for network devices. The focus was on exploring the capabilities of the router's web-based interface and understanding the various configuration options, diagnostic tools, and administrative functionalities available. The lab demonstrated the importance of secure and efficient router configuration for network management.

---

### Key Activities

#### 1. **SSH Connection to OpenWRT**
- **Accessing the Router:** 
  - The lab began by establishing a secure connection to the OpenWRT router using SSH. This approach allowed command-line access to the router for administrative tasks that might not be accessible via the web interface.
  - SSH also provided a secure communication channel, ensuring that sensitive administrative credentials and data were not transmitted in plaintext.
- **Commands Executed:** Common OpenWRT administrative commands were explored to retrieve information about the router's configuration and operational status.

#### 2. **Exploring the Web Interface**
After gaining an understanding of the router’s basic settings through SSH, the web interface was accessed to interactively explore its features, including:

- **Basic Configuration:**
  - **Network Interfaces:** Viewing and configuring LAN, WAN, and wireless interfaces.
  - **DHCP Settings:** Managing IP address distribution and DNS settings for connected devices.
  - **Firewall Rules:** Configuring basic firewall settings to manage incoming and outgoing traffic.

- **Advanced Features:**
  - **Quality of Service (QoS):** Managing bandwidth allocation to prioritize critical network traffic.
  - **Dynamic Host Configuration Protocol (DHCP) Leases:** Monitoring active devices and assigning static IPs.
  - **Port Forwarding:** Configuring port forwarding rules for specific devices and services.

- **Diagnostics:**
  - **Ping and Traceroute Tools:** Testing connectivity to internal and external networks.
  - **System Logs:** Viewing and analyzing logs to identify potential issues or security events.
  - **Real-Time Monitoring:** Observing bandwidth usage, connected devices, and network health metrics.

#### 3. **Router Security and Optimization**
The lab emphasized the importance of securing the router and optimizing its performance, including:
- **Changing Default Credentials:** Updating the router's administrative username and password to prevent unauthorized access.
- **Disabling Unused Services:** Ensuring that only necessary services are active to reduce the router’s attack surface.
- **Firmware Updates:** Checking for and applying updates to ensure the router has the latest security patches and features.

---

### Lessons Learned

- **Router Management:** The combination of SSH and the web interface provides administrators with powerful tools for configuring and managing OpenWRT routers.
- **Secure Access:** Using SSH ensures secure remote access to the router, while the web interface offers a user-friendly way to perform more complex configurations.
- **Diagnostics and Troubleshooting:** Built-in diagnostic tools like ping, traceroute, and system logs are essential for identifying and resolving network issues.
- **Proactive Security Measures:** Regular updates and disabling unused services are critical to maintaining a secure and resilient network environment.

---

This lab demonstrated the versatility of OpenWRT routers and the importance of understanding both command-line and graphical management tools in ensuring efficient and secure network operations.


<h2>Capturing Network Traffic</h2>

- ### [Capturing Network Traffic](https://youtu.be/AgQO20GmsvM?si=esR2TZBfZu1JQru9)

## Capturing and Analyzing Network Traffic

### Overview

In this lab, the focus was on capturing, analyzing, and interpreting network traffic using a combination of command-line tools and graphical analysis software. Tools like **tcpdump**, **nmap**, and **ping** were used to generate and capture network traffic, which was then redirected into files for detailed analysis. Finally, **Wireshark** was used to examine these captures in a more user-friendly, graphical format, enabling deeper insights into the network activity.

---

### Key Activities

#### 1. **Network Traffic Capture**
The lab utilized **tcpdump**, a powerful packet-sniffing tool, to capture various types of network traffic:
- **Command Usage:** 
  - Capturing traffic from a specific interface:  
    ```bash
    tcpdump -i eth0 -w capture.pcap
    ```
  - Filtering specific traffic types (e.g., ICMP, TCP, or HTTP):  
    ```bash
    tcpdump -i eth0 icmp -w icmp_traffic.pcap
    ```
- **Traffic Generation:**
  - **Ping:** Used to generate ICMP traffic for testing connectivity between devices and observing packet exchange.
  - **Nmap:** Employed to perform network scans, generating traffic related to service discovery, port scanning, and host enumeration.

Captured traffic was redirected into `.pcap` files for later analysis.

#### 2. **Traffic Analysis with Wireshark**
The captured `.pcap` files were imported into **Wireshark**, a popular network protocol analyzer, for detailed inspection:
- **Features Explored:**
  - **Protocol Filtering:** Wireshark's advanced filtering capabilities (`tcp`, `udp`, `icmp`) were used to isolate specific types of traffic for analysis.
  - **Packet Details:** Examined packet headers to extract details such as:
    - Source and destination IP addresses.
    - Protocol-specific data (e.g., sequence numbers in TCP or type codes in ICMP).
    - Application-layer payloads (e.g., HTTP or DNS requests).
  - **Statistics and Visualizations:** Utilized Wireshark's built-in tools to generate:
    - Protocol hierarchy statistics.
    - Communication flow diagrams.
    - Graphical representations of traffic over time.
- **Insights Gained:** Wireshark provided an intuitive way to view and interpret raw packet data captured by **tcpdump**, making it easier to understand network behavior and pinpoint anomalies.

---

### Lessons Learned

- **Traffic Capture and Generation:** Combining tools like **tcpdump**, **nmap**, and **ping** is an effective way to simulate and capture diverse network traffic for analysis.
- **File Redirection for Reusability:** Redirecting captured traffic to `.pcap` files allows for storage and later examination, making it an invaluable practice for troubleshooting or forensic purposes.
- **Wireshark for Analysis:** 
  - The graphical interface of Wireshark simplifies the process of dissecting and interpreting complex network data.
  - Its advanced features, such as protocol filtering and traffic visualization, make it an essential tool for both beginners and experienced network administrators.
- **Practical Applications:** This lab demonstrated how these tools can be used for tasks like diagnosing connectivity issues, identifying potential intrusions, and understanding network communication patterns.

---

### Conclusion

This lab provided hands-on experience with capturing and analyzing network traffic, emphasizing the importance of combining command-line tools like **tcpdump** with graphical tools like **Wireshark** for a comprehensive approach to network monitoring and diagnostics. The techniques and tools explored are foundational skills for network administrators and security professionals alike.
