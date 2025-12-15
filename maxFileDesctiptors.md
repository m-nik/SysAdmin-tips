# fix ulimit
https://docs.fluentd.org/installation/before-install

```sh
ulimit -n
1024
```

/etc/security/limits.conf
```conf
root soft nofile 65536
root hard nofile 65536
* soft nofile 65536
* hard nofile 65536
```
