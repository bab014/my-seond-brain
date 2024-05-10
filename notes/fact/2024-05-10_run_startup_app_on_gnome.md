---
date: 2024-05-10
tags:
    - fact
hubs:
    - "[[linux]]"
urls:
    - https://stackoverflow.com/questions/8247706/start-script-when-gnome-starts-up
---
#  Run Startup App On Gnome

The way you would have a script run when logging into `gnome`

I'm currently using this for starting a virtual machine in the background. This allows me to connect to it through RDP

We need a `[name].desktop` file in `~/.config/autostart` directory
```toml
[Desktop Entry]
Version=1.0
Type=Application
Name=UbuntuStart
GenericName=Ubuntu Virtual Machine
Comment=A way to start an ubuntu virtual machine
Exec=/home/bret/.local/scripts/startup.sh
Terminal=false
Icon=gnome-terminal
Categories=System;

```
