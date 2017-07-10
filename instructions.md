### Writing the image
``` dd bs=4M if=2017-07-05-raspbian-jessie-lite.img of=/dev/mmcblk0 status=progress ```
### ssh
In /boot: create empty file ssh
In /home/pi: create .ssh and .ssh/authorized_keys and place .ssh/id_rsa.pub
### static ip
```sudo nano /etc/dhcpcd.conf```
Append the lines:
```
interface eth0
static ip_address=192.168.1.100/24
static routers=192.168.1.1
static domain_name_servers=192.168.1.1
```
or
```
interface wlan0

static ip_address=192.168.1.200/24
static routers=192.168.1.1
static domain_name_servers=192.168.1.1
```
