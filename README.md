# R36S
Information for Handheld R36S

**Access console**:  
In EmulationStation -> Start -> Main Menu -> Quit -> Quit EmulationStation  
Plug keyboard to OTG Port then press ALT+F2:  
```
user: ark
pass: ark
```

**Install "SSH over USB" package**: `sudo dpkg -i usb_ssh.deb`

**Fix Audio**:  
Edit `/usr/local/bin/fixvolume.sh`
```
#!/bin/bash
amixer -c 0 cset iface=MIXER,name='Playback Path' SPK
exit 0
```
Console:  
```
amixer cset name="Playback Path" "1"
sudo alsactl store
```

**Stop EmulationStation**:
`sudo systemctl stop emulationstation.service`

**Start EmulationStation**:
sudo systemctl start emulationstation.service
