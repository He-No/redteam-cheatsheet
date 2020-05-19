### Login
ssh <username>@<ip>

### Copy files over ssh:
Host->Vuln machine:
scp -r ~/vbox_shared_folder/htb\ writeups/nc.exe nadine@10.10.10.184:C:\Temp\nc.exe

### Vuln machine->Host:
scp -r nadine@10.10.10.184:C:\\Program\ Files\\NSClient++\\nsclient.ini ~/Documents/hackthebox-writeups/1.machines/ServMon/nsclient.ini


### Algorithm
ssh <ip> -xKeyAlgorithms=+diffie-hellman-group1-sha1 -c aes128-cbc