## TOOL USED HERE
### ETTERCAP
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

## DNS SPOOFING
In a DNS spoofing attack, the attacker exploits vulnerabilities in the DNS resolution process to provide false information to a DNS resolver, which is responsible for translating domain names into IP addresses. The goal of DNS spoofing is to redirect users to a fraudulent website or to intercept sensitive information.

### CAUSE OF ATTACK
1. Weaknesses in DNS Protocol: The DNS protocol itself can have vulnerabilities that attackers exploit. For example, if the DNS messages are not adequately protected, an attacker might inject false DNS responses into the system.
2. Lack of DNS Security Extensions (DNSSEC): DNSSEC is a suite of extensions to DNS designed to add an additional layer of security by signing DNS data with cryptographic signatures. If DNSSEC is not implemented or configured incorrectly, it can leave the DNS system susceptible to spoofing attacks.

### PREVENTION
To prevent DNS spoofing, organizations and individuals should implement several key measures. Firstly, deploy DNS Security Extensions (DNSSEC) to authenticate and verify the integrity of DNS data through cryptographic signatures. Additionally, configure DNS resolvers to limit open access, ensuring they respond only to authoritative queries.

### PERFORMING THE ATTACK

>So to perform the attack we will be using the DNS spoof plugin that is available in Ettercap that we previously used.
We also have to modify /etc/ettercap/etter.conf file and
/etc/ettercap/etter.dns to change to perform the dns spoofing attack

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/a4711a59-9fc6-4d8a-8732-2e7efeab62b5)

![Screenshot 2024-01-29 220558](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/22bdb775-ad8d-43d4-a6f3-2796e4a24c8c)

![Screenshot 2024-01-29 220758](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/d60408fa-d2ae-4d36-8a27-30f1bf15b3c6)

>we will turn on the redirection and which website we spoof the DNS.
So first start the dns spoofing using the plugin in the Ettercap plugins.

![Screenshot 2024-01-29 221111](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/073cf52b-95dd-487a-b74a-9e64d0b962e2)

>So we can see that we have dns_spoof plugin. After starting the dns spoofing we
will use
Arp poisoning again to make the attack successful.

![Screenshot 2024-01-29 221023](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/a24513cc-fc86-45a2-9fce-51d0714fd770)

>We will add all the gate way as the first target and others host as the second target.
Now if we try to navigate to the specified website it should goto Apache server running
on the attacker machine.

![Screenshot 2024-01-29 221355](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/b152ceae-2fa2-428d-a8aa-14d7282f634a)

So the attack is successful.

![Screenshot 2024-01-29 222729](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/955a58e2-bdaa-4baa-87fc-7d9596110972)








