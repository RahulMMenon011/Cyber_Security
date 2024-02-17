## LAN Based Insider Attack

Making use of Ettercap tool to perform ARP Cache Poisoning and ICMP Redirect based attacks in a LAN environment:

### 1. ARP Spoofing
>ARP (Address Resolution Protocol) cache poisoning is a technique used by attackers to intercept network traffic between two hosts on a local network. In the context of ettercap, a popular network sniffing and MITM (Man-in-the-Middle) tool, the ARP cache poisoning plugin is used to perform this attack. When the ARP cache poisoning plugin is enabled in ettercap, it sends fake ARP messages to the hosts on the local network, which causes them to update their ARP cache with a fake MAC address for a particular IP address. This allows the attacker to intercept network traffic between two hosts on the local network by redirecting the traffic to their own machine. For this Attack we have to consider 2 system VM

### Familiarization with tool

![image](https://github.com/Nifalnasar/Cyber-Security-Lab/assets/141356053/491abb70-d5fe-4240-9677-c4a01c144c15)

So here we set the interface on which have to start sniffing and related attacks. Then we start sniffing on the interface.

## ARP SPOOFING
ARP spoofing is the process of linking an attacker’s MAC address with the IP address of a legitimate user on a local area network using fake ARP messages. As a result, data sent by the user to the host IP address is instead transmitted to the attacker.

### PERFORMING THE ATTACK
First we discover all the hosts and choose the target on which we want to perform ARP spoofing attack.

![Screenshot 2024-01-29 224055](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/26ab2b36-e589-437f-9097-b0852ce46fb9)

To find the Victim gateway.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/fdd0dc28-13c7-4453-8109-45c644e98856)

So here the target is 192.168.21.128 and the target gateway is 192.168.21.2

Then we perform the ARP poisoning attack

![Screenshot 2024-01-29 224141](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/7ddb166e-8101-4d74-8337-7fb50ce0098c)

Now we can see that we are able to see the traffic. So our attack is successful.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/c604e1d0-a7de-429c-a9c0-5413656e552f)

When analyze the Splunk reports we can see that http request was successful but there was no sign of showing ARP spoof.

### 2. Performing DOS Attack using ARP Cache Poisoning

What is DOS Attack?

>The DoS (Denial of Service) attack plugin in ettercap is used to flood a target system or network with an overwhelming amount of traffic to disrupt the normal functioning of the system or network. The purpose of this attack is to make the target system or network unavailable to legitimate users. The DoS attack plugin in ettercap works by generating a large amount of network traffic towards the target. The legitimate traffic may include HTTP requests, DNS queries, or other network requests.

Steps for the attack

* Scan for hosts
* Add hosts as target (only the target ip & not the gateway ip)
* Start arp poisoning the victim.
* Then search for dos_attack plugin and start it

  The DoS (Denial of Service) attack plugin in ettercap is used to overload a target system or network with traffic in order to prevent the system or network from operating normally. This attack aims to prevent authorised users from accessing the target system or network. The way the DoS attack plugin in ettercap operates is by flooding the target with a lot of network traffic. Requests sent over the network, such as HTTP or DNS inquiries, might be considered genuine traffic.

As like the previous steps,

Scan for hosts

Add hosts as target (only the target ip, gateway ip not required)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/91acc4f9-41cf-4019-9712-e9665d77e501)

Start arp poisoning the victim. 

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/125d2ef5-8973-4120-a252-e908c7d74028)

And now run the dos_attack plugin.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/00fa2337-71a5-4bc0-98f7-37453c9e5625)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/1a8b8886-35df-4d05-b67e-f5dd8ca27484)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/52f42ff9-535a-4349-aa0a-1beeb609c9f1)

The victim becomes slow as soon as we enable the plugin since the target IP starts sending the victim a large number of packets. Therefore, the victim's web searches just never stop loading.

![WhatsApp Image 2024-02-17 at 21 50 47_878e4305](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/2f6d2d2d-4a8b-4a8a-b286-0a7b512d2791)

