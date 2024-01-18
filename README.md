# shlib

A collection of small shell scripts that can be used as a standard library.

## Usage

You can clone the repo into your scripts directory and then source the modules
you want into your scripts, for example:

```sh
$ cd ~/.scripts/
$ git clone https://github.com/kvlach/shlib.git
$ cat example
#!/bin/sh

. "$(dirname "$0")/shlib/log"

log_info 'Example script'
```

Some modules use variables for configuration, make sure to set them **after**
importing, otherwise they will get overriden by the default values.
