# raspi-ansible
git repo to setup raspberries with ansible

. Flash SD card with raspbian OS [raspbian-stretch-lite](https://downloads.raspberrypi.org/raspbian_lite_latest) using [etcher](https://etcher.io/)
. Create SSH file on SD card (to enable SSH access to RPI3)
. Create SSH keys on ansible host `ssh-keygen -t rsa -b 4096 -C "<any comment>"`
. Copy SSH keys to RPI3 `ssh-copy-id username@IP-address` (RPI standard user is pi)


