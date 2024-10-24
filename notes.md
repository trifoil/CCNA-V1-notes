## top-4 commands

1) show the running config
```
Sw-Floor-1# show running-config
```

2) banner motd
```
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# banner motd #Authorized Access Only#
```

3) show ip interfaces 
```
show ip interface brief
```

4) hostname
```
Switch# configure terminal
Switch(config)# hostname Sw-Floor-1
Sw-Floor-1(config)#
```

* stars with a letter
* contain no spaces
* end with a letter or digit
* use only letters, digits, and dashes
* be less than 64 characters in length



## passwords

1) secure user EXEC mode access
```
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line console 0
Sw-Floor-1(config-line)# password cisco
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

2) secure privileged EXEC access
```
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# enable secret class
Sw-Floor-1(config)# exit
Sw-Floor-1#
```

3) secure VTY lines
```
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# line vty 0 15
Sw-Floor-1(config-line)# password cisco
Sw-Floor-1(config-line)# login
Sw-Floor-1(config-line)# end
Sw-Floor-1#
```

4) encrypt all plaintext passwords
```
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# service password-encryption
Sw-Floor-1(config)#
```

## configurations

1) write config
```
write memory
```

or

```
copy running-config startup-config
```

2) reboot the device (without saving conf)
```
reload
```

3) erase config
```
erase startup-config
```

4) show what's in a directory (i.e. nvram)
```
dir nvram
```

## ip addresses

ipv4 -> 32bits -> the structure of an IPv4 address is called dotted decimal notation
ipv6 -> 128bits

media factors :
* Distance
* Environment
* Amount
* Cost

SVI (switch virtual interface) does not have a physical port associated. default is vlan1

## switch vlan add ip
```
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# interface vlan 1
Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0
Sw-Floor-1(config-if)# no shutdown
Sw-Floor-1(config-if)# exit
Sw-Floor-1(config)# ip default-gateway 192.168.1.1
```

the default gateway is also configured

## notes

