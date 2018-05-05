
<img src="./yZ_Logo.png" width="100">

# raspi-ansible
git repo to setup raspberries with ansible

1. Flash SD card with raspbian OS [raspbian-stretch-lite](https://downloads.raspberrypi.org/raspbian_lite_latest) using [etcher](https://etcher.io/)
2. Create SSH file on SD card (to enable SSH access to RPI3)
3. Create SSH keys on ansible host `ssh-keygen -t rsa -b 4096 -C "<any comment>"`
4. Copy SSH keys to RPI3 `ssh-copy-id username@IP-address` (RPI standard user is pi). Thx to <https://hvops.com/articles/ansible-post-install/> for the hint.

## the ansible part

Thanks to <http://justin.isamaker.com/ansible-pi/> for providing very nice playbooks to setup the raspberry. This was the basis for the work done here.

