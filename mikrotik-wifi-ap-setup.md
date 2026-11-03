# SSID VLAN Tagging

/interface wifi
add name=wifi-guest2g interface=wifi1 ssid=119Guest security-name=guest-profile vlan-mode=access vlan-id=2
add name=wifi-guest5g interface=wifi2 ssid=119Guest security-name=guest-profile vlan-mode=access vlan-id=2
add name=wifi-apple2g interface=wifi1 ssid=119Apple security-name=apple-profile vlan-mode=access vlan-id=5
add name=wifi-apple5g interface=wifi2 ssid=119Apple security-name=apple-profile vlan-mode=access vlan-id=5
add name=wifi-personal2g interface=wifi1 ssid=119Personal security-name=personal-profile vlan-mode=access vlan-id=6
add name=wifi-personal5g interface=wifi2 ssid=119Personal security-name=personal-profile vlan-mode=access vlan-id=6
add name=wifi-gaming2g interface=wifi1 ssid=119Gaming security-name=gaming-profile vlan-mode=access vlan-id=7
add name=wifi-gaming5g interface=wifi2 ssid=119Gaming security-name=gaming-profile vlan-mode=access vlan-id=7
add name=wifi-anycubic2g interface=wifi1 ssid=119AnyCubic security-name=anycubic-profile vlan-mode=access vlan-id=9
add name=wifi-anycubic5g interface=wifi2 ssid=119AnyCubic security-name=anycubic-profile vlan-mode=access vlan-id=9
add name=wifi-brother2g interface=wifi1 ssid=119Brother security-name=brother-profile vlan-mode=access vlan-id=10
add name=wifi-brother5g interface=wifi2 ssid=119Brother security-name=brother-profile vlan-mode=access vlan-id=10
add name=wifi-work2g interface=wifi1 ssid=119Work security-name=work-profile vlan-mode=access vlan-id=11
add name=wifi-work5g interface=wifi2 ssid=119Work security-name=work-profile vlan-mode=access vlan-id=11
add name=wifi-bose2g interface=wifi1 ssid=119Bose security-name=bose-profile vlan-mode=access vlan-id=14
add name=wifi-bose5g interface=wifi2 ssid=119Bose security-name=bose-profile vlan-mode=access vlan-id=14

/interface bridge port
add bridge=bridge interface=ether4
add bridge=bridge interface=ether1
add bridge=bridge interface=ether2
add bridge=bridge interface=ether3
add bridge=bridge interface=wifi-home  pvid=10 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-guest pvid=20 frame-types=admit-only-untagged-and-priority-tagged   
