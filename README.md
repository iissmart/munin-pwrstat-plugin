# munin-pwrstat-plugin
Munin plugin for monitoring various CyberPower UPS devices via the official PowerPanel utility

## Prerequisites
Install pwrstat from CyberPower (https://www.cyberpowersystems.com/product/software/powerpanel-for-linux/)

Verify pwrstat is working by running `sudo pwrstat -status`

## Installation
Place in /usr/share/munin/plugins, then create a symlink to it from /etc/munin/plugins.

Edit /etc/munin/plugin-conf.d/munin-node and add:
```
[pwrstat]
user root
```

Reload munin config with `sudo service munin-node restart`

## Test Run
Verify the plugin is working by running `sudo munin-run pwrstat`
