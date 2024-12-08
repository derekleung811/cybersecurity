Part 1 of CEH Skill Check covers Footprinting and Reconnaissance, Scanning Networks, Enumeration, and Vulnerability Analysis modules. In this part, you are required to perform passive and active reconnaissance of the target organization, enumerating services, shares, users, user groups, etc., and perform vulnerability analysis of the identified systems/networks on the target. You need to note all the information discovered in this part of the Skill Check and proceed to the subsequent phases of the ethical hacking cycle in the next part of the Skill Check.

Challenge 1:
You are performing reconnaissance for CEHORG and has been assigned a task to find out the physical location of one of their webservers hosting www.certifiedhacker.com. What are the GEO Coordinates of the webserver? Note: Provide answer as Latitude, Longitude. (Format: NN.NNN, *NN.NNN)

<img width="468" alt="image" src="https://github.com/user-attachments/assets/fbf89af3-d3a4-4655-b84d-c87df18cacda"> \
<img width="362" alt="image" src="https://github.com/user-attachments/assets/c61c31b2-84bf-4148-aa1d-6fb202a009aa">

Challenge 2:
Identify if the website www.certifiedhacker.com allows DNS zone transfer. (Yes/No) (Format: Aa)

```
  dig www.certifiedhacker.com axfr
```

Challenge 3:
Identify the number of live machines in 172.16.0.0/24 subnet. (Format: N)

Nmap –sP –PS22 172.16.0.0/24
 

Challenge 4:
Find the IP address of the machine which has port 21 open. Note: Target network 172.16.0.0/24 (Format: NNN.NN.N.NN)

Nmap –sV –p21 172.16.0.0/24
 

Challenge 5:
Find the IP address of the Domain Controller machine in 10.10.10.0/24. (Format: NN.NN.NN.NN)

Nmap –sV –p389 10.10.10.10/24
 



Challenge 6:
Perform a host discovery scanning and identify the NetBIOS name of the host at 10.10.10.25. (Format: AAAAAAAAA)

Nmap –script smb-os-discovery 10.10.10.25
 
 

Challenge 7:
Perform an intense scan on 10.10.10.25 and find out the FQDN of the machine in the network. (Format: AaaaaAaaa.AAAAAA.aaa)

Nmap -sV -A -T4 10.10.10.25
 
 
 

Challenge 8:
What is the DNS Computer Name of the Domain Controller? (Format: AaaaaAaaa.AAAAAA.aaa)

Nmap -sV -A -T4 10.10.10.25

Same as Challenge 7

Challenge 9:
While performing a security assessment against the CEHORG network, you came to know that one machine in the network is running OpenSSH and is vulnerable. Identify the version of the OpenSSH running on the machine. Note: Target network 192.168.0.0/24. (Format: N.NaN)

Nmap -sV -p22 192.168.0.0/24
 

Challenge 10:
During a security assessment, it was found that a server was hosting a website that was susceptible to blind SQL injection attacks. Further investigation revealed that the underlying database management system of the site was MySQL. Determine the machine OS that hosted the database. (Format: Aaaaaa)

nmap -sV -O -A -p 3306 192.168.0.0/24
 


nmap -sV -O -A -p- 3306 192.168.0.55
 

Challenge 11:
Perform LDAP enumeration on the target network and find out how many user accounts are associated with the domain. (Format: N)

ldapsearch -x -h 10.10.10.25 -b "DC=CEHORG,DC=com" "objectclass=user" cn

 
 

Challenge 12:
Perform an LDAP Search on the Domain Controller machine and find out the latest version of the LDAP protocol. (Format: AAAAaN)

ldapsearch -h 10.10.10.25 -x -s base namingcontexts

 

Challenge 13:
What is the IP address of the machine that has NFS service enabled? Note: Target network 192.168.0.0/24. (Format: NNN.NNN.N.NN)

nmap -sV -p 2049 192.168.0.0/24
 

Challenge 14:
Perform a DNS enumeration on www.certifiedhacker.com and find out the name servers used by the domain. (Format: aaN.aaaaaaaa.aaa, aaN.aaaaaaaa.aaa)

dnsenum www.certifiedhacker.com
 

Challenge 15:
Find the IP address of the machine running SMTP service on the 192.168.0.0/24 network. (Format: NNN.NNN.N.NN)
namp -sV -p 25 192.168.0.0/24

 

Challenge 16:
Perform an SMB Enumeration on 192.168.0.51 and check whether the Message signing feature is enabled or disabled. Give your response as Yes/No. (Format: Aaa)

nmap -A -T4 192.168.0.51

 

Challenge 17:
Perform a vulnerability research on CVE-2022-30171 and find out the base score and impact of the vulnerability. (Format: N.N Aaaaaa)

https://nvd.nist.com
 
Challenge 18:
Perform vulnerability scanning for the domain controller using OpenVAS and identify the number of vulnerabilities with severity level as "medium". (Format: N)

Challenge 19:
Perform vulnerability scanning for the webserver hosting movies.cehorg.com using OpenVAS and identify the severity level of RPC vulnerability. (Format: N)

Challenge 20:
Perform vulnerability scanning for the Linux host in the 172.16.0.0/24 network using OpenVAS and find the number of vulnerabilities with severity level as medium. (Format: N)
![Uploading image.png…]()
