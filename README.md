`nix-top`
=========

This is a script to help users figure out what's building.

Usage:

```
 $ nix-env -if .
 $ nix-top --help
Usage: nix-top [options]
   -d, --delay [seconds]            In seconds (default: 0.5)
   -1, --once                       Only run once (generates one screen)

```

Example output:

```
Summary:
     owner       pid  nr_processes → derivation
     foobar  2104885     3 → /tmp/nix-build-fastclick-2024.01.15-21.drv-1

 * * *

:: (nixbld1) → /tmp/nix-build-fastclick-2024.01.15-21.drv-1
  UID     PID    PPID STIME     TIME COMMAND
30001 2104921 2104888 18:51 00:00:00 bash -e /nix/store/v6x3cs394jgqfbi0a42pam708flxaphh-defau
30001 2107718 2104921 18:51 00:00:00 find . -type f -exec sed -i s/\/bin\/rm/rm/g {} ;
```
