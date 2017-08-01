# Cleartran-Migration
Cisco switch configurations for NPC Cleartran Migration

NPC01SR01
*********

vlan 4073
 name F5_non-route_L2-10.0.90.112/28

interface Port-channel10
 description ** npc01lbasm03a **
 switchport
 switchport mode trunk
 swicthport trunk allowed vlan 4071,4073


interface GigabitEthernet6/21
 description ** np01f5ltm01-1.10 **
 switchport
 switchport access vlan 4071
 switchport mode access
 speed 1000
 duplex full
 channel-protocol lacp
 channel-group 10 mode active


interface GigabitEthernet6/22
 description ** np01f5ltm01-1.11 **
 switchport
 switchport access vlan 4071
 switchport mode access
 speed 1000
 duplex full
 channel-protocol lacp
 channel-group 10 mode active


interface GigabitEthernet4/36
 description ** wnpcqwbzkn01 **
 switchport
 switchport access vlan 4073
 switchport mode access
 speed 1000
 duplex ful
