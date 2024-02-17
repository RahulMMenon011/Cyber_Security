### ARP Spoofing
Ettercap is a comprehensive, open-source network security tool used for analyzing, monitoring, and manipulating network traffic in a computer network. Originally developed for Unix-like operating systems, it has since been adapted for Windows as well. Ettercap operates as a man-in-the-middle (MITM) attack tool, allowing cybersecurity professionals, penetration testers, and ethical hackers to inspect and modify data as it passes through a network.

### Familiarization with tool

![image](https://github.com/Nifalnasar/Cyber-Security-Lab/assets/141356053/491abb70-d5fe-4240-9677-c4a01c144c15)

So here we set the interface on which have to start sniffing and related attacks. Then we start sniffing on the interface.

## ARP SPOOFING
ARP spoofing is the process of linking an attacker’s MAC address with the IP address of a legitimate user on a local area network using fake ARP messages. As a result, data sent by the user to the host IP address is instead transmitted to the attacker.

### CAUSE OF ATTACK
The main cause of ARP spoofing attacks is the fundamental trust issue within the Address Resolution Protocol (ARP) itself. ARP is a network communication protocol that helps devices translate IP addresses, which are easy for humans to remember, into MAC addresses, which are the unique identifiers used by network devices.

### PREVENTION
We can prevent it by implementing the IDS(Intrusion detection system).
Using the Arp-spoof detecting software.

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
