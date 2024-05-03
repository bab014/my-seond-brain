---
date: 2024-05-02
tags:
    - code-snips
hubs:
    - "[[linux]]"
urls:
    - https://ar.al/2019/03/11/setting-multiple-key-bindings-for-the-same-action-in-gnome/
---
#  Gnome Set A Keybinding

A quick snippet to remember how to change a key binding programmatically

```bash
gsettings set org.gnome.desktop.wm.keybindings switch-group "['<Alt>Above_Tab', '<Super>Above_Tab']"
```
 
