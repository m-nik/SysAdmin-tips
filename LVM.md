### create lvm with 100% size
```
lvcreate --name docker-lv -l 100%FREE docker-vg
```

### Resize PV
```sh
pvs
pvresize /dev/sdb1
pvs
```

### Extend an lvm
```sh
lvextend /dev/longhorn-vg/longhorn-lv -L 49.994G --resizefs
```
