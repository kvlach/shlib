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

## Private and Public functions

Private functions in the code are prefixed by `__modulename_`, you are, as the
name suggests, not supposed to use these, public ones are prefixed by
`modulename_`. It is possible to redefine both the private and the public
functions so be careful about that.
