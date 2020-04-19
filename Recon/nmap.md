### flags:	
-sC = default scripts
-p = port
-sU = udp scan	
-T = aggressive scan
-p- = all ports
--script = script	
-sv = enumerate versions
-A = enumerate OS	
-oN = output nmap format	
-sS = stealth

### modes:										
Intense scan:
nmap -T4 -A -v <target>

Intense scan + UDP:
nmap -sS -sU -T4 -A -v <target>

Intense scan, all TCP:
nmap -p 1-65535 -T4 -A -v <target>

Intense scan, no ping:
nmap -T4 -A -v -Pn <target>

Ping scan:
nmap -sn <target>

Quick scan:
nmap -T4 -F <target>

Quick scan+:
nmap -sV -T4 -O -F –version-light <target>

Quick traceroute:
nmap -sn –traceroute <target>

Regular scan:
nmap <target>

Slow comprehensive scan:
nmap -sS -sU -T4 -A -v -PE -PP -PS80,443 -PA3389 -PU40125 -PY -g 53 –script “default or (discovery and safe)” <target>

### Additional information:
https://www.securesolutions.no/zenmap-preset-scans/

### Additional information:
Intense scan
Command: nmap -T4 -A -v <target>
Should be reasonable quick, scan the most common TCP ports. It will make an effort in determining the OS type and what services and their versions are running.
This comes from having a pretty fast timing template (-T4) and for using the -A option which will try determine services, versions and OS. With the verbose output (-v) it will also give us a lot of feedback as Nmap makes progress in the scan.

Intense scan plus UDP
Command: nmap -sS -sU -T4 -A -v <target>
Same as the regular Intense scan, just that we will also scan UDP ports (-sU).
The -sS option is telling Nmap that it should also scan TCP ports using SYN packets. Because this scan includes UDP ports this explicit definition of -sS is necessary.

Intense scan, all TCP ports
Command: nmap -p 1-65535 -T4 -A -v <target>
Leave no TCP ports unchecked.
Normally Nmap scans a list of 1000 most common protocols, but instead we will in this example scan everything from port 1 to 65535 (max). The 1000 most common protocols listing can be found in the file called nmap-services.

Intense scan, no ping
Command: nmap -T4 -A -v -Pn <target>
Just like the other intense scans, however this will assume the host is up. Usefull if the target is blocking ping request and you already know the target is up.

Ping scan
Command: nmap -sn <target>
Do only a ping only on the target, no port scan.

Quick scan
Command: nmap -T4 -F <target>
Scan faster than the intense scan by limiting the number of TCP ports scanned to only the top 100 most common TCP ports.

Quick scan plus
Command: nmap -sV -T4 -O -F –version-light <target>
Add a little bit of version and OS detection and you got the Quick scan plus.

Quick traceroute
Command: nmap -sn –traceroute <target>
Use this option when you need to determine hosts and routers in a network scan. It will traceroute and ping all hosts defined in the target.

Regular scan
Command: nmap <target>
Default everything. This means it will issue a TCP SYN scan for the most common 1000 TCP ports, using ICMP Echo request (ping) for host detection.

Slow comprehensive scan
Command: nmap -sS -sU -T4 -A -v -PE -PP -PS80,443 -PA3389 -PU40125 -PY -g 53 –script “default or (discovery and safe)” <target>
This scan has a whole bunch of options in it and it may seem daunting to understand at first. It is however not so complicated once you take a closer look at the options. The scan can be said to be a “Intense scan plus UDP” plus some extras features.
It will put a whole lot of effort into host detection, not giving up if the initial ping request fails. It uses three different protocols in order to detect the hosts; TCP, UDP and SCTP.
If a host is detected it will do its best in determining what OS, services and versions the host are running based on the most common TCP and UDP services. Also the scan camouflages itself as source port 53 (DNS).
