# Core 1_MB
```yaml
hostname Core1_MB
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip routing
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
aaa new-model
aaa authentication login default group radius local
aaa authorization exec default group radius local
radius server WINSERVER
add ipv4 10.10.10.4
key ITInfra2024@GF
ex
line vty 0 4
login authentication default
transport input ssh
exit
vlan 99
name MANAGEMENT_MB
exit
interface vlan 99
description Management
ip add 172.10.2.2 255.255.255.224
no shut
exit
int e0/0
no switchpo
ip add 172.16.1.2 255.255.255.252
ip ospf 10 area 0
no shut
exit
int e0/2
switchport trunk encapsulation dot1q
switchport mode trunk
switchport trunk native vlan 99
exit
router ospf 10
router-id 6.6.6.6
net 172.16.1.0 0.0.0.3 area 0
net 172.10.2.0 0.0.0.31 area 0
net 192.168.0.0 0.0.255.255 area 0
passive-interface e1/0
passive-interface e0/2
passive-interface e0/3
exit
do write
```

# Core 2_MB
```yaml
hostname Core2_MB
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip routing
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalMB secret 2023@InFraGF
ip ssh ver 2
aaa new-model
aaa authentication login default group radius local
aaa authorization exec default group radius local
radius server WINSERVER
add ipv4 10.10.10.4
key ITInfra2024@GF
ex
line vty 0 4
login authentication default
transport input ssh
exit
interface vlan 99
description Management
ip add 172.10.2.3 255.255.255.224
no shut
exit
int e0/0
no switchpo
ip add 172.16.1.6 255.255.255.252
ip ospf 10 area 0
no shut
exit
int e0/2
switchport trunk encapsulation dot1q
switchport mode trunk
exit
router ospf 10
router-id 5.5.5.5
net 172.16.1.4 0.0.0.3 area 0
net 172.10.2.0 0.0.0.31 area 0
net 192.168.0.0 0.0.255.255 area 0
passive-interface e1/0
passive-interface e0/2
passive-interface e0/3
exit
do write
```

# F1_MB
```yaml
hostname F1_MB
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
aaa new-model
aaa authentication login default group radius local
aaa authorization exec default group radius local
radius server WINSERVER
add ipv4 10.10.10.4
key ITInfra2024@GF
ex
line vty 0 4
login authentication default
transport input ssh
exit
no ip routing
ip default-gateway 172.10.2.1
vlan 99
name MANAGEMENT_MB
exit
interface vlan 99
description Management
ip add 172.10.2.4 255.255.255.224
no shut
exit
int range e0/0-1
switchport trunk encapsulation dot1q
switchport trunk native vlan 99
switchport mode trunk
exit
do write
```

# F2_MB
```yaml
hostname F2_MB
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
aaa new-model
aaa authentication login default group radius local
aaa authorization exec default group radius local
radius server WINSERVER
add ipv4 10.10.10.4
key ITInfra2024@GF
exit
line vty 0 4
login authentication default
transport input ssh
exit
no ip routing
ip default-gateway 172.10.2.1
vlan 99
name MANAGEMENT_MB
exit
interface vlan 99
description Management
ip add 172.10.2.5 255.255.255.224
no shut
exit
int range e0/0-1
switchport trunk encapsulation dot1q
switchport trunk native vlan 99
switchport mode trunk
exit
do write
```

# F3_MB
```yaml
hostname F3_MB
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
aaa new-model
aaa authentication login default group radius local
aaa authorization exec default group radius local
radius server WINSERVER
add ipv4 10.10.10.4
key ITInfra2024@GF
exit
line vty 0 4
login authentication default
transport input ssh
exit
no ip routing
ip default-gateway 172.10.2.1
vlan 99
name MANAGEMENT_MB
exit
interface vlan 99
description Management
ip add 172.10.2.6 255.255.255.224
no shut
exit
int range e0/0-1
switchport trunk encapsulation dot1q
switchport trunk native vlan 99
switchport mode trunk
exit
do write

```

