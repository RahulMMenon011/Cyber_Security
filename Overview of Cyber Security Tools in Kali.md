# Kali Tools

## Information Gathering tools

### 1. NMap
High Level Summary
> Nmap (Network Mapper) is a powerful and widely used open-source tool for network exploration and security auditing.Nmap operates by sending packets to the target network and analyzing the responses to gather information about hosts, open ports, services running on those ports, and other details.

Recomendations
>This Tool is majorly used in port scanning and security audititng

Methodologies
>Its free utility tool available in kali linux

`nmap -sn 10.0.2.1`

The nmap -sn command is used for ping sweep scanning in the powerful network scanner Nmap.It tells Nmap to perform a quick scan to discover live hosts on a network without attempting to connect to any ports or services.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/b7eb23ee-c093-4c84-b341-909360626cad)

`nmap 10.0.2.1`

The nmap command is used for understanding the state and service of the ports under a specific ip adress.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/8511d120-08b8-4d50-97df-4a17a2a2b001)

`nmap -sV 10.0.2.1`

The nmap -sV command is used to perform service version detection during a port scan.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/66149f23-d881-4825-99e3-e19322dc8e1e)

`sudo nmap -O 10.0.2.1`
 
The nmap -O command is used for operating system detection during a network scan.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/5b0652b7-8cf8-48f6-98f3-3a2bccdf3320)

`sudo nmap amrita.edu -Pn -F --osscan-guess`

Here the -Pn command skips the host discovery, -F is for fast mode and --osscan-guess is for agressive os detection.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/f9d32d84-5f5e-4cad-8e31-ca345fe9efe0)

Service Enumeration
> N.A.

### 2. Netcat

High Level Summary
>Netcat, often abbreviated as "nc," is a versatile and powerful command-line networking tool used for various networking tasks it provides a simple yet effective way to read and write data across network connections using TCP or UDP protocols.

Recommendations
>Security Considerations: Be aware of the security implications when using Netcat, especially when dealing with remote connections.

>Be Cautious with Backdoors: While Netcat can be used for legitimate purposes, creating backdoors with it for unauthorized access is a security risk

>Firewall Settings: Check and adjust firewall settings as needed. Some operations with Netcat may require specific ports to be open, and modifying firewall rules may be necessary.

Methodologies
>Netcat is used for port scanning, file transfer, remote shell access, chat servers, port forwarding, banner grabbing, proxying.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/01608161-21f0-4c67-a77f-57b1d7a35286)

I was able to chat between two diffrent terminals using the loopback address in the same machine using netcat.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/ad23f6f6-0d73-494e-ae16-78d1673abbdf)

Different functions available in netcat.

Service Enumeration
> Use Netcat to connect to specific ports on a target machine and gather information about the services running on those ports.

>Example:` nc -v target_host target_port`

### 3. DMitry

High Level Summary
>DMitry is an open-source command-line tool designed for intelligence gathering during the reconnaissance phase of penetration testing or network assessments. It aims to collect as much information as possible about a target domain, including subdomains, IP addresses, network infrastructure, and more.

Recommendations
>Information Gathering Tool through which we can get all basic required information of it

Methodologies
>DMitry (Deepmagic Information Gathering Tool) is a reconnaissance tool designed for gathering intelligence about a target during network assessments or penetration testing.

`dmitry -i 8.8.8.8`

In this command the 'i' flag perform a whois lookup on the IP address of a host.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/e014ee83-0577-4844-ae49-c51b19181653)
![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/931140e3-1f96-4570-bc22-7c702aee2073)

`dmitry -w google.com`

Here the 'w' flag perform a whois lookup on the domain name of a host

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/75f02e69-ba1c-4fae-9468-33788e96c5a4)

`dmitry -s google.com`

Here the 's' flag Perform a search for possible subdomains

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/4d9179e5-6916-4646-9fb8-8e4a75dafed3)

`dmitry -e google.com`

Here the 'e' flag perform a search for possible email addresses

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/2d07fd18-e8de-45f6-9450-743b51f60550)

Service Enumeration
>By this we can get to know which all are live application running on the system

## Vulnerability Analysis Tools

### 1. Legion

High Level Summary
>Legion tool is a super-extensible and semi-automated network penetration testing framework.GUI with panels and a long list of options that allow pentesters to quickly find and exploit attack vectors on hosts. It has the feature of real-time auto-saving of project results and tasks. 

Recommendations
>Automatic detection of CVEs (Common Vulnerabilities and Exposures) and CPEs (Common Platform Enumeration).

Methedologies
>Its free utility tool available in kali linux which is GUI Based and also we can customize it.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/7475aafa-d75b-428c-a913-f453143e58c9)

we can use the ip address or url check the Vulnerability Analysis

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/beb20536-6259-4ac4-a04b-1b5d755214da)

Several tools will be used for information gathering and find out the cVe(Common Vulnerability and exposure of the url or ip address)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/d17402d6-6c8a-463c-a602-28b3f9576280)

Host, Port and protocol of the url

Service Enumeration
>N.A.

Penetration
>We can get the information of open ports of host and many more options like auto detecting CVE

###  2. Lynis

High Level Summary
>Lynis is a widely used open-source security auditing tool for Unix and Linux-based systems. It is designed to perform system and security audits to identify potential vulnerabilities and configuration issues.

Recommendations
>Regularly run Lynis, address identified vulnerabilities and implement recommended hardening measures to ensure ongoing security compliance on your Linux system.

Methodologies
>Analyze the pentest report to identify high-priority vulnerabilities and misconfigurations flagged by the testers.

`lynis audit system --forensics --verbose`

Here the 'forensics' flag perform forensics on a running or mounted system and the 'verbose' flag gives a detailed output on screen.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/3bbefe67-49cf-42b9-9d1b-a4b0d1e08909)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/5019b0d9-5436-4641-8698-f1dcdf9eb09a)

Lynis checks the system for security-related information, such as user accounts, system configurations, file permissions, and network settings. It identifies potential security risks and provides recommendations for improvement.

Service Enumaration
>N.A.

### 3. Nikito

High Level Summary
>Nikto is an open-source web server scanner which performs comprehensive tests against web servers for multiple items.Nikto can check for server configuration items such as the presence of multiple index files, HTTP server options, and will attempt to identify installed web servers and software.

Recommendations
>This Tool is majorly used in port scanning and security audititng

Methodologies
>Its free utility tool available in kali linux

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/9882804c-e156-49ae-adf2-51c79e467731)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/473c8f14-4c4b-4130-b91f-3324260cced0)

Discovers Hosts, Scanning order and port specification, The detection of service or version and operating system, Scanning Ports.

Service Enumeration
>Nikto performs service enumeration by scanning web servers to identify open ports, extract banners for service identification, and assess configurations, aiding in the discovery of potential vulnerabilities and security risks.

Penetration
>We can get the information of open ports in that particular domain

## Web Application Analysis Tools

### 1. Burp Suite

High-Level Summary
>Burp Suite is a cybersecurity tool designed for web application security testing. It is help in finds bugs in the websites and is gui based tool.

Recommendations
>It is used to perform security testing in web application and also finding exploits in that surface.

Methodologies

* Proxy: Burp Suite acts as a proxy server between the user's browser and the target web application. It allows the user to intercept and modify the communication between the two, enabling the analysis and manipulation of HTTP requests and responses.
* Intruder: Burp Intruder is a powerful tool for performing automated attacks against web applications. It can be used to test the susceptibility of an application to different types of attacks, such as brute force and parameter tampering.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/33924c03-2742-4497-addf-f5b4b4c00693)

Using the proxy option with intercept turned on, we can intercept the http get request from the user and modify the request according to our need.

Service Enumeration
>N.A.

### 2. WPScan-(WordPress Scan)

High-Level Summary
>WordPress is known to have many flaws and vulnerabilities. WPScan will scan the WordPress website for its version, plugins, users and also has an in-built password cracker

Recommendations
>This is used specifically for Websites hosted on WordPress.

Methodologies
>Checking the version of WordPress used and associated vulnerabilities for that version.Checks for database dumps that may be openly accessible.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/d921567c-52d8-4db3-ade8-b53752a61e99)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/fbf41c67-b54b-4670-b219-10dfd2669354)


Service Enumeration
>N.A.

### 3. WhatWeb

High-Level Summary
>WhatWeb identifies websites. It recognises web technologies including content management systems (CMS), blogging platforms, statistic/analytics packages, JavaScript libraries, web servers, and embedded devices.

Recommendations
>It scans website with aggression level set to 1 -v is for more readablility

Methodologies
>This tool can identify and recognize all the web technologies available on the target website. This tool can identify technologies used by websites such as blogging, content management system, all JavaScript libraries.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/5db3e388-4c4b-4133-a98d-d91a880c0b31)

Service Enumeration
>N.A.

Penetration
>WhatWeb is responsible for grabbing particular information from the target website. Whatweb works as an information-gathering tool and can identify all the email addresses, SQL errors, technology used in the website.

## Database Management Tools

## 1. SqlMap

High-Level Summary
>Sqlmap is a python based tool; therefore it should operate on any system that supports Python. The purpose of sqlmap is to find and take benefit of SQL injection vulnerabilities in web applications.

Recommendations
>It includes a robust detection engine, numerous specialist features for the ultimate penetration tester, and a wide range of switches that span database fingerprinting, data retrieval from databases, access to the underlying file system, and executing commands on the operating system via out-of-band connections.

Methodologies
>When it detects one or more SQL injections on the target host, the user can choose from a number of options, including performing an extensive back-end database management system fingerprint, retrieving DBMS session user and database, enumerating users, password hashes, privileges, databases, dumping entire or user-specific DBMS table/columns, running his own SQL statement, reading particular files on the file system and more.


![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/3e0d95aa-0ff7-4c72-af49-51f3e1cbb859)


Service Enumeration
>N.A.

Penetration
>By giving DBMS credentials, IP address, port, and a database name, it is possible to connect to the database directly without using SQL injection.

## Password Attack Tools

### 1. Medussa

High-Level Summary
>Medusa is a modular, speedy, and parallel, login brute-forcer. It is a very powerful and lightweight tool. Medusa tool is used to brute-force credentials in as many protocols as possible which eventually lead to remote code execution. It currently has over 21 modules, some of which are: PcAnywhere, POP3, CVS, FTP etc.

Recommendations
>N.A.

Methodologies
>It works on bruteforce method

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/bd5310dd-c32b-4b72-ad64-01f9ddef53c8)

Service Enumeration
>N.A.

Penetration
>It uses the wordlist which is available on kali linux and apply brute force method

### 2. Crunch

High-Level Summary
>In order to hack a password, we have to try a lot of passwords to get the right one. When an attacker uses thousands or millions of words or character combinations to crack a password there is no surety that any one of those millions of combinations will work or not

Recommendations
>This collection of a different combination of characters is called a wordlist. And in order to crack a password or a hash, we need to have a good wordlist which could break the password. So to do so we have a tool in Kali Linux called crunch.

Methodologies
>crunch is a wordlist generating tool that comes pre-installed with Kali Linux. It is used to generate custom keywords based on wordlists. It generates a wordlist with permutation and combination. We could use some specific patterns and symbols to generate a wordlist.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/3faa1471-b72d-4cfd-b513-9e2d5915858b)

Service Enumeration
>N.A.

Penetration
>It uses the wordlist which is available on kali linux and apply brute force method

### 3. Hash Finder

High-Level Summary
>As the name is it used to identify the type of hashes that is given as input further based on the hash information we can crack hash using any other tools.

Recommendations
>This collection of a different combination of characters is called a wordlist. And in order to crack a password or a hash, we need to have a good wordlist which could break the password. So to do so we have a tool in Kali Linux called crunch.

Methodologies
>It simply suggests type of hash whether its of MD5 or hash

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/4a0c201f-8db3-404e-ad53-d3cb4f89fd11)

Service Enumeration
>N.A.

Penetration
>N.A

## Wireless attacks Tools

### 1. Wifite

High-Level Summary
>Wifite is a tool to audit WEP or WPA encrypted wireless networks. It uses aircrack-ng, pyrit, reaver, tshark tools to perform the audit.

Recommendations
>This collection of a different combination of characters is called a wordlist. And in order to crack a password or a hash, we need to have a good wordlist which could break the password. So to do so we have a tool in Kali Linux called crunch.

Methodologies
>When cracking the passwords for multiple networks it sorts them based on their signal strength. Packed with a lot of customizing options to improve the effectiveness of the attack. Changes mac address while attacking to make the

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/e0de4b3e-e635-460d-b4e8-e4149b9b521a)

Service Enumeration
>N.A.

Penetration
>N.A

### 2. Revear

High-Level Summary
>Reaver is a package that is a handy and effective tool to implement a brute force attack against Wifi Protected Setup (WPS) registrar PINs to recover WPA/WPA2 passphrases. It is depicted to be a robust and practical attack against WPS, and it has been tested against a wide variety of access points and WPS implementations. In today’s time hacking WPA/WPA2 is exceptionally a tedious job.

Recommendations
>Normal Dictionary attack could take days, and still will not succeed. On average Reaver will take 4-10 hours to recover the target AP’s plain text WPA/WPA2 passphrase, depending on the AP. Generally, it takes around half of this time to guess the correct WPS pin and recover the passphrase.

Methodologies
>First we can scan the available networks with airodump-ng and selected one network and we will take the bssid of that network and we will give the input to the reaver and try to brutteforce the password.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/c4516579-9268-4cce-99da-ad7fc0a259df)

Service Enumeration
>N.A.

Penetration
>N.A

### 3. Bully

High-Level Summary
>Bully is a new implementation of the WPS brute force attack, written in C. It is conceptually identical to other programs, in that it exploits the (now well known) design flaw in the WPS specification. It has several advantages over the original reaver code. These include fewer dependencies, improved memory and cpu performance, correct handling of endianness, and a more robust set of options.

Reccomendations
>none

Methodologies
>Bully can be used by security professionals and network administrators to assess the security of wireless networks. Specifically, Bully is designed to exploit vulnerabilities in the WPS (Wi-Fi Protected Setup) feature commonly found in routers. WPS is intended to simplify the process of connecting devices to a Wi-Fi network, but some implementations have been found to have security flaws that can be exploited.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/490bc202-4ce6-42f6-a92e-b91511efa268)

Service Enumeration
>N.A.

Penetration
>N.A

## Reverse Engineering Tools

### 1. Nasm

High-Level Summary
>NASM stands for Netwide Assembler. It's a popular assembler for the x86 architecture used in many Unix-like operating systems, including Linux.

Recommendations
>This tool Nasm very useful when we have understand the machine level language and what it does.

Methodologies
>NASM take assembly language code, which is a low-level programming language that closely maps to machine code, and convert it into machine code or object code that a computer's processor can understand and execute.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/5c3f78cd-6313-48bf-a2d0-ebcf61fe1b3b)

Service Enumeration
>N.A.

Penetration
>N.A

### 2. Radare2

High-Level Summary
>Radare2 is an open-source framework for reverse engineering and binary analysis. It provides a comprehensive set of tools for examining, analyzing, and understanding binary files.

Recommendations
>Radare2 is used by a diverse group of individuals, including security professionals, researchers, and hobbyists. It is particularly useful for reverse engineers, who rely on tools like r2 to understand and analyze code at a low level. This article will introduce you to radare2 and explore its key features and benefits.

Methodologies
>Disassembling and analyzing code, Debugging with Radare2 is also possible

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/9884b747-2441-4283-acb5-edc331f8cb4b)


Service Enumeration
>N.A.

Penetration
>N.A

## Exploitation tools

### 1. Metasploit

High-Level Summary
>Metasploit is an open-source platform that supports vulnerability research, exploit development, and the creation of custom security tools.It contains many exploits and we can get exploit to many well known vulnerabilities. And it also supports some scanners to.

Recommendations
>None

Methodologies
>Metasploit is a powerful and widely used penetration testing framework that assists security professionals in identifying and exploiting vulnerabilities in computer systems. It provides a set of tools, resources, and exploits to test the security of a network or system

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/2d6896bf-7f11-4847-8cd9-df9d56794048)


Service Enumeration
>N.A.

Penetration
>The penetration testing use of Metasploit revolves around simulating real-world cyber attacks in a controlled environment to identify and address vulnerabilities in computer systems, networks, and applications.

### 2. Searchsploit

High-Level Summary
>SearchSploit is a command-line search tool for Exploit-DB that allows you to take a copy of the Exploit Database with you.

Recommendations
>SearchSploit is very useful for security assessments when you don’t have Internet access because it gives you the power to perform detailed offline searches for exploits in the saved Exploit-DB.

Methodologies
>suppose we are taking the vulnerable machine here i.e 192.168.219.129 we get some info about the services that are running on the port here take port 21 so the service running on the port 21 is vsftpd 2.3.4 if try check for the possible exploit in searchsploit we can get the result.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/2afe9fa3-9b80-4dc4-bb63-31b03bb1018b)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/0b69a10d-68d9-4796-b64c-e4afc47f145a)

Service Enumeration
>N.A.

Penetration
>N.A

## Sniffing and Spoofing tools

### 1. Wireshark

High-Level Summary
>Wireshark is a free and open-source packet analyzer tool used for network troubleshooting, analysis, and communication protocol development and education.

Recommendations
>It captures network traffic from ethernet, Bluetooth, wireless (IEEE.802.11), and frame relay connections, among others, and stores that data for offline analysis.

Methodologies
>This image shows the main page of the wireshark it contains many options for capturing the traffic the we select interface eg eth0 for etherenet we can see that some traffic going through eth0 we can select the interface and start the capture

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/a2eca1b9-5d88-4a76-85be-3608e77c2d16)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/12bb0756-5b29-4148-8f6a-e36ecc11b028)


Service Enumeration
>N.A.

Penetration
>We can filter as per our requirement which we need.

### 2. TcpDump
High-Level Summary
>This program allows you to dump the traffic on a network. tcpdump is able to examine IPv4, ICMPv4, IPv6, ICMPv6, UDP, TCP, SNMP, AFS BGP, RIP, PIM, DVMRP, IGMP, SMB, OSPF, NFS and many other packet types.

Recommendations
>It can be used to print out the headers of packets on a network interface, filter packets that match a certain expression. You can use this tool to track down network problems, to detect attacks or to monitor network activities.

Methodologies
>we use tcpdump command to run tcpdump -i to specify interface here we are using eth0 interface that is ethernet -v increase the verbosity are make the output more readable.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/f391695f-fac7-45e2-9737-b714190b0682)

Service Enumeration
>N.A.

Penetration
>N.A.

### 3. Macchanger
High-Level Summary
>GNU MAC Changer is an utility that makes the maniputation of MAC addresses of network interfaces easier. MAC addresses are unique identifiers on networks, they only need to be unique, they can be changed on most network hardware.

Recommendations
>Kali linux comes pre installed with a tool called macchanger which allows us to change mac address on a temporary basis.

Methodologies
>If you have prior experience with Kali Linux then you would understand that eth0 is the name of the system’s networking interface card or NIC.Always remember to specify the name of the interface whenever working with macchanger. Let us now change into a particular mac address,If you observe the help option then you can see that in order to that we need to use the -m argument.Use the help option well if you want to get proficient in using professional tools.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/28033000-e6de-478e-9bea-7dcaedda89f5)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/82c3d04d-3e37-4426-8273-fa748c022e41)

Service Enumeration
>N.A.

Penetration
>Sometimes to manipulate the mac address we have to change the device Mac Address

## Post Exploitation Tool

### 1. Weevely

High-Level Summary
>Weevely is a stealth PHP web shell that simulate telnet-like connection. It is an essential tool for web application post exploitation, and can be used as stealth backdoor or as a web shell to manage legit web accounts, even free hosted ones.

Recommendations
>At the same time it is a feature-rich network debugging and exploration tool, since it can create almost any kind of connection you would need and has several interesting built-in capabilities.

Methodologies
>suppose when generated and ran the payload in the target machine we got the reverse shell using netcat

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/202f390b-0437-4ef5-abe4-362e48f6ce8a)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/26e9456d-953c-444f-b276-980d82f4fe69)

Service Enumeration
>N.A.

Penetration
>N.A

### 2. Mimikatz

High-Level Summary
>Mimikatz is also capable of assisting in lateral movements and privilege escalations. Attacks like Pass-the-Hash, Pass-the-Ticket, Over-Pass-the-Hash, Kerberoasting etc. can also be achieved with Mimikatz.

Recommendations
>Mimikatz abuses and exploits the Single Sign-On functionality of Windows Authentication that allows the user to authenticate himself only once in order to use various Windows services.

Methodologies
>After a user logs into Windows, a set of credentials is generated and stored in the Local Security Authority Subsystem Service (LSASS) in the memory. As the LSASS is loaded in memory, when invoked mimikatz loads its dynamic link library (dll) into the library from where it can extract the credential hashes and dumps them onto the attacking system, and might even give us cleartext passwords.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/625bf74c-bac1-43cd-a076-65b69d3405bc)

Service Enumeration
>N.A.

Penetration
>N.A

## Social Engineering Tools
### 1. SET(Social Engineering Tool kit)

High-Level Summary
>The Social-Engineer Toolkit (SET) is an open-source Python-driven tool aimed at penetration testing around Social-Engineering.It can be used to perform various social engineering attacks like email phisphing, site phisphing etc.

Recommendations
>The Spear-phishing module allows you to specially craft email messages and send them to your targeted victims with attached FileFormatmalicious payloads. For example, sending malicious PDF document which if the victim opens, it will compromise the system.

Methodologies
>The web attack module is a unique way of utilizing multiple web-based attacks in order to compromise the intended victim. This module is used by performing phishing attacks against the victim if they click the link. There is a wide variety of attacks that can occur once they click a link.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/229d81fc-99f6-4004-ba5a-43edd3196eba)

Service Enumeration
>N.A.

Penetration
>N.A

## Forensic Tools
### 1. BinWalk

High-Level Summary
>Binwalk is a great tool when we have a binary image and have to extract embedded files and executable codes out of them.

Recommendations
>It is even used to identify the files and codes which are embedded inside the firmware images. Binwalk is compatible with magic signatures for UNIX file utility as it uses libmagic library.

Methodologies
>binwalk supports a variety of command-line options that allow you to customize the analysis and extraction process, such as the signature database to use, the output format, or the extraction options. You can use these options to fine-tune the analysis and extraction to suit your needs.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/76e6e14a-2c1f-4549-b723-7ba84e43aecd)

Service Enumeration
>N.A.

Penetration
>N.A

### 2. Autopsy

High-Level Summary
>Autopsy is a digital forensics tool that is used to gather the information form forensics. Or in other words, this tool is used to investigate files or logs to learn about what exactly was done with the system.

Recommendations
>It could even be used as a recovery software to recover files from a memory card or a pen drive.

Methodologies
>Autopsy comes pre-installed in Kali Linux Just type “autopsy” in the terminal.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/99ef3e3e-ad08-4f4e-99f0-d59522a16e5f)

Service Enumeration
>N.A.

Penetration
>N.A
