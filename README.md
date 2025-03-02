# FreeRADIUS Prometheus Exporter

Prometheus exporter for [FreeRADIUS](https://freeradius.org) metrics.

Supports FreeRADIUS 3.0.x.

### Installation

    go install github.com/bvantagelimited/freeradius_exporter@latest

### Run Project using Docker

1. Create .env file template based .env_template
2. Specify variables in a .env file
3. Run Project using Docker

```bash
docker-compose up -d
```

### Usage

Name               | Description
-------------------|------------
radius.address     | Address of [FreeRADIUS status server](https://wiki.freeradius.org/config/Status), defaults to `127.0.0.1:18121`.
radius.secret      | FreeRADIUS client secret, defaults to `adminsecret`.
radius.timeout     | Timeout, in milliseconds, defaults to `5000`.
radius.homeservers | Addresses of home servers separated by comma, e.g. "172.28.1.2:1812,172.28.1.3:1812"
web.listen-address | Address to listen on for web interface and telemetry, defaults to `:9812`.
web.telemetry-path | Path under which to expose metrics, defaults to `/metrics`.
version            | Display version information
config             | Config file (optional)

### Environment Variables

Name               | Description
-------------------|------------
RADIUS_ADDRESS     | Address of [FreeRADIUS status server](https://wiki.freeradius.org/config/Status).
RADIUS_SECRET      | FreeRADIUS client secret.
RADIUS_TIMEOUT     | Timeout, in milliseconds.
RADIUS_HOMESERVERS | Addresses of home servers separated by comma, e.g. "172.28.1.2:1812,172.28.1.3:1812"
