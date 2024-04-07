# homelab-adguard
Configuration is saved in `conf/AdGuardHome.yaml`. The file contains salted password and won't be synchronized on github.
A new file will be generated when starting the service.

After configuring the user and password (http on port `3000`), stop the service and add the path to `upstream.txt` to configure the upstream DNS servers:
```
upstream_dns_file: /opt/adguardhome/conf/upstream.txt
```
Also changing the mode to parallel is a good idea (can be done also from the GUI):
```
upstream_mode: parallel
```
Now restart the service.