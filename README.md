## Vagrant box for Tor + Privoxy + Arm

This will spin up a vagrant box with Tor + Privoxy + Arm.

Use this at your own risk.

## Install

```bash
vagrant up
```

## Verify

```bash
vagrant@tor:~$ netstat -nltp
(No info could be read for "-p": geteuid()=1000 but you should be root.)
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 0.0.0.0:111             0.0.0.0:*               LISTEN      -
tcp        0      0 0.0.0.0:8118            0.0.0.0:*               LISTEN      -
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      -
tcp        0      0 0.0.0.0:9050            0.0.0.0:*               LISTEN      -
tcp        0      0 0.0.0.0:9051            0.0.0.0:*               LISTEN      -
tcp        0      0 0.0.0.0:37128           0.0.0.0:*               LISTEN      -
tcp6       0      0 :::111                  :::*                    LISTEN      -
tcp6       0      0 :::22                   :::*                    LISTEN      -
tcp6       0      0 :::49719                :::*                    LISTEN      -
```


## Ports

```
- tcp/9050 : Tor socks5
- tcp/9051 : control Tor
- tcp/8118 : Privoxy

```
