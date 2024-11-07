# Monitoring Server

Monitoring is often done entirely separately from the primary server configuration, so that it does not interfere with daily usage, and can detect when issues arise on the primary server.
Previously, this has been done with a FreeBSD server, partially for experience sake, partially for stable and long-term support, partially for its relatively small install requirements.
The `rc.d` directory included here configures system services for the monitoring server, after the packages have been installed. Services then need to be enabled, as documented in the [FreeBSD handbook](https://docs.freebsd.org/en/books/handbook/book/#config-tuning). 

Prometheus, InfluxDB, Telegraf, Grafana, and AlertManager have dedicated documentation for being setup, which will be added and/or summarised to this repository and/or its wiki in the future.

## Packages

|Program|Purpose|
|---|---|
|`prometheus`|Data collection backend|
|`influxdb`|Data collection backend|
|`telegraf`|Data collection backend|
|`grafana`|Data visualisation software; requires data collection endpoint(s)|
|`alertmanager`| Used for sending notifications to admin|
|`openssh`| SSH backend, for management purposes|

