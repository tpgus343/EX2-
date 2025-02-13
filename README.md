# Milvus and PostgreSQL (pgvector) Docker Setup Guide

This document explains how to set up Milvus and PostgreSQL with the pgvector extension in a Docker environment. Additionally, it covers the steps to connect to Milvus from Jupyter and use it for data insertion and similarity search.

## 1. Milvus Setup

### 1.1 Download Docker Compose File
To install Milvus, download the docker-compose.yml file using the following command:

```bash
wget https://github.com/milvus-io/milvus/releases/download/v2.3.21/milvus-standalone-docker-compose.yml -O docker-compose.yml

