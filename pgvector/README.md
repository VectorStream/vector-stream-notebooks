# PostgreSQL + pgvector

To Deploy on Openshift:

```bash
oc login -u developer -p developer
```

Using the `oc` CLI, to create new instance of PostgreSQL:
 * [Deployment](https://github.com/VectorStream/vector-stream/blob/main/components/vector-databases/pgvector/README.md#deployment)
```bash
oc create -k https://github.com/VectorStream/vector-stream/components/vector-databases/pgvector/instance
```

Reference [Containerfile](https://github.com/VectorStream/vector-stream/blob/main/components/vector-databases/pgvector/Containerfile) for building the image:

[Creating an index and populating it with documents using PostgreSQL+pgvector](Langchain-PgVector-Index.ipynb)
![20241112162935](https://i.imgur.com/L6Ust1M.png)

[Querying a PGVector index](Langchain-PgVector-Query.ipynb)
![20241112162721](https://i.imgur.com/qm0ATb3.png)