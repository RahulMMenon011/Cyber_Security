#### a) Explain the subnet and use the NMAP Command to scan the services for the whole subnet.

>A segment of a network that has been divided into smaller networks, each having a distinct IP address range, is known as a subnet. Enhancing network performance, security, and management is the goal of this.
Network managers can create smaller subnetworks within a larger network by using subnetting, which might be used to organize devices with comparable features or security needs.

`victim`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/be1059ae-0cd4-4861-b89b-036c2834859d)

`Attacker`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/76f113cf-d879-4d48-9bc3-517ea4d73416)

command used is `nmap  -sV 192.168.26.132/24`

#### b) What is a firewall, and mention its types. Use the NMAP command to detect that a firewall protects the host.

>A firewall is a network security device that monitors incoming and outgoing network traffic and decides whether to allow or block specific traffic based on a defined set of security rules.

Types of Firewalls

* Packet filtering firewall 
* Stateful inspection firewall
* Application-level gateway firewall
* Next-generationfirewall
* Host-based firewall

`Victim`


![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/efcef83f-9bd7-429e-b645-59dedb433e17)

`Attacker`

Command

`nmap -sS <ip>`

![Screenshot 2024-02-16 233059](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/7511b8a3-0a8d-46d5-ba48-091406a47977)

#### c) Use the NMAP command to scan a network and determine which devices are running

Command

`nmap -sn <ip>/<CIDR>`

`Attacker`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/715da44a-c7b6-4421-8588-7aa83fa7bd1a)

#### d) What are vertical and horizontal scanning?

* `Vertical scanning`also known as service scanning, involves scanning a single host for all the openports and services that are running on it. This approach allows for a detailed analysis of the individualhost, including the versions of services running, operating system, and other relevant information.
* `Horizontal scanning`also known as port scanning, involves scanning multiple hosts for a specific openport or set of ports. This approach allows for a quick overview of the network or hosts that may have aspecific service or vulnerability present.

#### e) Use the NMAP command to scan multiple hosts

`Attacker`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/4f524f4c-deb5-4056-8c60-e9262033f8d5)

#### f) Use NMAP commands to export the output in XML format.

we use the `-oX` flag

Command used here

`nmap -sV <ip> -oX result.xml`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/d5dd8689-80c4-49bc-b7b1-9eb9ed24679c)

#### g) Use the NMAP command to get OS information about a host

Command 

`nmap -O <ip>`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/67f64932-505a-4644-a8a1-968a74bfb6b4)

#### h) Explain ping sweeping and Perform ping sweeping using Nmap
`Ping Sweep` is a network reconnaissance technique used to determine which IP addresses are alive and responsive on a network.
It involves sending a series of ICMP echo request messages, also known as pings, to a range of IP
addresses, usually in a sequential order, to identify which ones are available and can be reached.
Ping sweeping is often used by network administrators to identify active hosts on a network and to map
the network

Nmap command to perform ping sweep - `nmap -sn <network address>/<CIDR`

sn - allows to perform a ping scan on the target

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/02c76938-f70e-4e7c-9b7a-412aebc0858f)

#### 1.What is a web application firewall? How do you use Nmap to detect a WAF? Perform WAF fingerprintdetection using NMAP.

a) A web application firewall (WAF) is a firewall that monitors, filters and blocks data packets as theytravel to and from a website or web application.

b) A WAF can be either network-based, host-based or cloud-based and is often deployed through areverse proxy and placed in front of one or more websites or applications.

c) Running as a network appliance, server plugin or cloud service, the WAF inspects each packet anduses a rule base to analyze Layer 7 web application logic and filter out potentially harmful traffic that canfacilitate web exploits.

Command  `nmap --script http-waf-detect`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/dae1f7f3-2935-4a52-a96c-f4308e0310cc)

#### 2.What is EXIF data? Try to find EXIF data of images on a website using NMAP NSE.

EXIF DATA It is a metadata that is embedded within image files, such as JPEGs, TIFFs, and RAW files. Thisdata includes information about the camera settings used to take the picture, as well as informationabout the date, time, and location of the image Exif data can also include information about the camera'smake and model, the lens used, and the exposure settings, such as shutter speed, aperture, and ISO.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/f31297a0-d80f-44ed-83ff-1318705253d5)

#### 3.Use NMAP NSE to find all subdomains of the website.

All the nse scripts are loacated in `/usr/share/nmap/scripts`

command used `nmap --script dns-brute.nse www.google.com`

The dns-brute script built into Nmap is designed to enumerate subdomains and their correspondingserver IP addresses.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/a76d74ea-f500-4117-a539-1b7677d54463)

#### 4.Perform a vulnerability scan on the target host using NMAP NSE.

command used `nmap -sV --script=vuln <target ip>`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/58f480db-ce0b-4c27-9284-c991719c45eb)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/c6b4ada8-5d7b-456d-bbc5-b629c1f5bf3d)

