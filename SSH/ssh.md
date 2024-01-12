# Core 1
```yaml
hostname Core1
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.2 255.255.255.224
no shut
exit
do write
```

# Core 2
```yaml
hostname Core1
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.3 255.255.255.224
no shut
exit
do write
```

# Dis1
```yaml
hostname Dis1
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.4 255.255.255.224
no shut
exit
do write
```

# Dis 2
```yaml
hostname Dis2
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.5 255.255.255.224
no shut
exit
do write
```

# F1
```yaml
hostname F1_HO
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.6 255.255.255.224
no shut
exit
do write
```

# F2
```yaml
hostname F2_HO
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.7 255.255.255.224
no shut
exit
do write
```

# F3
```yaml
hostname F3_HO
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.8 255.255.255.224
no shut
exit
do write

```

# F4
```yaml
hostname F4_HO
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.9 255.255.255.224
no shut
exit
do write
```

# F5
```yaml

hostname F5_HO
enable secret level 15 2023@InFraGF
banner motd "KHONG PHAN SU MIEN VAO"
service password-encryption
ip domain-name gf.com
no ip domain-lookup
crypto key generate rsa general-keys modulus 1024
username adminlocalHO secret 2023@InFraGF
ip ssh ver 2
line vty 0 4
login local
transport input SSH
exit
do wr
interface vlan 1
description Management
ip add 172.10.1.10 255.255.255.224
no shut
exit
do write
```