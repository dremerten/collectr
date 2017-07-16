# collectr

Quick and easy data collection, designed for [infosetDB](https://github.com/PalisadoesFoundation/infoset-ng)

## Usage

```bash
$ collectr.py --help
usage: collectr.py [-h] [--start] [--stop] [--status] [--restart] [--force]

optional arguments:
  -h, --help  show this help message and exit
  --start     Start the agent daemon.
  --stop      Stop the agent daemon.
  --status    Get daemon daemon status.
  --restart   Restart the agent daemon.
  --force     Stops or restarts the agent daemon ungracefully when used with --stop or
              --restart.
```

## Configuration

Edit `etc/config.yaml` to change configuration options

```yaml
main:
    log_file: collectr.log 
    log_level: debug
    log_directory: ./log
    agent_cache_directory: /home/proxima/Desktop/collectr/cache
    language: en
    interval: 15
    api_server_name: 127.0.0.1
    api_server_port: 6000
    api_server_https: False
    api_server_uri: /infoset/api/v1
```

| Config Options          | Description                    |
| ----------------------- |--------------------------------|
| `log_file`              | Path to log file               |
| `log_level`             | Directory of log file          |
| `agent_cache_directory` | Directory of unsuccessful data posts to infosetdb      |
| `language`              | Language                       |
| `interval`              | Interval of data collection    |
| `api_server_name`       | IP address of `infosetdb`      |
| `api_server_port`       | Port of `infosetdb` server     |
| `api_server_https`      | Use `https` when sending data  |
| `api_server_uri`        | infosetdb `route` prefix       |