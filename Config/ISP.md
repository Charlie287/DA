# ISP_R5
```
hostname ISP_R5
access-list 1 permit any
ip nat inside source list 1 interface e0/0 overload
int e0/0
ip add dhcp
ip nat out
no shut
exit
int e0/1
ip add 115.30.25.1 255.255.255.252
no shut
exit
int s1/2
ip add 209.100.150.14 255.255.255.252
ip ospf 209 area 1
ip nat in
no shut
ex
int s1/1
ip add 209.100.150.10 255.255.255.252
ip ospf 209 area 1
ip nat in
no shut
ex
router ospf 209
passive-interface e0/0
passive-interface e0/1
net 209.100.150.0 0.0.0.31 area 1
net 115.30.25.0 0.0.0.3 area 1
default-information originate
exit
```

# ISP_R1
```
hostname ISP_R1
int s1/0
ip add 209.100.150.1 255.255.255.252
ip ospf 209 area 1
no shut
exit
int s1/1 
ip add 209.100.150.5 255.255.255.252
ip ospf 209 area 1
no shut
exit
int s2/1
ip add 209.100.150.9 255.255.255.252
ip ospf 209 area 1
no shut
exit
int e0/1
ip add 100.150.20.1 255.255.255.252
no shut
exit
router ospf 209
net 209.100.150.0 0.0.0.31 area 1
net 100.150.20.0 0.0.0.15 area 1
passive-interface e0/1
exit
```

# ISP_R2
```
hostname ISP_R2
int s1/0
ip add 209.100.150.2 255.255.255.252
ip ospf 209 area 1
no shut
exit
int s1/1 
ip add 209.100.150.17 255.255.255.252
ip ospf 209 area 1
no shut
exit
int e0/1
ip add 100.150.20.5 255.255.255.252
no shut
exit
router ospf 209
net 209.100.150.0 0.0.0.31 area 1
net 100.150.20.0 0.0.0.15 area 1
passive-interface e0/1
exit
do wr
```

# ISP_R3
```
hostname ISP_R3
int s1/0
ip add 209.100.150.21 255.255.255.252
ip ospf 209 area 1
no shut
exit
int s1/1 
ip add 209.100.150.6 255.255.255.252
ip ospf 209 area 1
no shut
exit
int s2/1
ip add 209.100.150.13 255.255.255.252
ip ospf 209 area 1
no shut
exit
int e0/1
ip add 100.150.20.13 255.255.255.252
no shut
exit
router ospf 209
net 209.100.150.0 0.0.0.31 area 1
net 100.150.20.0 0.0.0.15 area 1
passive-interface e0/1
exit
do wr
```

# ISP_R4
```
hostname ISP_R4
int s1/0
ip add 209.100.150.22 255.255.255.252
ip ospf 209 area 1
no shut
exit
int s1/1 
ip add 209.100.150.18 255.255.255.252
ip ospf 209 area 1
no shut
exit
int e0/1
ip add 100.150.20.9 255.255.255.252
no shut
exit
router ospf 209
net 209.100.150.0 0.0.0.31 area 1
net 100.150.20.0 0.0.0.15 area 1
passive-interface e0/1
exit
do wr
```
