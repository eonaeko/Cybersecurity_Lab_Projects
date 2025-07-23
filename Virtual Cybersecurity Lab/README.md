
# Project 1: Virtual Cybersecurity Lab Setup 

**Objective:** To simulate a secure, real-world environment for offensive and defensive security testing through Virtual Machines

### Tools Used for this virtual cybersecurity lab setup

| Operations    |  Tools    |
|----------------|----------------- |
| Hypervisor    | VirtualBox  |
| Operating Systems:|  Kali Linux, Windows |
| Service Enumeration |NMAP, Shared Folders |

### Activities

- Install a Type 2 Hypervisor
- Create and configure two  Virtual Machines(VMs)
- Establishing internal virtual networking between VMs
- Verify Connectivity via Ping tests, Shared directories, and Service Enumeration

### Procedures
- Installation of Type 2 Hypervisor  
- Ensuring Virtual internetworking between VMs
- Verification of internal networking via ping tests
- Shared Files and Nmap Service Enumeration 

### Installation of Type 2 Hypervisor

This process began with selecting and configuring the Hypervisor to be used. I would settle into using the VirtualBox Platform for this lab, where the two VMs  were virtualized and allocated operational resources such as RAM, Storage, processors, and Network Interfaces, then also User profiles and passwords were set up  afterwards.

### Ensuring Internal Virtual Networking between VMs 

This is where the major tasks started, as even though the VMs were on the same hypervisor, they were separate devices that could not communicate unless enabled by putting them on the network, and the following were stated to achieve their communication

- **Changing Network Adapter Settings**
 I  configured the network adapter for both VMs on VirtualBox, changing it from NAT to internal Network, making to logically be on the same network
<img width="852" height="538" alt="kali on same network as windows" src="https://github.com/user-attachments/assets/337d4b28-c998-4cf9-8079-94441fad6987" />

<img width="836" height="490" alt="windows on same network as kali" src="https://github.com/user-attachments/assets/12b82dba-b1f7-4118-bae0-a2d8e2086158" />

- **Configuration of private IP addresses for both VMs**
  
  To make them communicate, a vital element was needed, and that is IP addresses, so I configured both the Kali VMs and Windows VMs with the IP addresses  192.168.1.10 and 192.168.1.20 on the /24 subnets, respectively
  
<img width="820" height="620" alt="ipaddr config on kali" src="https://github.com/user-attachments/assets/52472a9a-f8fc-4470-b0fc-1e8c363e0830" />

<img width="1237" height="718" alt="windows ip addr configuration" src="https://github.com/user-attachments/assets/c09a69b1-ed26-4af0-8ad7-d3996593f684" />

- **Verification of Internal communication via Ping tests**
  
  I confirm their internal communication through ping tests carried out, but at first, my pings into Windows would fail, so I researched and I discovered that Windows had its Windows Defender to block pings (which I considered a good feature), I reconfigured the defender to accept ICMP messages
  
  <img width="883" height="647" alt="window firewall inbound rule change" src="https://github.com/user-attachments/assets/4904f369-abbb-4e22-ac04-ad8a5cb473d9" />
  
<img width="1080" height="668" alt="final successful ping from kali to windows" src="https://github.com/user-attachments/assets/f70815c9-0866-42e2-9c70-1e689ed3093b" />

### Service Enumeration by Shared Files and searching for open ports via Nmap 
After connectivity was established between the two VMs, I created a folder on the Windows VM named WannaShare. I configured it to be a shared folder accessible on the network, while I accessed it in Kali VM 

<img width="1350" height="747" alt="Attempt to share files " src="https://github.com/user-attachments/assets/2f54bc73-5a4f-4247-8527-1fcc3760315a" />

I further scanned for open ports and vulnerable services through NMAP

<img width="702" height="251" alt="first nmap capture" src="https://github.com/user-attachments/assets/87d4454a-6b6c-4646-9e78-b54f8e4dfc69" />

<img width="682" height="256" alt="2nd nmap capture" src="https://github.com/user-attachments/assets/807a1314-22b0-483d-9bb7-b346d66edf34" />

<img width="773" height="272" alt="emmanuel" src="https://github.com/user-attachments/assets/647abbcd-9dd9-4399-a584-fcc7acc6d9d5" />

### Conclusion And Major Takeaways
This lab helped me get comfortable with setting up my Virtual Machines, which is important for other labs I will work on, understanding how virtualization was carried out, and I also got comfortable with using the Linux OS through the terminal, as I used a handful of terminal commands. I also got some experience with working a firewall, NMAP, and Vulnerability Assessment. It equipped me with the soft skills of actively researching.

 [View my report](https://drive.google.com/file/d/1N6Gfk3DX6lGsq99e39k0ZDkBkv5zOVbD/view?usp=drive_link)





  





  


