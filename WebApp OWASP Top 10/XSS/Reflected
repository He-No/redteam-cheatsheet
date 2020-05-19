## Client sided

inject something malicious & it reflects on the webpage of the user (client-sided)
Requires social engineering (open malicious URL to users/employees)

<?php
$username = $_GET['username'];
echo "Hi $username!";
?>

index?username=Hendrik
	Ø Hi Hendrik!

index?username=<script>alert(1)</script>
	Ø javascript pop-up "1" returns on the screen!

## PAYLOAD:
<script>alert('1')</script>