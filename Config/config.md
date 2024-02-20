# NAT
```
access-list 1 permit any
ip nat inside source list 1 interface e0/0 overload

int e0/0
ip add dhcp
no shut
ip nat out
```

# R1
```
int s1/0
ip add 209.100.150.1 255.255.255.252
ip nat in
no shut
ex

int s1/1
ip add 209.100.150.5 255.255.255.252
ip nat in
no shut
ex

int s1/2
ip add 209.100.150.9 255.255.255.252
ip nat in
no shut
ex

int e0/1
ip add 100.150.20.1 255.255.255.252
ip nat in
no shut
ex
```

# R2
```
int s1/0
ip add 209.100.150.2 255.255.255.252
no shut
ex

int s1/2
ip add 209.100.150.13 255.255.255.252
no shut
ex

int s1/1
ip add 209.100.150.17 255.255.255.252
no shut
ex

int e0/1
ip add 100.150.20.5 255.255.255.252
no shut
ex
```

# R3
```
int s1/0
ip add 209.100.150.21 255.255.255.252
ip nat in
no shut
ex

int s1/1
ip add 209.100.150.6 255.255.255.252
ip nat in
no shut
ex

int s1/2
ip add 209.100.150.14 255.255.255.252
ip nat in
no shut
ex
```



# R4
```
int s1/0
ip add 209.100.150.22 255.255.255.252
no shut
ex

int s1/2
ip add 209.100.150.10 255.255.255.252
no shut
ex

int s1/1
ip add 209.100.150.18 255.255.255.252
no shut
ex

int e0/1
ip add 100.150.20.9 255.255.255.252
no shut
ex
```

# FW1
