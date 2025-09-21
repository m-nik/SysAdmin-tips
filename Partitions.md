

### resize a partition
```sh
sudo parted /dev/sdb
(parted) print        # برای دیدن پارتیشن‌ها
(parted) resizepart 1 100%
(parted) quit
```
