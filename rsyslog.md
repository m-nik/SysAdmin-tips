

# Remote logs using rsyslog
```
module(load="imudp")
input(type="imudp" port="514")

template(name="AllUDP" type="string" string="/var/log/remote/%fromhost-ip%-%programname%.log")

if ($inputname == "imudp") then {
    action(type="omfile" dynaFile="AllUDP")
    stop
}
```

