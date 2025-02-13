# Milvus and PostgreSQL (pgvector) Docker Setup Guide

This document explains how to set up Milvus and PostgreSQL with the pgvector extension in a Docker environment. Additionally, it covers the steps to connect to Milvus from Jupyter and use it for data insertion and similarity search.

## 1. Milvus Setup

### 1.1 Download Docker Compose File
To install Milvus, download the docker-compose.yml file using the following command:

```bash
wget https://github.com/milvus-io/milvus/releases/download/v2.3.21/milvus-standalone-docker-compose.yml -O docker-compose.yml

```

# 1.2 Start Milvus
Navigate to the directory where the `docker-compose.yml` file was downloaded and run the following command to start Milvus:

```bash
sudo docker compose up -d

**Expected output:**

```bash
Creating milvus-etcd  ... done
Creating milvus-minio ... done
Creating milvus-standalone ... done

# 1.3 Verify Milvus Installation
To check if Milvus DB is running properly, use the following command:

```bash
sudo docker compose ps


**Expected output:**

```bash
Name                     Command                  State                            Ports
--------------------------------------------------------------------------------------------------------------------
milvus-etcd         etcd -advertise-client-url ...   Up             2379/tcp, 2380/tcp
milvus-minio        /usr/bin/docker-entrypoint ...   Up (healthy)   9000/tcp
milvus-standalone   /tini -- milvus run standalone   Up             0.0.0.0:19530->19530/tcp, 0.0.0.0

# 1.4 Check Milvus Listening Port
To verify the port Milvus is listening on, use the following command:

```bash
docker port milvus-standalone 19530/tcp

# 2. Connecting to Milvus from Jupyter

## 2.1 Install pymilvus
To connect to Milvus from Python (e.g., Jupyter notebook), first install the `pymilvus` library:

```bash
pip install pymilvus

## 2.2 Running Milvus Data Insert and Search Example
Now that everything is set up, you can run the Milvus example scripts to insert data and search using text embeddings.

- **milvus.py** (Milvus Data Insert Example)
- **milvus_cosine.py** (Search by Text Embedding Example)

# Conclusion
By following this guide, you have successfully set up Milvus and PostgreSQL with the pgvector extension in a Docker environment. You can now use Milvus for vector search and PostgreSQL with pgvector for managing vector data. Additionally, the Python scripts (`milvus.py` and `milvus_cosine.py`) allow you to insert data into Milvus and perform similarity searches based on text embeddings.

