# big-data-primer

##THIS IS VERY INITIAL DRAFT. JUST THE SKELETON. ITS A WORK IN PROGRESS.


## Introduction 

Learn about everything big data

## Big Data Dimensions

- Collection
- Ingestion
- ETL
- Storage
- Insights

## Collection

### Tools
- FluentD
- Logstash
- Scoop

## CDC

Change Data Capture

### Features
- Stream changes from database in a reliable, scalable manner


### Tools

- https://debezium.io/

### Further reads

- https://www.confluent.io/blog/how-bolt-adopted-cdc-with-confluent-for-real-time-data-and-analytics/
- https://netflixtechblog.com/dblog-a-generic-change-data-capture-framework-69351fb9099b
- https://eng.uber.com/dbevents-ingestion-framework/


## Data Quality

### 

- Verify data type matching
- cardinality of source and target
- Value distributions of source and target
- profiling the statistics against historic trends to detect anomalies and potential quality issues

### Tools

- https://griffin.apache.org/
- https://github.com/awslabs/deequ (Spark Scala — from AWS)
- https://github.com/ronald-smith-angel/owl-data-sanitizer (Pyspark)

### Further reads

- https://dzone.com/articles/java-amp-apache-spark-for-data-quality-amp-validat
- https://quickbooks-engineering.intuit.com/taming-data-quality-with-circuit-breakers-dbe550d3ca78
- https://www.youtube.com/watch?v=fXHdeBnpXrg
- https://medium.com/datamindedbe/data-quality-libraries-the-right-fit-a6564641dfad
- https://medium.com/disney-streaming/testing-asynchronous-pipelines-with-fs2-and-weaver-test-f0ffd37676d
- https://aws.amazon.com/blogs/big-data/build-a-distributed-big-data-reconciliation-engine-using-amazon-emr-and-amazon-athena/
- https://eng.uber.com/monitoring-data-quality-at-scale/


## Data Lake (with upsert and delete support)
- Data lifecycle management
- Store clean data 
- Data Access control
- Upserts
- Schema evolution

### Tools
- Hudi
- Delta Lake
- Iceberg

### Further reads
- https://databricks.com/session_na20/a-thorough-comparison-of-delta-lake-iceberg-and-hudi

 
## Ingestion

- Kafka

## Stream Processing

- Flink
- Kafka Streams
- Spark Streaming

## Orchestration
- Workflows
- Pipeline
- Scheduling

### Tools

- https://airflow.apache.org/
- Uber’s Piper
- Netflix’s Meson
- Uber’s Cadence 
- https://docs.dagster.io/
- https://www.getdbt.com/product/


### Further reads

- https://netflixtechblog.com/unbundling-data-science-workflows-with-metaflow-and-aws-step-functions-d454780c6280
- https://eng.uber.com/managing-data-workflows-at-scale/ 

## Data Discovery and Search

- Typically uses a search engine (ES , Solr etc.) for providing search capabilities and a graph (neo4j, Janusgraph etc.) for storing relationships (lineage etc.).

### Features


### Tools


### Further reads

- https://cloud.google.com/data-catalog
- DataHub (Linkedin)
- Databook (Uber)
- Metacat (Netflix)
- https://medium.com/criteo-labs/datadoc-the-criteo-data-observability-platform-2cd826a9a1afAirBnb’s Dataportal
- https://cloud.google.com/data-catalog


## Text Search 

- Typically uses Lucene based indexing.

### Features
- Text indexing

### Tools

- Elasticsearch
- Solr

## Metrics

- Typically uses a time-series datastore

### Tools
- Apache Druid
- Pinot
- Uber’s M3
- Grafana

## Cost

### Features

- Cost tagging and attribution
- alerting
- budgeting
- monitoring
- forecasting
- reporting

### Tools

- https://github.com/cloud-custodian/cloud-custodian
- https://github.com/Teevity/ice

### Further reads

- https://netflixtechblog.com/byte-down-making-netflixs-data-infrastructure-cost-effective-fee7b3235032
- https://www.youtube.com/watch?v=ChupgIbZr5Q&ab_channel=AWSEvents


## Lamba Architecture
Query batch data + Query Real time data => Let the application join the data

## Kappa Architecture
Everything is a stream. Batch data is converted into stream and joined with Real time. Application is only written once to query the stream data.
- https://milinda.pathirage.org/kappa-architecture.com/
- https://eng.uber.com/kappa-architecture-data-stream-processing/
- https://www.talend.com/blog/2017/08/28/lambda-kappa-real-time-big-data-architectures/


## Wide column stores
- Hbase 
- Dynamodb
- Cassandra

## Graph Databasees
- https://neo4j.com/
- https://janusgraph.org/

## Consensus algorithems and tools
- ZAB, Paxos and Raft 
- ZK (ZAB)
- etcd (Raft)
- Chubby
