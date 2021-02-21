# Useful Stuffs

This is my personal list of useful stuffs, such as linux command, configurations and issues resolution guides, I've found on Internet or from my personal experience.


* Reconfigure GRUB2 on Ubuntu -> https://wiki.ubuntu.com/SecurityTeam/KnowledgeBase/GRUB2SecureBootBypass
```
sudo dpkg-reconfigure grub-pc
```

* Duplicate Android screen on PC -> https://github.com/Genymobile/scrcpy
```
scrcpy
```

* Redirect Ubuntu Firewall to another file
1. Create a new file in `/etc/rsyslog.d` with name `10-iptables.conf`
2. Paste following into file:
```
:msg, contains, "iptables denied: " -/var/log/iptables.log
& stop
```
3. Restart Syslog Service `sudo service rsyslog restart`
