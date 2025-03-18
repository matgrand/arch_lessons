# Audio Jack Not Working
## Note: this fixes the audio jack, but we lose the internal microphone

## Better fix: 
selecting the profile allows to choose between the headphones PROFILE and the speakers PROFILE,
there is no automatic switch between the two, but it is a good workaround. Since I will never use
the speakers, I can set the profile to headphones and forget about it.



## Bad Fix: use legacy HDA driver and lose mic

1. Create a file `/etc/modprobe.d/oldHDA.conf` with the following content:
```bash
options snd_intel_dspcfg dsp_driver=1
```
> This will force the system to use the old HDA driver, and the microphone will stop working
2. Reboot

> I'm writing by memory, may not be 100% accurate