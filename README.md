# Network Troubleshooting Tools Guide
Guides to essential networking tools used in IT support roles.

## Tools Included
* Ping
* Tracert
* Ipconfig
* nslookup
* Netstat

# Tool: `ping`
The `ping` command is used to verify network connectivity by checking whether a host (domain name or IP address) is reachable and measuring the response time for data packets. 

### 1. Ping a domain
``` ping google.com ```
<img width="976" height="509" alt="Screenshot 2026-02-03 214518" src="https://github.com/user-attachments/assets/8b4d4d85-7809-447c-a51e-263a737c9f25" />

### 2. Ping a DNS server
``` ping 8.8.8.8 ```
<img width="975" height="510" alt="Screenshot 2026-02-03 214657" src="https://github.com/user-attachments/assets/54e0baff-8aca-418d-b90b-11541af194fe" />

# Tool: `tracert`
The `tracert` command shows the path packets take across a network and highlights where delays or connection issues occur.

### 1. Tracing your destination
``` tracert gooogle.com ```

<sup>Use this command to trace the route from your computer to a website or server. It lists all the routers along the way, and if any hop is slow or unresponsive, it could point to a network issue.<sup>

<img width="977" height="506" alt="Screenshot 2026-02-03 220321" src="https://github.com/user-attachments/assets/15100722-5a73-4ad7-aff3-4f87d986ef2a" />

### Tracing DNS
``` tracert 8.8.8.8 ```

<sup>This helps you see the path your network takes to reach a DNS server. It’s useful for troubleshooting slow or failing DNS lookups.<sup>

<img width="974" height="509" alt="Screenshot 2026-02-03 220756" src="https://github.com/user-attachments/assets/6d6388f0-b0e7-4e79-82ad-e084b4256783" />

# Tool: `ipconfig`
The `ipconfig` command shows and manages a Windows computer’s IP configuration. It’s commonly used for troubleshooting network issues and refreshing DHCP settings.

### 1. View IP Configuration
```ipconfig```

<sup>Shows and manages your Windows computer’s IP configuration. Useful for troubleshooting network issues and checking your IP settings.<sup>

<img width="976" height="508" alt="Screenshot 2026-02-03 222043" src="https://github.com/user-attachments/assets/f66191e7-cfe6-4d83-ab88-b737d1b8fd4b" />

### 2. View Detailed Network Info
```ipconfig /all```

<sup>Provides detailed information for all network adapters, including MAC addresses, DNS servers, DHCP status, and lease details. Use this for in-depth network diagnostics.<sup>

<img width="975" height="506" alt="Screenshot 2026-02-03 222420" src="https://github.com/user-attachments/assets/786f8dfd-786a-43b5-b567-defd0f58cfb5" />

### 3. Release the IP Address
```ipconfig /release```

<sup>Disconnects your computer from the network by releasing its current IP address. Often used before renewing the IP or troubleshooting DHCP issues.<sup>

<img width="1210" height="739" alt="Screenshot 2026-02-03 223606" src="https://github.com/user-attachments/assets/2585b5e4-e453-4f34-b810-c447bad627a6" />

### 4. Renew the IP Address
```ipconfig /renew```

<sup>Requests a new IP address from the DHCP server. Use this after releasing an IP or if your connection needs refreshing.<sup>

<img width="1210" height="739" alt="Screenshot 2026-02-03 224359" src="https://github.com/user-attachments/assets/135cb6af-4231-442c-8994-522750aa55ef" />

### 5. Flush the DNS Cache
```ipconfig /flushdns```

<sup>Clears the DNS resolver cache on your computer. This is useful if you’re having trouble with outdated or incorrect DNS entries, such as when a website isn’t loading correctly.<sup>

<img width="974" height="508" alt="Screenshot 2026-02-03 224919" src="https://github.com/user-attachments/assets/682b72ed-2bd8-412f-9be3-9bceba044967" />

# Tool: `nslookup`
The ```nslookup``` command is a tool used to query DNS records. It helps resolve domain names to IP addresses and vice versa, making it useful for troubleshooting DNS issues.

### 1. nslookup google.com
Ask your computer’s default DNS server to find the IP address for google.com

```nslookup google.com```

<img width="975" height="508" alt="Screenshot 2026-02-03 230400" src="https://github.com/user-attachments/assets/213b2268-2f2c-4f79-89c8-08b205710d49" />

The results will show:
* Your current DNS server – the server your computer is using to resolve domain names.
* The IP address of google.com – the addresses that the DNS server returns for the domain.

### 2. nslookup google.com 8.8.8.8
Run the same query, but this time use Google’s public DNS server (8.8.8.8) instead of your default DNS. This lets you see what IP address Google’s DNS returns directly.

```nslookup google.com 8.8.8.8.```

<img width="974" height="508" alt="Screenshot 2026-02-03 231252" src="https://github.com/user-attachments/assets/cfce2dbb-c266-49e6-9a72-941d3b0ef3d4" />

This is useful for:
* Verifying whether your DNS server returns different results than other servers.
* Checking for DNS-related issues on your network. 

# Tools: `netstat`
The ```netstat``` command displays active network connections, listening ports, routing tables, interface statistics, and more. It’s useful for diagnosing network problems or monitoring ongoing connections.

## Common Syntax
```netstat [options]```

## Commonly used netstat commands

### 1. netstat -a
Displays all active network connections and listening ports, helping you see which applications are communicating over the network.

```netstat -a```

<img width="650" height="734" alt="Screenshot 2026-02-03 232303" src="https://github.com/user-attachments/assets/014edb19-75cd-4217-8a10-ac9632484b7f" />

### 2. netstat -n
Displays active connections and listening ports using numerical IP addresses and port numbers, rather than resolving them to host or domain names.

```netstat -n```

<img width="974" height="520" alt="Screenshot 2026-02-03 232654" src="https://github.com/user-attachments/assets/ed6e9b14-7827-4b35-a1df-c726e495bb8f" />

### 3. netstat -o
Shows active connections along with the associated Process IDs (PIDs), helping you identify which programs are using each connection.

```netstat -o```

<img width="976" height="509" alt="Screenshot 2026-02-03 233018" src="https://github.com/user-attachments/assets/e277f410-9518-4cd4-89f8-9f28600ab285" />

### 4. netstat -an
Combines -a and -n to show all active connections and listening ports using raw IP addresses and port numbers.

```netstat -an```

<img width="736" height="897" alt="Screenshot 2026-02-03 233328" src="https://github.com/user-attachments/assets/315d5637-d91f-42cb-9a56-139234c24592" />

### 5. netstat -b
Displays which executable (program) created each connection or listening port, helping identify the source of network activity. Requires administrator privileges to run.

```netstat -b```

<img width="1429" height="726" alt="Screenshot 2026-02-03 233933" src="https://github.com/user-attachments/assets/138d12da-85c8-4cbf-bc80-829a526814e8" />

# This lab was created for personal learning and to demonstrate IT support skills as part of a portfolio project.


