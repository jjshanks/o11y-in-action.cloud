## Run Echo Service

```
go run main.go 2>&1 | tee echo.log
```

## Generate Logs

```
while true ; do curl -s -o
/dev/null localhost:4242/echo ; sleep 1 ; done
```

## Log Infra

Setup grafana, loki, and promtail

```
docker-compose up
```

## Add Datasource

Add `http://loki:3100` as the url for a Loki datasource on grafana http://localhost:3000/

## See Logs

On the explore page you should be able to set your label filter to `service` and `echo` and after
pressing run query you should see the logs that have been generated.
