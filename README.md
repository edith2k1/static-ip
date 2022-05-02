Step 1. Run this command

    sudo nano /etc/netplan/00-installer-config.yaml
    
Step 2. Copy this code 

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
      
Step 3. Save and run this command

    sudo netplan try --state /etc/netplan
