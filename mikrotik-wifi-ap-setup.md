# SSID VLAN Tagging

```terminal
/interface wifi
add name=wifi-guest-2g interface=wifi1 ssid=119Guest security-name=guest-profile vlan-mode=access vlan-id=2
add name=wifi-guest-5g interface=wifi2 ssid=119Guest security-name=guest-profile vlan-mode=access vlan-id=2
add name=wifi-apple-2g interface=wifi1 ssid=119Apple security-name=apple-profile vlan-mode=access vlan-id=5
add name=wifi-apple-5g interface=wifi2 ssid=119Apple security-name=apple-profile vlan-mode=access vlan-id=5
add name=wifi-personal-2g interface=wifi1 ssid=119Personal security-name=personal-profile vlan-mode=access vlan-id=6
add name=wifi-personal-5g interface=wifi2 ssid=119Personal security-name=personal-profile vlan-mode=access vlan-id=6
add name=wifi-gaming-2g interface=wifi1 ssid=119Gaming security-name=gaming-profile vlan-mode=access vlan-id=7
add name=wifi-gaming-5g interface=wifi2 ssid=119Gaming security-name=gaming-profile vlan-mode=access vlan-id=7
add name=wifi-anycubic-2g interface=wifi1 ssid=119AnyCubic security-name=anycubic-profile vlan-mode=access vlan-id=9
add name=wifi-anycubic-5g interface=wifi2 ssid=119AnyCubic security-name=anycubic-profile vlan-mode=access vlan-id=9
add name=wifi-brother-2g interface=wifi1 ssid=119Brother security-name=brother-profile vlan-mode=access vlan-id=10
add name=wifi-brother-5g interface=wifi2 ssid=119Brother security-name=brother-profile vlan-mode=access vlan-id=10
add name=wifi-work-2g interface=wifi1 ssid=119Work security-name=work-profile vlan-mode=access vlan-id=11
add name=wifi-work-5g interface=wifi2 ssid=119Work security-name=work-profile vlan-mode=access vlan-id=11
add name=wifi-bose-2g interface=wifi1 ssid=119Bose security-name=bose-profile vlan-mode=access vlan-id=14
add name=wifi-bose-5g interface=wifi2 ssid=119Bose security-name=bose-profile vlan-mode=access vlan-id=14

/interface bridge port
add bridge=bridge interface=wifi-guest-2g pvid=2 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-guest-5g pvid=2 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-apple-2g pvid=5 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-apple-5g pvid=5 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-personal-2g pvid=6 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-personal-5g pvid=6 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-gaming-2g pvid=7 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-gaming-5g pvid=7 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-anycubic-2g pvid=9 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-anycubic-5g pvid=9 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-brother-2g pvid=10 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-brother-5g pvid=10 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-work-2g pvid=11 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-work-5g pvid=11 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-bose-2g pvid=14 frame-types=admit-only-untagged-and-priority-tagged
add bridge=bridge interface=wifi-bose-5g pvid=14 frame-types=admit-only-untagged-and-priority-tagged
```
