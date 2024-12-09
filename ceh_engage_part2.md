![image](https://github.com/user-attachments/assets/34992e73-f1ba-48b9-93a9-7cb3c6c4d619)**CEH Engage Part 2**

Part 2 of CEH Skill Check covers System Hacking, Malware Threats, Sniffing, Social Engineering, and Denial-of-Service modules. In this part, you must exploit vulnerabilities identified in the last part and use various network/system/human exploitation techniques to gain access to the target’s systems. You have to perform lateral and vertical privilege escalations and install malicious apps and utilities to maintain access and clear logs to avoid detection. You will need to create and use malicious applications against the target and will also be required to analyze any malware discovered on any of the targets. You need to note all the information discovered in this part of the Skill Check and proceed to the subsequent phases of the ethical hacking cycle in the next part of the Skill Check.

Flags

**Challenge 1:**

You are assigned a task to crack the NTLM password hashes captured by the internal security team. The password hash has been stored in the Documents folder of the Parrot Security console machine. What is the password of user James? (Format: aaaaaa)

#John the Ripper#
```
john --format=NT hashes.txt
```
<figure><img width="796" alt="Screenshot 2024-12-08 at 3 47 56 PM" src="https://github.com/user-attachments/assets/02c1d0a0-2dc7-4f3b-9112-8af9fe11c23c"></figure>

**Challenge 2:**

You are assigned a task to crack the NTLM password hashes captured by the internal security team. The password hash has been stored in the Documents folder of the Parrot Security console machine. What is the password of user Jones? (Format: NNNNNNNN)

```
john --format=NT hashes.txt
```

<figure><img width="796" alt="Screenshot 2024-12-08 at 3 47 56 PM" src="https://github.com/user-attachments/assets/25f64832-8d86-435b-b73e-9d43adaa1b1e"></figure>

**Challenge 3:**

You have been given a task to audit the passwords of a server present in CEHORG network. Find out the password of the user Adam and submit it. (Note: Use Administrator/ CSCPa$$ when asked for credentials). (Format: aaaaaaaaN)

#L0phtCrack#
<img width="1025" alt="Screenshot 2024-12-08 at 3 57 27 PM" src="https://github.com/user-attachments/assets/bbcf2ed7-f617-4393-81a6-33c46cb8adaa">

**Challenge 4:**

An employee in your organization is suspected of sending important information to an accomplice outside the organization. The incident response team has intercepted some files from the employee's system that they believe have hidden information. You are asked to investigate a file named Confidential.txt and extract hidden information. Find out the information hidden in the file. Note: The Confidential.txt file is located at C:\Users\Admin\Documents in EH Workstation – 2 machine. (Format: Aaaaa/AaaaaaaNNNNN)

#SNOW#
```
SNOW.EXE -C Confidential.txt
```
![Screenshot 2024-12-09 at 4 10 24 PM](https://github.com/user-attachments/assets/8d3c783e-f3d2-4b66-9447-1d3ba9f80ebb)

**Challenge 5:**

The incident response team has intercepted an image file from a communication that is supposed to have just text. You are asked to investigate the file and check if it contains any hidden information. Find out the information hidden in the file. Note: The vacation.bmp file is located at C:\Users\Admin\Documents in EH Workstation – 2 machine. (Format: AAANNNNNNN)

#OpenStego#
<figure><img width="655" alt="Screenshot 2024-12-09 at 4 48 20 PM" src="https://github.com/user-attachments/assets/e7ab02bf-6946-43f7-92aa-1c052b408f46"></figure>

**Challenge 6:**

A disgruntled employee in CEHORG has used the Covert_TCP utility to share a secret message with another user in the CEHORG network. Covert_TCP manipulates the TCP/IP header of the data packets to send a file one byte at a time from any host to a destination. It can be used to hide the data inside IP header fields. The employee used the IP ID field to hide the message. The network capture file “Capture.pcapng” has been retained in the “C:\Users\Administrator\Documents” directory of the “EH Workstation – 2” machine. Analyze the session to get the message that was transmitted. (Format: AN*A*AN)

#Wireshark#
![Screenshot 2024-12-09 at 5 15 23 PM](https://github.com/user-attachments/assets/6080407c-65c8-4d4b-8e17-0882f6e8335d)

**Challenge 7:**

You are a malware analyst working for CEHORG. During your assessment within your organisation's network, you found a malware face.exe. The malware is extracted and placed at C:\Users\Admin\Documents in the EH Workstation – 2 machine. Analyze the malware and find out the File pos for KERNEL32.dll text. (Hint: exclude zeros.) (Format: AANN)

#BinText#
![Screenshot 2024-12-09 at 5 28 52 PM](https://github.com/user-attachments/assets/6dd981b4-d4ed-45e9-9b07-4190f9bac2cd)

**Challenge 8:**

Analyze an ELF executable (Sample-ELF) file placed at C:\Users\Admin\Documents in the EH Workstation – 2 machines to determine the CPU Architecture it was built for. (Format: AAAAANN)

**Challenge 9:**

CEHORG has assigned you with analysing the snapshot of the operating system registry and perform the further steps as part of dynamic analysis and find out the whether the driver packages registry is changed. Give your response as Yes/No. (Format: Aaa)

**Challenge 10:**

Perform windows service monitoring and find out the service type associated with display name "afunix". (Format: aaaaaa)

**Challenge 11:**

Use Yersinia on the “EH Workstation – 1” (Parrot Security) machine to perform the DHCP starvation attack. Analyze the network traffic generated during the attack and find the Transaction ID of the DHCP Discover packets. (Format: NaNNNaNNNN)

**Challenge 12:**

CEHORG suspects a possible sniffing attack on a machine in its network. The organization has retained the network traffic data for the session and stored it in the Documents folder in EH Workstation – 2 (Windows 11) machine as sniffsession.pcap. You have been assigned a task to analyze and find out the protocol used for sniffing on its network. (Format: AAA)

**Challenge 13:**

As an ethical hacker, you are tasked to analyze the traffic capture file webtraffic.pcapng. Find out the packet's id that uses ICMP protocol to communicate. Note: The webtraffic.pcapng file is located at C:\Users\Administrator\Documents\ in the Documents folder on EH Workstation – 2 (Windows 11) machine. (Format: NaaaNN)

**Challenge 14:**

CEHORG has found that one of its web application movies.cehorg.com running on its network is leaking credentials in plain text. You have been assigned a task of analysing the movies.pcap file and find out the leaked credentials. Note: The movies.pcapng file is located at C:\Users\Administrator\Documents\ in the Documents folder on EH Workstation – 2 (Windows 11) machine. Make a note of the credentials obtained in this flag, it will be used in the Part 3 of CEH Skill Check. (Format: Aaaaa/aaaaaaa)

**Challenge 15:**

An attacker has created a custom UDP packet and sent it to one of the machines in the CEHORG. You have been given a task to study the ""CustomUDP.pcapng"" file and find the data size of the UDP packet (in bytes). Note: The CustomUDP.pcapng file is located at C:\Users\Administrator\Documents\ in the Documents folder on EH Workstation – 2 (Windows 11) machine. (Format: NNN)

**Challenge 16:**

A denial-of-service attack has been launched on a target machine in the CEHORG network. A network session file "DoS.pcapng" has been captured and stored in the Documents folder of the EH Workstation - 2 machine. Find the IP address of the attacker's machine. (Format: NNN.NNN.N.NN)

**Challenge 17:**

CEHORG hosts a datacenter for its bussiness clients. While analyzing the network traffic it was observed that there was a huge surge of incoming traffic from multiple sources. You are given a task to analyze and study the DDoS.pcap file. The captured network session (DDoS.pcapng) is stored in the Documents folder of the EH Workstation -2 machine. Determine the number of machines that were used to initiate the attack. (Format: N)
