HOT SPOT BY PASS
====================================================================================================

# Spoofing MAC Adress
$ ifconfig wlan0 hw ether 00:00:8b:ad:f0:0d
$ iplink set dev wlan0 adress 00:00:8b:ad:f0:0d

# Spoofing IP Adress
$ ifconfig wlan0 192.168.2.3
$ ip addr add 192.168.2.3 dev wlan0


