# thanos-tests

> fork from https://github.com/caarlos0/thanos-playground  and add grafana

This is project is purely educational and is not a pattern for production
deployments or anything like that.

## Usage

Run `docker-compose up -d` and wait.

It will start:

- 2 prometheus instances (`prometheus1` and `prometheus2`)
- 2 thanos sidecars (1 for each prometheus instance) (`sidecar1` and `sidecar2`)
- 1 minio instance
- 1 traefik instance
- 3 thanos query instances
- 1 domain_exporter instance to have some sample metrics
- 1 thanos compact instance (which is short lived, will run and `exit 0`)
- 1 thanos storer (you must add monio bucket first)
- 1 grafana
In our example it will not be used though.

## Accessing things

- http://localhost : querier
- http://localhost:9000 : minio (`minio`/`miniostorage`)
- http://localhost:8080 : traefik dashboard

## More info

- [Thanos docs](https://thanos.io/getting-started.md/) - much here is based on these docs
