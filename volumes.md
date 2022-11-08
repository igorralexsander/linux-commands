# Commands to manage volumes in Linux

## List volumes ids
`sudo blkid`

## List volumes
`sudo lsblk`

## Mount volume by id
`sudo mount -t vfat -o gid=1000,uid=1000 UUID=50BE-08F9 /mnt2`

## Umount volume
`sudo umount /mnt2`

## Format disk
`sudo mkfs -t (vfat, ext4, etc) /dev/sdd`

## Mount volume on boot
Edit file `/etc/fstab`

```
LABEL=writable	/	ext4	discard,errors=remount-ro	0 1
LABEL=system-boot       /boot/firmware  vfat    defaults       0      1
#this volume refers to nfs server
192.168.1.217:/mnt/nfs_server /mnt/nfs_server  nfs defaults,_netdev 0 0

```