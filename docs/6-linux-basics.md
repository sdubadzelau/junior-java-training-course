[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

## Linux Basics

1. Managing users and access
   1. `sudo`, `su`
   2. `whoami`
   3. `usermod -L username` - Locking the account prevents a user from logging in, without erasing the account or changing their password.
2. Monitoring and controlling processes
   1. ps - Without any options, the ps command shows processes running in the current shell
   2. top - This command shows an interactive, constantly-updating view of processes on the system.
   3. PID, parent PID
   4. KILL process
3. Managing services
   1. systemctl
      1. list, enable, disable, stop, start
4. Managing software with APT
   1. apt update - updates package list from repository
   2. apt upgrade - install new versions of installed packages
   3. apt install - install package
   4. apt list [package name or regex] - list packages
   5. apt search - search package by description
   6. apt show - show info about package
5. Securing programs with AppArmor (cmd: aa-status)
   1. Path-based mandatory access control mechanism
   2. AppArmor ensures that programs only access what they're supposed to
   3. Application permissions managed inside config files like this e.g. /etc/apparmor.d/usr.bin.[appname], /etc/apparmor.d/usr.bin.man
      In naming AppArmor profiles, periods replace slashes in the absolute path to a program
6. rConfiguring networking with NetworkManager
   1. Controlling network settings
   2. /etc/network/interfaces
   3. nmtui - NetworkManager TUI
   4. nmcli - info about active connections. `nmcli c` - connections info, `nmcli d` - devices netwotk info 
7. Managing the firewall with nftables
   1. Nftables replaces iptables
   2. The iptables command now uses nftables on the back end
8. Exploring logs

