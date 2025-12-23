

# Remote logs using rsyslog
/etc/rsyslog.d/19-remote-udp.conf
```
module(load="imudp")
input(type="imudp" port="514")

template(name="AllUDP" type="string" string="/var/log/remote/%fromhost-ip%-%programname%.log")

if ($inputname == "imudp") then {
    action(type="omfile" dynaFile="AllUDP")
    stop
}
```
```sh
sudo mkdir /var/log/remote
sudo chown syslog:adm /var/log/remote
```
