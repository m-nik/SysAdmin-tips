
## Rescue ssh keys
On Proxmox cluster nodes, root SSH keys are often stored in the cluster filesystem (`/etc/pve/priv/authorized_keys`) and `~/.ssh/authorized_keys` is a **symlink**. When pve-cluster is stopped or a node is removed from the cluster, that filesystem may disappear, causing SSH key authentication to fail and locking you out if password login is disabled.
Solution:
```
cp .ssh/authorized_keys .ssh/rescue_authorized_keys
vi /etc/ssh/sshd_config
```
sshd_config:
```
AuthorizedKeysFile      .ssh/authorized_keys .ssh/rescue_authorized_keys
```
```
systemctl restart ssh
```
