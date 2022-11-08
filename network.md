# Commands to manage network

## Show ip address, can change wlan0 eth0
`ip addr show wlan0 | grep "inet\b" | awk '{print $2}' | cut -d/ -f1`
