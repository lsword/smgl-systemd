Source Mage GNU/Linux Systemd Scripts
=====================================

Symlinks needed to get things working
-------------------------------------

So to ensure that things are correctly started, you have to add them to a wants.

Symlink /etc/systemd/system/default.target to whatever you want to be the primary runlevel.

    ln -s /lib/systemd/system/multi-user.target

Create symlinks for the things you want started in multi-user level:

    mkdir /etc/systemd/multi-user.target.wants
    cd /etc/systemd/multi-user.target.wants
    ln -s /lib/systemd/system/remote-fs.target
    ln -s /lib/systemd/system/rsyslog.service ''example''

