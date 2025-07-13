---
layout: post
title: What Is a Data Engineering Pipeline? Explained Like Super Mario
image: "assets/posts/20230314/20230314.webp"
category: Data Engineering
read_time: true
show_date: true
description: Discover how data pipelines work—from ingestion to serving—through a fun analogy with Super Mario Bros. Learn key tools, stages, and best practices in data engineering.
author: Manfredi Miraula
tags:
  - data engineering pipeline
  - what is a data pipeline
  - data ingestion
  - data processing
  - data storage
  - data serving
  - ETL pipeline
  - Apache Kafka
  - Apache Spark
  - AWS Redshift
  - Super Mario analogy
  - data engineering for beginners
  - modern data stack
  - real-time data processing
  - data lake vs warehouse
---
When I think about data engineering pipelines, Super Mario Bros often comes to mind. For those who are not familiar with the video game, Mario is a plumber who is teleported to a fantasy world. To me, the role of data engineering is very much like the role of a plumber, only in the analytics world. Where a real plumber would deal with tubes, water flows, and use a wrench, in data engineering, you are working with data flows, data pipes, and code as your tool.

Let's abandon the parallelism with plumbing and define what a data engineering pipeline really is. Simply put, it's a set of processes and tools that move data from its source to its destination. It involves several key components that work together to ensure that data is transformed, cleaned, and made accessible to data scientists, analysts, and other stakeholders. In this blog post, we'll explore the key components of a data engineering pipeline.

## Data Ingestion
First, we want to centralize everything in one place. The first component of a data engineering pipeline is data ingestion. This involves extracting data from various sources, such as databases, APIs, or file systems, and moving it to a centralized location where it can be processed and analyzed. If we imagine our pipeline as a big funnel, this step represents the "mouth" of the funnel. As we get down to the end of the funnel, data is cleaned and reorganized, but at this stage, the data is as close as it can be to the original source.
<centre>
<img src="/assets/posts/20230314/mario_bros__plumbing_by_imaginatorvictor_db885s6-fullview.jpeg"  alt="Data Engineering pipeline funnel (photo by Artem Podrez)" /> 
</centre>

Data ingestion is a critical step in the data engineering process because it sets the foundation for all downstream tasks.

There are several tools and frameworks available for data ingestion, such as Apache Kafka, Apache Nifi, and AWS Kinesis. These tools provide functionalities for data ingestion, transformation, and streaming. In addition, they also allow for data validation, error handling, and retry mechanisms to ensure that data is ingested correctly.

## Data Processing
Remembering the funnel image, we are now within the "belly" of the funnel. In here, you can imagine two big gears crunching and molding the data to shape them from their original format to their "final" format. A lot of steps can occur at this stage, since the data processing can vary a lot (e.g., filtering out irrelevant data, aggregating data, and joining multiple data sources), depending on the final outcome of the data.
Generally speaking, this step involves transforming and cleaning the data to make it usable for analysis.

Data processing is typically done using batch or stream processing frameworks. Batch processing frameworks, such as Apache Spark and Apache Hadoop, process data in large batches, while stream processing frameworks, such as Apache Flink and Apache Storm, process data in real-time.

## Data Storage
We arrived close to the end of our pipeline, this is the neck of the funnel. Our main objective here is to store the processed data in a way that is easily accessible to data consumers and scalable. There are several storage options available, including traditional relational databases, NoSQL databases, and data lakes.

Relational databases, such as MySQL and PostgreSQL, are well-suited for structured data, while NoSQL databases, such as MongoDB and Cassandra, are better suited for unstructured data. Data lakes, such as AWS S3 and Azure Data Lake, provide a scalable and cost-effective solution for storing large amounts of data.

## Data Serving
The final component of a data engineering pipeline is data serving. This involves making the processed data accessible to downstream applications, such as data analytics tools, machine learning models, and dashboards. Data serving can be done through APIs or data warehouses.

Data warehouses, such as AWS Redshift and Google BigQuery, provide a centralized location for storing and querying data, while APIs provide a programmatic interface for accessing data.

## Super Mario Bors Inc. 
The role of a data engineer can sit within a specific stage of the funnel, but it's likely that you will see multiple stages of the funnel during your career. It might seem daunting at first, especially considering the velocity of innovation that is always present in this space. However, if you approach the work with an open mind and without the fear of "having to know it all," I believe you can be rewarded.

If you like challenges and possess a curious mind, this could be the plumbing work you need to fulfill your working days!