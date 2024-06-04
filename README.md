# Real-Time Named Entity Recognition and Visualization

This project implements a real-time data pipeline for named entity recognition and visualization using Spark Streaming, Apache Kafka, and the ELK stack (Elasticsearch, Logstash, Kibana). The pipeline continuously processes text data from a real-time source, extracts named entities, and visualizes the top 10 entities in real-time using Kibana's bar plot feature.

## Project Overview

The project consists of the following components:

1. **Real-Time Data Ingestion:**
   - A Python application reads text data from a real-time source and streams it to Apache Kafka.

2. **Named Entity Recognition with PySpark:**
   - A PySpark Structured Streaming application extracts named entities from the incoming text data and maintains a running count.

3. **Kafka Integration:**
   - Processed data, containing named entity counts, is sent to another Kafka topic.

4. **Data Visualization with ELK Stack:**
   - Logstash ingests data from Kafka and sends it to Elasticsearch for indexing.
   - Kibana creates and displays a real-time bar plot of the top 10 named entities and their counts.

## Project Setup

To run the project, follow these steps:

1. **Install Dependencies:**
   - Ensure Python, Apache Spark, Apache Kafka, Elasticsearch, Logstash, and Kibana are installed and configured.

2. **Set Up Kafka Topics:**
   - Create two Kafka topics: one for incoming data (e.g., `topic1`) and another for processed data (e.g., `topic2`).

3. **Run Python Application:**
   - Execute the Python application to read and stream real-time text data to Kafka.

4. **Run PySpark Streaming Application:**
   - Run the PySpark Structured Streaming application to process data from Kafka topic1 and send results to Kafka topic2.

5. **Configure ELK Stack:**
   - Configure Logstash to ingest data from Kafka topic2 and send it to Elasticsearch for indexing.
   - Set up Kibana to visualize the indexed data with a bar plot.

6. **View Real-Time Visualizations:**
   - Access Kibana to view the real-time bar plot of the top 10 named entities and their counts.
