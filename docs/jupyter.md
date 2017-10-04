---
layout: default
title: 'Jupyter'
---

# Jupyter Cheat Sheet

A bunch of cool things about the Jupyter coding environment.

## <a name='toc'></a>Table of Contents

* [Keyboard Shortcuts](#shortcuts)
* [Using over SSH](#ssh)

---

## <a name='shortcuts'></a>Keyboard Shortcuts

When in command mode (press `esc` to enable):

| Shortcut | Command |
|:--------:| ------- |
|h|Open keyboard shortcuts window|
|l|Toggle line numbers|
|up / k|Select cell above|
|down / j|Select cell below|
|a|Insert cell above|
|b|Insert cell below|
|x|Cut selected cell|
|c|Copy selected cell|
|v|Paste cell below|
|shift + v|Paste cell above|
|dd|Delete cell|
|z|Undo cell deletion|

When in edit mode (press `enter` to enable):

| Shortcut | Command |
|:--------:| ------- |
|shift + tab|Tooltip|
|cmd + /|Comment/uncomment current or selected lines|
|shift + enter|Run cell, select below|
|cmd + enter|Run cell|
|cmd + up|Go to beginning of cell|
|cmd + down|Go to end of cell|
|cmd + left|Go to beginning of current line|
|cmd + right|Go to end of current line|

Return to [Table of Contents](#toc).

## <a name='ssh'></a>Using over SSH

1. Start jupyter notebook on the remote machine.
``` bash
remote_user@remote_host$ jupyter notebook --no-browser --port=8889
```

2. Start an SSH tunnel on the local machine, ensuring the port numbers (8889) match.
``` bash
local_user@local_host$ ssh -N -L localhost:8888:localhost:8889 remote_user@remote_host
```

3. Open a browser and type `localhost:8888` in the address bar.

The session can be closed with `ctrl+c` on the local machine, and the jupyter server can be closed on the remote machine with `ctrl+c ctrl+c`.

Return to [Table of Contents](#toc).
