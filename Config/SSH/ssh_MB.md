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
username adminlocalMB secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
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
exit
router ospf 10
net 172.16.1.0 0.0.0.3 area 0
net 172.10.2.0 0.0.0.31 area 0
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
line vty 0 4
login local
transport input SSH
exit
do wr
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
net 172.16.1.4 0.0.0.3 area 0
net 172.10.2.0 0.0.0.31 area 0
exit
do write
```

# F1_MB
```yaml

```

# F2_MB
```yaml

```

# F3_MB
```yaml


```

