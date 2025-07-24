# Virtual Firewall Implementation 

**Objective:**  To enhance the lab environment with a virtual firewall for traffic inspection and segmentation.

**Activites**
- Create a virtual pfSense or OPNsense appliance
**Configure:**
- WAN and LAN interfaces
- NAT, DHCP, and DNS as needed
- Basic firewall rules (e.g., port filtering)
-  Connect the Kali and Windows machines to route traffic through the firewall
- Test filtering and logging functionality; document configuration steps and output

**Tools used for this cybersecurity lab setup**

| Operations  | Tools |
| ------------| -------|
| Hypervisor | Virtual Box |
| Operating Systems | Kali Linux, Windows |
|Virtual Firewall | PFsense |

### Overview of pfSense

**pfSense**is an open-source firewall and router operating system built on FreeBSD. It provides enterprise-grade network security and management features, all accessible through a
user-friendly web interface. It can be used by individuals, businesses, schools, and data centers for building reliable and secure network infrastructures.

## Process 

I will provide a work-through of how I configure and use pfSense as a virtual firewall
to restrict certain traffic and operations, such as visiting certain websites like altschoolafica.com and youtube.com, and stop pinging from the Google DNS server: 8.8.8.8
on my virtual networks, which consisted of two virtual machines: Kali Linux and Windows 10

### Installation of pfSense
<img width="1366" height="721" alt="pfsense install" src="https://github.com/user-attachments/assets/ae74942d-5191-43fd-8bfa-cc028b098ac1" />
This snippet above shows the installation process of the pfSense virtual appliance on VirtualB

### Installation showing the configuration of the LAN and WAN interfaces
<img width="711" height="472" alt="Wan and lan" src="https://github.com/user-attachments/assets/ac33fd5b-d90e-45d0-891a-23cf00a17213" />

### pfSense Start up Interface login
<img width="1366" height="701" alt="PFsense interface" src="https://github.com/user-attachments/assets/042677da-f39e-4d80-8dcf-d359d82bab65" />
This snippet shows the start-up page on the GUI of pfSense when it was logged in on the
Windows browser through the IP address:**192.168.1.1**, which is the IP address of the pfSense
which acted as the default gateway for both VMs in the virtual environment, and with a default login with username: **admin** and password: **pfsense**, I was able to access the pfSense to access the GUI and make some default configurations that are referenced below

<img width="1366" height="704" alt="pfsense dashboard " src="https://github.com/user-attachments/assets/b036f02f-0bb3-4aeb-9dc9-d350809cf0ce" />
<img width="1364" height="663" alt="pfsense hostname and DNS change" src="https://github.com/user-attachments/assets/1afb1c36-9683-48f8-8905-c8a4d99bc017" />
I changed the hostname and primary DNS server on the pfSense appliance
<img width="1163" height="228" alt="ipv4 static" src="https://github.com/user-attachments/assets/22ef9a32-fc2e-4793-9cd4-8147839c296f" />

 **Snippnet shows the static IPv4 configuration of the firewall**
<img width="1163" height="228" alt="ipv4 static" src="https://github.com/user-attachments/assets/1d55e7ad-20b3-4dcd-a08c-5723d192774b" />

 **Snippet shows the configuration of the time server**
 <img width="1358" height="663" alt="pfsense ntp capture" src="https://github.com/user-attachments/assets/38d9ebe3-ed53-4cd7-a61e-3b9d70a2837f" />

### Interface Assignments 
<img width="1271" height="427" alt="interface assignment" src="https://github.com/user-attachments/assets/5f3fd2b2-a550-43e7-a6c6-fbe6f1fdacac" />
<img width="1076" height="664" alt="Lan interface" src="https://github.com/user-attachments/assets/4d032658-50bc-4e95-8771-fe53909cffe8" />
<img width="1360" height="653" alt="Wan interface" src="https://github.com/user-attachments/assets/188a4485-7ad9-4e47-883a-3a3aecae029a" />
Snippnets shows the interface assignment on the pfSense, showing its WAN and LAN interfaces, and which network ports they are on the interface

### Firewall Rules to block some websites and operations
<img width="1366" height="722" alt="Final update on firewall" src="https://github.com/user-attachments/assets/7c07b509-29bc-40dd-bf0d-c9263a64950c" />
To simulate the functionality of the firewall, I decided to set up some rules in the Firewall section of the GUI and configure the firewall rules on the LAN interface, which stated the following:
1. **Blocking the Whole 192.168.1.0/24 network from accessing the YouTube website**
   
- *Before the configuration of Firewall rules, hosts were able to access the YouTube website*
<img width="1357" height="718" alt="youtube_DSA_Cybersecurity" src="https://github.com/user-attachments/assets/5172a7d5-05f4-489d-bda8-15a6de54fd4a" />

- *After configuring the Firewall rules applied, the hosts were unable to access the YouTube website*
  <img width="1365" height="731" alt="youtube blocked" src="https://github.com/user-attachments/assets/3808c187-ae47-4a1b-910a-c958d4bc87ab" />
  
2. **Blocking the Kali Linux host from accessing the altschoolafica.com website**
   
 - *Kali is unable to access the altschoolafica page*
    <img width="1366" height="722" alt="altschoolblock" src="https://github.com/user-attachments/assets/43ac2051-ac7e-4a67-987f-1f5a3a299460" />
 - *Other websites being able to be accessed by Kali*
   <img width="1365" height="720" alt="other websites allowed" src="https://github.com/user-attachments/assets/456d3207-2f10-489b-9015-5d8f0e536170" />
3.  **Blocking the entire LAN network from being able to ping the Google DNS server**
   <img width="1363" height="722" alt="windows ping to 8 8 8 8 fail" src="https://github.com/user-attachments/assets/da5b8052-5733-4abe-b50a-ba903f69d123" />
   <img width="1365" height="724" alt="kali failed to 8 8 8 8" src="https://github.com/user-attachments/assets/6c761759-ac0e-47b2-b13b-dc8ea6e36dc0" />

### Firewall Logs

<img width="1363" height="719" alt="firewall logs" src="https://github.com/user-attachments/assets/ca5d68c6-0da0-4da4-8931-e4dc143b1e93" />
This snippet  shows the firewall logs captured on the firewall, giving a view of the functionality of the firewall rules set up

## Conclusion / Lessons Learnt 
I explored the capabilities and functionality of the firewall in blocking and filtering traffic, which opened me up to an understanding of traffic engineering and security controls, and how important it is in network security and ensuring that hosts are safe on the network. Although not captured here, I learnt  about the use of pfBlockerNG to easily block certain websites and domain.






  
 




