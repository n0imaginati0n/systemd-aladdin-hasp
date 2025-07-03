# systemd-aladdin-hasp

systemd service units for SafeNet Sentinel and Aladdin HASP keys drivers

Replacement of the old-styled init.d scripts to the systemd service units
with a similar functionality. You need to install haspd package first. Then
you can remove or copy in the safe place init.d scripts:

 - /etc/init.d/haspd
 - /etc/init.d/haspd.outformat

and link given scripts to execution:

```sh
systemctl link ./scripts/aksubd.service
systemctl link ./scripts/hasplm.service
```

enable them:

```sh
systemctl enable aksubd
systemctl enable hasplm
```

start them

```sh
systemctl start aksubd
systemctl start hasplm
```

