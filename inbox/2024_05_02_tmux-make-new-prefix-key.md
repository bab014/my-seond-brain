---
date: 2024-05-02
tags:
    - fact
hubs:
    - "[[tmux]]"
urls:
    - https://hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/
---
# Tmux Make New Prefix Key

Need to be able to remember how to change my tmux prefix key

Defaults to `C-b` typically like `C-a`
 
```bash
unbind C-b
set-option -g prefix C-a
bind-key C-a send-prefix
```
