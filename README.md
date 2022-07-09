# Floating-Static-Route
----------------------

R1
-----
int g0/2
ip address 192.168.1.1 255.255.255.0
=no shutdown 
int g0/0
ip address 12.0.0.1 255.255.255.252
no shutdown 
int g0/1
ip address 13.0.0.1 255.255.255.252
no shutdown 

Floating Static Route
----------------------
ip route 10.1.1.0 255.255.255.0 12.0.0.2
ip route 10.1.1.0 255.255.255.0 13.0.0.2 15

R2
-----
ip route 192.168.1.1 255.255.255.0 12.0.0.1
ip route 192.168.1.0 255.255.255.0 12.0.0.1
ip route 192.168.1.0 255.255.255.0 13.0.0.1
![Floating Static Route](https://user-images.githubusercontent.com/106605770/178120866-11824676-d30e-43bc-9536-88a82d44ec84.png)
