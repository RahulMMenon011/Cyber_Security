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

>nmap -sS <ip>

![Screenshot 2024-02-16 233059](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/7511b8a3-0a8d-46d5-ba48-091406a47977)

#### c) Use the NMAP command to scan a network and determine which devices are running

Command

>nmap -sn <ip>/<CIDR>

`Attacker`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/715da44a-c7b6-4421-8588-7aa83fa7bd1a)

#### d) What are vertical and horizontal scanning?

* `Vertical scanning`also known as service scanning, involves scanning a single host for all the openports and services that are running on it. This approach allows for a detailed analysis of the individualhost, including the versions of services running, operating system, and other relevant information.
* `Horizontal scanning`also known as port scanning, involves scanning multiple hosts for a specific openport or set of ports. This approach allows for a quick overview of the network or hosts that may have aspecific service or vulnerability present.

#### e) Use the NMAP command to scan multiple hosts

`Attacker`

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/4f524f4c-deb5-4056-8c60-e9262033f8d5)

#### f) Use NMAP commands to export the output in XML format.

we use the -oX flag