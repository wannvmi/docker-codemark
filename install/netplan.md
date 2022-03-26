# /etc/netplan#

01-network-manager-all.yaml
# Let NetworkManager manage all devices on this system
network:
  version: 2
  renderer: NetworkManager


## 新配网 方案

# Let NetworkManager manage all devices on this system
network:
  version: 2
  renderer: networkd
  ethernets:
    enp3s4f1:
      addresses:
      - 192.168.16.152/24
      gateway4: 192.168.16.1
      nameservers:
        addresses:
        - 223.5.5.5
        - 223.6.6.6
