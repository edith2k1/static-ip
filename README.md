# Cấu hình IP tĩnh

    sudo nano /etc/netplan/00-installer-config.yaml
    
> Copy đoạn code này vô

    # This is the network config written by 'subiquity'
    network:
      ethernets:
        ens160:
          dhcp4: no
          addresses: [172.20.232.100/16]
          gateway4: 172.20.0.1
          nameservers:
            addresses: [8.8.8.8,8.8.4.4]
      version: 2
      
> Save lại, chạy lệnh này

    sudo netplan try --state /etc/netplan
        
> Kiểm tra IP đã thiết lập thành công hay chưa

    ip a

![alt](https://i.imgur.com/nSbAw2u.png)
