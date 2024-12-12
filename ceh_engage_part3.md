**CEH Engage Part 3**

Part 3 of CEH Skill Check covers Session Hijacking, Evading IDS, Firewalls, and Honeypots, Hacking Web Servers, Hacking Web Applications, and SQL Injection modules. In this part, you must take over active network and application sessions, compromise firewall, IDS, and other perimeter defense mechanisms, and exploit the organization’s web applications. You need to note all the information discovered in this part of the Skill Check and proceed to the subsequent phases of the ethical hacking cycle in the next part of the Skill Check.

Flags

**Challenge 1:**

CEHORG suspects of a possible session hijacking attack on a machine in its network. The organisation has retained the network traffic data for the session at C:\Users\Admin\Documents in the EH Workstation – 2 as sniffsession.pcap. You have been assigned a task to perform an analysis and find out the protocol that has been used for sniffing on its network. (Format: AAA)

#Module 11 Session Hijacking - Lab 2 - Wireshark#
![Screenshot 2024-12-12 at 11 49 56 AM](https://github.com/user-attachments/assets/d1210604-f1dc-4e0d-b089-729266bfc0a6)

**Challenge 2:**

Perform an HTTP-recon on www.certifiedhacker.com and find out the version of Nginx used by the web server. (Format: N.NN.N)

#Module 13 Hacking Web Servers - Lab 1 - httprecon#
![Screenshot 2024-12-12 at 11 53 33 AM](https://github.com/user-attachments/assets/91dc1966-6db4-4f68-a38b-b722a7b749c8)


**Challenge 3:**

An FTP site is hosted on a machine in the CEHORG network. Crack the FTP credentials, obtain the “flag.txt” file and determine the content in the file. (Format: Aaaaaaa*AAA)

#Module Hacking Web Servers - Lab 2 - Hydra#

```
nmap -p 21 172.16.0.0/24

nmap -p 21 10.10.10.0/24

nmap -p 21 192.168.0.0/24
```

```
hydra -L <username.txt> -P <password.txt> ftp://172.16.0.12
```
![Screenshot 2024-12-12 at 12 08 57 PM](https://github.com/user-attachments/assets/cdab6979-a6b1-4ec8-863e-314000aa648b)

![Screenshot 2024-12-12 at 12 11 40 PM](https://github.com/user-attachments/assets/98e5919d-cd2a-4632-a20e-17075b4f6b14)

**Challenge 4:**

Perform Banner grabbing on the web application movies.cehorg.com and find out the ETag of the respective target machine. (Format: "NaNNNNNaaaNaaNN*N")

**Challenge 5:**

Identify the Content Management System used by www.cehorg.com. (Format: AaaaAaaaa)

**Challenge 6:**

Perform web application reconnaissance on movies.cehorg.com and find out the HTTP server used by the web application. (Format: Aaaaaaaaa-AAA/NN.N)

**Challenge 7:**

Perform Web Crawling on the web application movies.cehorg.com and identify the number of live png files in images folder. (Format: N)

**Challenge 8:**

Identify the load balancing service used by eccouncil.org. (Format: aaaaaaaaaa)

**Challenge 9:**

Perform a bruteforce attack on www.cehorg.com and find the password of user adam. (Format: aaaaaaNNNN)

**Challenge 10:**

Perform parameter tampering on movies.cehorg.com and find out the user for id 1003. (Format: Aaaaa)

**Challenge 11:**

Perform a SQL Injection attack on movies.cehorg.com and find out the number of users available in the database. Use Jason/welcome as login credentials. (Format: N)

**Challenge 12:**

Perform XSS vulnerability test on www.cehorg.com and identify whether the application is vulnerable to attack or not. (Yes/No). (Format: Aa)

**Challenge 13:**

A file named Hash.txt has been uploaded through DVWA (http://10.10.10.25:8080/DVWA). The file is located in the directory mentioned below. Access the file and crack the MD5 hash to reveal the original message; enter the content after cracking the hash. You can log into the DVWA using the following credentials. Note: Username- admin; Password- password Path: C:\wamp64\www\DVWA\hackable\uploads\Hash.txt Hint: Use “type” command to view the file. Use the following link to decrypt the hash- https://hashes.com/en/decrypt/hash (Format: Aa*aaNa)

**Challenge 14:**

Perform command injection attack on 10.10.10.25 and find out how many user accounts are registered with the machine. Note: Exclude admin/Guest user (Format: N)

**Challenge 15:**

You have identified a vulnerable web application on a Linux server at port 8080. Exploit the web application vulnerability, gain access to the server and enter the content of RootFlag.txt as the answer. (Format: Aa*aaNNNN)
