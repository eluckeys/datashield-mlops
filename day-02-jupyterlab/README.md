# Day 02 — JupyterLab Server

## Problem
Data scientists need to run heavy ML code on powerful remote server
but see results in their laptop browser without using terminal.

## Solution
JupyterLab = web server (like nginx) running on ML server
Data scientist accesses it from browser anywhere.

## Key Config
- ip=0.0.0.0     → accept from all interfaces (not just localhost)
- port=8888      → standard JupyterLab port
- notebook-dir   → where notebooks are stored

## Command
```bash
jupyter lab \
  --ip=0.0.0.0 \
  --port=8888 \
  --notebook-dir=/root/code/datashield/notebooks \
  --no-browser \
  --allow-root &
```

## Verify
```bash
ss -tlnp | grep 8888
# LISTEN 0.0.0.0:8888 ← correct
```

## Linux Equivalent
| JupyterLab | Linux/nginx |
|------------|-------------|
| --ip | listen address |
| --port | listen port |
| --notebook-dir | root directory |
| 0.0.0.0 | bind all interfaces |
| 127.0.0.1 | loopback only |
