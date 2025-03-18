# How to map F9 F10 F11 keys to media pause/play, prev, next keys on Thinkpad T14s

1. Create a file with the new bindings in: `/etc/udev/hwdb.d/t14s-keyboard.hwdb`, with the following content:

```
evdev:name:ThinkPad Extra Buttons:dmi:bvn*:bvr*:bd*:svnLENOVO*:pn*:*
 KEYBOARD_KEY_4b=playpause
 KEYBOARD_KEY_4c=nextsong
 KEYBOARD_KEY_4d=previoussong
```

2. Run the following commands to update the keymap:

```
sudo systemd-hwdb update && sudo udevadm control --reload-rules && sudo udevadm trigger
```

3. Reboot for the changes to take effect.