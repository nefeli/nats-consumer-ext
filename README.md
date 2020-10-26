# nats_consumer_ext

Telegraf External plugins for NATS IO messages. This plugin extends the
functionality of nats_consumer plugin on telegraf official repo
[nats_consumer](https://github.com/influxdata/telegraf/tree/002bc9d4866d9b4806feabe7f734ba2ec3c8876f/plugins/inputs/nats_consumer).

- adding tags from the subjects
  e.g.,

  ```
  subject_tags = {"country": 1, "resourcetype": 4}
  ```
  to add two tags "country"="us","resourcetype"="memory",
  for all the data from the subject "country.us.type.memory" or "country.*.type.*"


## compile
```
CGO_ENABLE=0 go build
```

## run demo
```
./nats_consumer_ext -config nats_consumer_ext.conf
```
