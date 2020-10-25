# check_os_release #

This is a Nagios/Icinga plugin to check if the currently installed operating system version is outdated. It checks whether the installed version is about to reach end-of-life or whether a newer release is available.

Currently only Debian and Ubuntu are supported.

## Usage ##
```
usage: check_os_release [-h] [-v] [--eolWarningDays DAYS]
                        [--eolCriticalDays DAYS] [--releaseWarningDays DAYS]
                        [--releaseCriticalDays DAYS] [--lts] [--server]

Check whether OS release is outdated.

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose         increase output verbosity
  --eolWarningDays DAYS
                        set WARNING status if less than DAYS until end-of-life
                        (default: 30)
  --eolCriticalDays DAYS
                        set CRITICAL status if less than DAYS until end-of-
                        life (default: 7)
  --eolIgnore           ignore end-of-life
  --releaseWarningDays DAYS
                        set WARNING status if new release available for more
                        than DAYS (default: 0)
  --releaseCriticalDays DAYS
                        set CRITICAL status if new release available for more
                        than DAYS (default: 30)
  --releaseIgnore       ignore any new release
  --lts                 [Ubuntu] check only for LTS releases
  --server              [Ubuntu] check for server EOL dates
```
