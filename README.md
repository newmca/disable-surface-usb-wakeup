# disable-surface-usb-wakeup
Service to disable usb wakeup caused by a Surface Type Go Cover interrupting suspend.
When the lid (the keyboard) is closed, it will keep sending wake signals, then suspending, then sending wake signals again, then suspending, causing a loop that drains the device's battery.
You may or may not need this depending on your distro or kernel version.

## Instructions

1. Create `/etc/systemd/system/disable-surface-usb-wakeup.service`
2. Run `sudo systemctl enable disable-surface-usb-wakeup.service`
2. Run `sudo systemctl start disable-surface-usb-wakeup.service`