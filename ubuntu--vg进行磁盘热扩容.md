# ubuntu--vg进行磁盘热扩容



sudo lsblk
sudo fdisk -lu

sudo growpart /dev/vda 3

# Increase the Physical Volume (pv) to max size
sudo pvresize /dev/vda3

# Expand the Logical Volume (LV) to max size to match
sudo lvresize -l +100%FREE /dev/mapper/ubuntu--vg-ubuntu--lv

# Expand the filesystem itself
sudo resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv
