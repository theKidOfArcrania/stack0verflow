# Hibernation does not work

https://askubuntu.com/questions/1034185/ubuntu-18-04-cant-resume-after-hibernate/1038856#1038856

https://askubuntu.com/a/1056364/831088

https://askubuntu.com/questions/1053134/hibernation-in-18-04

```
cat /etc/fstab
```

set this in `/etc/default/grub`
```
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash resume=UUID=<SWAPFILE UUID>
```

assuming that swap is a partition.

Can use `swapon -f` to verify.


