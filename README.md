# otlp-react 

This repo tries:
- [OpenTelemetry for Javascript/Browser](https://opentelemetry.io/docs/instrumentation/js/getting-started/browser/)
- Tracing backend, e.g. Jaeger, Zipkin 
- Metrics backend, e.g. Prometheus

## Setting up

With `docker-compose.yml`, boot up
1. OpenTelemetry Collector
2. Jaeger, Zipkin 
3. Prometheus

```
$ docker-compose up -Vd # --build --force-recreate --no-deps 
```

Boot up react app

```
$ yarn && yarn dev
```

View apps in browser:
- React app - http://localhost:5173/
- Jaeger UI - http://localhost:16686
- Zipkin - http://localhost:9411
- Prometheus - http://localhost:9090

## References
- [Collector docs](https://opentelemetry.io/docs/collector/)
- [Collector demo](https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/examples/demo)
- [CORS for receiver](https://github.com/open-telemetry/opentelemetry-collector/blob/main/receiver/otlpreceiver/README.md)
- [Instrumentation modules](https://github.com/open-telemetry/opentelemetry-js-contrib)