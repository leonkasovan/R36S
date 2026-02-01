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

Purple R36S Game Console:
```
🔋 designCapacity in your DTB: 2808
🔋 designQmax in your DTB: 3089
• Kinhank → K36 Origin Panel
• Clone R36s → Clone Type 1 Without Amplifier
• Clone R36s → Clone Type 1 Without Amplifier And Invert Right Joystick
• Other → GameConsole HG36(HG3506)
```
