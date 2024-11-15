# OpenShift AI - Reference Notebooks

# Pre-requisites
- OpenShift AI Cluster
- Optional:  [RHOAI on OCP on AWS with NVIDIA GPUs](https://catalog.demo.redhat.com/catalog?item=babylon-catalog-prod/sandboxes-gpte.ocp4-demo-rhods-nvidia-gpu-aws.prod&utm_source=webapp&utm_medium=share-link)

## Configure notebooks in OpenShift AI
Under the `redhat-ods-applications` Routes open the JupyterHub URL.
![20241114165033](https://i.imgur.com/durq04o.png)
Click on `Login in with OpenShift` and use your OpenShift credentials to login.
![20241114165110](https://i.imgur.com/2Bebsm4.png)
Login with the credentials.
![20241114165221](https://i.imgur.com/aH2wgGp.png)
Create a new data science project name it  `vector-stream-notebooks`
![20241115081633](https://i.imgur.com/PetCQv4.png)
Create a Workspace and name it `vector-stream-notebooks`
![20241115081714](https://i.imgur.com/6kPAZ9R.png)
Check on `Open` to open the workspace.
![20241115081828](https://i.imgur.com/0q8K66P.png)
Login with the credentials.
![20241115082005](https://i.imgur.com/8D3ct43.png)
Authorize account access.
![20241115082027](https://i.imgur.com/QVLyev4.png)
Clone `https://github.com/VectorStream/vector-stream-notebooks.git` and upload the notebooks to the JupyterHub.
![20241115082140](https://i.imgur.com/Gdpou6N.png)
You are now ready to use the notebooks.
![20241115082347](https://i.imgur.com/3G22I83.png)

## PostgreSQL + pgvector Notebooks
- [README.md](pgvector/README.md)
- [Creating an index and populating it with documents using PostgreSQL+pgvector](pgvector/Langchain-PgVector-Ingest.ipynb)
- [Querying a PGVector index](pgvector/Langchain-PgVector-Query.ipynb)

# Redis Notebooks
- [README.md](redis/README.md)
- [Creating an index and populating it with documents using Redis](redis/Langchain-Redis-Ingest.ipynb)
- [Querying a Redis index](redis/Langchain-Redis-Query.ipynb)