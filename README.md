# sys

This script simplifies common `systemctl` interactions by providing shorter aliases for frequent commands and flags.

## Installation

You can just add it to a directory in `$PATH` environment variable, `$HOME/.local/bin/` is recommended

## Usage

```bash
sys [options] [command] [args]
```

### Options

- `-h`, `--help`    Returns this message
- `-u`, `--user`    Operate at user level
- `-n`, `--now`     Apply immediately (with enable/disable)

### Commands

- `st`, `--st`, `--start`      Start service(s)
- `rt`, `--rt`, `--restart`    Restart service(s)
- `rd`, `--rd`, `--reload`     Reload service(s)
- `sp`, `--sp`, `--stop`       Stop service(s)
- `ee`, `--ee`, `--enable`     Enable service(s)
- `de`, `--de`, `--disable`    Disable service(s)

### Examples

**Start a system service:**
```bash
sys st nginx
```

**Enable a system service and start it immediately:**
```bash
sys -n ee docker
```

**Reload a user service:**
```bash
sys -u rd pw-loudcompd
```
