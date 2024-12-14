Devices in the Network

- Router: ISR4331
  - GigabitEthernet0/0/0: 168.90.0.1 (Switch 1 Network)
  - GigabitEthernet0/0/1: 210.3.14.1 (Switch 2 Network)

- Switches:
  - Switch 1: Cisco 2960-24TT
  - Switch 2: Cisco 2960-24TT

- Hosts connected to Switch 1:
  - Laptop0: IP 168.90.0.2
  - PC0: IP 168.90.0.3
  - PC1: IP 168.90.0.4
  - Server0: IP 168.90.0.5
PC3
   - IP: 168.90.0.6
   - Gateway: 168.90.0.1

- Hosts connected to Switch 2:
  - PC2: IP 210.3.14.2
  - Server1: IP 210.3.14.3
  - Server2: IP 210.3.14.4
PC4
    - IP: 210.3.14.4
    - Gateway: 210.3.14.1

DHCP Configuration on Router
- Configure DHCP pools for Switch 1 and Switch 2:
  ip dhcp pool Switch1
  network 168.90.0.0 255.255.0.0
  default-router 168.90.0.1

  ip dhcp pool Switch2
  network 210.3.14.0 255.255.255.0
  default-router 210.3.14.1
