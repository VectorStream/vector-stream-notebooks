# Redis

## Access notebook folder in JupyterHub
`path: vector-stream-notebooks/redis`
![20241115082429](https://i.imgur.com/Vl5IvC2.png)
## To Deploy on Openshift:

```bash
oc login -u developer -p developer
```

## Use the `oc` CLI, to create new instance of PostgreSQL:
 * [Deployment](https://github.com/VectorStream/vector-stream/tree/main/components/vector-databases/redis)
```bash
$ oc create -f https://raw.githubusercontent.com/VectorStream/vector-stream/refs/heads/main/components/vector-databases/redis/operators/base/namespace.yaml
$ oc apply -k https://github.com/VectorStream/vector-stream/components/vector-databases/redis/operators/overlays/default
$ oc get pods -n redis-rag -w                                                             03:47:53 PM
NAME                                        READY   STATUS    RESTARTS   AGE
rec-0                                       2/2     Running   0          2m38s
rec-1                                       2/2     Running   0          2m1s
rec-2                                       2/2     Running   0          63s
redis-enterprise-operator-9c9c4b89b-5fbrv   2/2     Running   0          2m43s
$ oc apply -k https://github.com/VectorStream/vector-stream/components/vector-databases/redis/instance/overlays/default
$ oc get svc redb-rag-instance  -n redis-rag # redb-rag-instance.redis-rag.svc.cluster.local  and the exposed port Use this service name for the notebooks
$ oc get secret redb-redb-rag-instance -n redis-rag -o jsonpath='{.data.password}' | base64 -d # Use this password for the notebooks
```

## [Creating an index and populating it with documents using PostgreSQL+pgvector](Langchain-PgVector-Ingest.ipynb)
![20241112162935](https://i.imgur.com/L6Ust1M.png)

## [Querying a PGVector index](Langchain-PgVector-Query.ipynb)
![20241112162721](https://i.imgur.com/qm0ATb3.png)