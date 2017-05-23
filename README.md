# pimp
Triton based R2 plugin for concolic execution (WIP)

---
 ## Asciinema
[![asciicast](http://ak42.io/wp-content/uploads/2017/05/scrot.png)](https://asciinema.org/a/ccncic4ab0m7080dxdl4gye5z)
 
#### Dependencies:
   * r2
   * Triton (and its dependencies)
   * r2pipe
   * lang-python

#### Warning:
Currently, R2 and Triton need to be compiled with the same libcapsone version.
This should change in the future.

As this is still WIP, commands might change, check for the readme file updates after git pull.


### Installation:
add the following line to your radare2rc file:
```
$pimp=#!pipe python /path/to/pimp_wrapper.py
```

### Usage:
Initialise the Triton context:

`$pimp init`

Declare the symbolic variables (memory):

`$pimp input size address`

Emulate execution until a symbolic instruction is met:

`$pimp dcusi`

Emulate execution until a symbolic jump is met:

`$pimp dcusj`

Take Current conditional jump:

`$pimp take`

Avoid current conditional jump:

`$pimp avoid`

Reset triton memory with current binary memory

`$pimp reset`

Load triton generated input back into r2

`$pimp sync`

### Author:
Ayman Khamouma (@dsknctr)
