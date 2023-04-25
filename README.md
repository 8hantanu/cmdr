# cmdr
Command Runner

## Setup

Add the below snippet to `~/.bashrc`.

```bash
export CMDR=<path_to_cmdr_folder>
cmdr () {
  $CMDR/cmdr ${1:--h} $2
  src_file="$CMDR/src.sh"
  if [ -f $src_file ]; then
    source $src_file
  fi
  if [ -f $src_file ]; then
    rm $src_file
  fi
}
```

### Help

To use cmdr do `cmdr <action>`:
```
-e, --edit              Edit commands file
-g, --grep              Grep for a particular command
-x, --execute <regex>   Execute a set of commands
-s, --source  <regex>   Source a set of commands
-l, --history           Show commands history
-V, --version           Print version
-h, --help              Display this help
```
