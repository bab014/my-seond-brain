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


The `s/\(# \)[^_]*/\1/` strips off the date
The `s/_/ /g` removes all _ and replaces them with spaces
The `s/\<./\u&/g` capatilizes the words to form a better looking title
