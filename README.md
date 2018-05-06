
<img src="./yZ_Logo.png" width="100">

# raspi-ansible
git repo to setup raspberries with ansible

1. Flash SD card with raspbian OS [raspbian-stretch-lite](https://downloads.raspberrypi.org/raspbian_lite_latest) using [etcher](https://etcher.io/)
2. Create SSH file on SD card (to enable SSH access to RPI3)
3. Create SSH keys on ansible host `ssh-keygen -t rsa -b 4096 -C "<any comment>"`
4. Copy SSH keys to RPI3 `ssh-copy-id username@IP-address` (RPI standard user is pi). Thx to <https://hvops.com/articles/ansible-post-install/> for the hint.

## the ansible part

> Thanks to <http://justin.isamaker.com/ansible-pi/> for providing very nice playbooks to setup the raspberry. This was the basis for the work done here.

### Creating Role Framework
> Thanks to the guys from [digitalocean for their nice summary of roles](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-roles-to-abstract-your-infrastructure-environment).

Roles are created fro everything that shall be setup (e.g. Jupyter). In the roles a directory `jupyter` is created with sub-directories `mkdir files handlers meta templates tasks vars`.

This is what they are all for:

. files: This directory contains regular files that need to be transferred to the hosts you are configuring for this role. This may also include script files to run.
. handlers: All handlers that were in your playbook previously can now be added into this directory.
. meta: This directory can contain files that establish role dependencies. You can list roles that must be applied before the current role can work correctly.
. templates: You can place all files that use variables to substitute information during creation in this directory.
. tasks: This directory contains all of the tasks that would normally be in a playbook. These can reference files and templates contained in their respective directories without using a path.
. vars: Variables for the roles can be specified in this directory and used in your configuration files.

Within all of the directories but the "files" and "templates", if a file called main.yml exists, its contents will be automatically added to the playbook that calls the role.
