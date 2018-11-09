## Description

Control daemon in /service/ by daemontools

## Usage

```bash
daemon  DAEMON
daemon  -r DAEMON
daemon  -k DAEMON
daemon  -h
```

## Options

```
-h, --help  show this help message and exit  
-r, --run   Run daemon  
-k, --kill  Kill daemon  
```

## Example

- Show status of DAEMON  
  `$ daemon DAEMON`

- Run DAEMON  
  `$ daemon -r DAEMON`

- Kill DAEMON  
  `$ daemon -k DAEMON`

## DAEMON conf examle

```
---
script: |
  #!/bin/bash

  echo "Hello World!"
bin: ls
user: cloudops
extrainrun: |
  echo "------------"
  echo "sleep 5..."
  sleep 5
log:
  size: 10000000
  number: 10
```
