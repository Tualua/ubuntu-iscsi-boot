# ubuntu-iscsi-boot
Install and boot Ubuntu from iSCSI Target Server

Original post: https://ubuntuforums.org/showthread.php?t=2442081

- Boot from ISO and add disk-detect/ibft/enable=true partman-iscsi/iscsi_auto=true for the boot options
- Enter language and keyboard options
- Enter a management IP address and then go immediately to shell (Ctrl-F2):
- Start ISCSI using the following commands (no other option is given anywhere in the install process. If you don't do this now, you see no disks):

```
modprobe iscsi_ibft
iscsistart -N
iscsistart -b
```
