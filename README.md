# newrelic_redis_plugin

New Relic plugin for Redis in Ruby.

Unlike other plugins, it's simple and dedicated for Redis. Most of the statistics are available and built to run as a daemon with PID file and logging.

## Spec

Tested with:
- Ruby 2.0.0
- Gem: dante 0.2.0

## Installation

1. Download the latest [release](https://github.com/kenjij/newrelic_redis_plugin/releases)
2. Extract to the location you want to run the agent from
3. Copy `config/template_newrelic_plugin.yml` to `config/newrelic_plugin.yml`
4. Edit `config/newrelic_plugin.yml` and replace "YOUR_LICENSE_KEY_HERE" with your New Relic license key

## Usage

Simply do `./newrelic_redis_agent` to run in the foreground. Other command line options are:

- `-d` – Run as daemon
- `-c FILE` – Designate a config file

## Config Options

Few configuration options are available in `config/newrelic_plugin.yml`.

- `instance_name` – Name of the instance that will be listed in New Relic; default: "HOSTNAME:PORT"
- `url` – Your Redis server; use "redis://127.0.0.1:6379" as default
- `database` – the database in which to lookup 'total keys'; use "db0" as default

### Example
``` yaml
agents:
  redis:
    instance_name: MyRedisServer
    url: redis://127.0.0.1:6379
    database: db0
```

## License

[MIT](http://opensource.org/licenses/MIT)
