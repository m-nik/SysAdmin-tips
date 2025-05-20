# Software RAID in linux
```
cat /proc/mdstat
mdadm --detail /dev/md2
mdadm --add /dev/md2 /dev/nvme0n1p3
```
