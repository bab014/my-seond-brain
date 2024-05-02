---
date: 2024-05-02
tags:
    - fact
hubs:
    - [[vim]]
---
# Vim Format Note Name

The find/replace regex to format a title on my note template for obsidian

```vim
s/\(# \)[^_]*_/\1/ | s/_/ /g | s/\<./\u&/g
```

