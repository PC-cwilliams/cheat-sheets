# Ubuntu 20.04
## Resize File System

[Ubuntu: Extend your default LVM space](https://packetpushers.net/ubuntu-extend-your-default-lvm-space/)

### Steps
Resize partition: `sudo cfdisk`
Extend PV physical volume: `pvresize /dev/sda3`
Extend logical volume: `lvextend -l +100%FREE /dev/ubuntu-vg/ubuntu-lv`
Resize: `resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv`