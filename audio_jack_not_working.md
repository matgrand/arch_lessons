# Audio Jack Not Working
## Note: this fixes the audio jack, but we lose the internal microphone

1. Create a file `/etc/modprobe.d/oldHDA.conf` with the following content:
```bash
options snd_intel_dspcfg dsp_driver=1
```
> This will force the system to use the old HDA driver, and the microphone will stop working
2. Reboot

> I'm writing by memory, may not be 100% accurate