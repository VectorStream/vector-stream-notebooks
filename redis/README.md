# Redis

## To Deploy on Openshift:

```bash
oc login -u developer -p developer
```

## Use the `oc` CLI, to create new instance of PostgreSQL:
 * [Deployment](https://github.com/VectorStream/vector-stream/tree/main/components/vector-databases/redis)
```bash
oc create -f components/vector-databases/redis/base/namespace.yaml
oc apply -k components/vector-databases/redis/operators/overlays/default
oc get pods -n redis-rag
oc apply -k components/vector-databases/redis/instance/overlays/default
```

## [Creating an index and populating it with documents using PostgreSQL+pgvector](Langchain-PgVector-Ingest.ipynb)
![20241112162935](https://i.imgur.com/L6Ust1M.png)

## [Querying a PGVector index](Langchain-PgVector-Query.ipynb)
![20241112162721](https://i.imgur.com/qm0ATb3.png)