# lab-cassandra-stress
Run tests:

```bash
docker exec -it cassandra-1 bash
```

```bash
cd /opt/cassandra/tools/bin/
```

```bash
./cassandra-stress write n=10000
```


Monitoring:
```bash
docker exec -it cassandra-2 bash
```

```bash
nodetool tablehistograms keyspace1 standard1
```
