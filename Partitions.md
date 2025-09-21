

### rescan partitions
```sh
fdisk -l /dev/sdb
sudo sh -c "echo 1 > /sys/class/block/sdb/device/rescan"
fdisk -l /dev/sdb
```



### resize a partition
```sh
cfdisk /dev/sdb
```
OR
```sh
sudo parted /dev/sdb
(parted) print        # برای دیدن پارتیشن‌ها
(parted) resizepart 1 100%
(parted) quit
```




