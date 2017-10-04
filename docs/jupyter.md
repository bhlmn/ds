---
layout: default
title: 'Jupyter'
---

# Jupyter Cheat Sheet

A bunch of cool things about the Jupyter coding environment.

## Table of Contents

* [Keyboard Shortcuts](#shortcuts)
* [Using over SSH](#ssh)

---

## <a name='shortcuts'></a>Keyboard Shortcuts

When in command mode (press `esc` to enable):

When in edit mode (press `enter` to enable):

| Shortcut | Command |
|:--------:| ------- |
|shift+tab|Tooltip|
|cmd+/|Comment/uncomment current or selected lines|
|shift+enter|Run cell, select below|
|cmd+enter|Run cell|

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
