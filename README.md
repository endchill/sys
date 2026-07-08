# sys

This script simplifies common `systemctl` interactions by providing shorter aliases for frequent commands and flags.

## Installation

You can Just add it to a directory in `$PATH` environment variable, `$HOME/.local/bin/` is recommended

## Usage

```bash
sys [options] [command] [args]
```

### Options

- `-h`, `--help`    Returns this message
- `-u`, `--user`    Whather to operate in user-level
- `-n`, `--now`     Whather to operates now, used with enable/disable operations

### Commands

- `st`, `--st`, `--start`      Starts systemd services
- `rt`, `--rt`, `--restart`    Restarts systemd services
- `rd`, `--rd`, `--reload`     Reloads systemd services
- `sp`, `--sp`, `--stop`       Stops systemd services
- `ee`, `--ee`, `--enable`     Enables systemd services
- `de`, `--de`, `--disable`    Disables systemd services

### Examples

**Start a system service:**
```bash
sys st nginx
```

**Enable a system service and start it immediately:**
```bash
sys -n ee docker
```

**reload a user service:**
```bash
sys -u rd pw-loudcompd
```
