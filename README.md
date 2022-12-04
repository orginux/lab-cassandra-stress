# lab-cassandra-stress
Run tests:

```bash
docker exec -it cassandra-1 bash
```

```bash
cd /opt/cassandra/tools/bin/
```

```bash
./cassandra-stress user profile=/var/lib/stress-profiles/test_profile_1.yml duration=1m "ops(insert=1)" truncate=once
```


Monitoring:
```bash
docker exec -it cassandra-2 bash
```

```bash
watch  -t -d nodetool tablehistograms stresscql test
```
