# Spotify End-to-End Data Pipeline Project  

This repository demonstrates a fully automated data engineering pipeline that extracts, processes, and analyzes Spotify's Global Top Songs using APIs and AWS services. Additionally, it includes an analysis of the **Best of 2024 songs in India** based on Spotify data. The project illustrates how modern cloud-native tools enable seamless ETL workflows and facilitate advanced analytics.  

## Project Overview  

This project extracts real-time music data from the **Spotify API**, processes and transforms it, and prepares it for analytics. It enables insights into music trends, including the **Best of 2024 songs in India**, leveraging AWS services for storage, transformation, and querying.  

## Pipeline Architecture  

### **Data Extraction**  
- Extract **Spotify Global Top Songs** via the Spotify API.  
- Convert data into structured formats using **Pandas**.  
- Deploy extraction logic on **AWS Lambda** for automated and scalable workflows.  

### **Data Storage**  
- **AWS S3** stores extracted data:  
  - **Raw Data**: Segmented into **to-process** and **processed** folders.  
  - **Transformed Data**: Organized into structured tables (**songs, artists, albums**).  

### **Data Transformation**  
- Implemented a **Spotify Transformation Lambda Function**:  
  - Triggered on new uploads to the **to-process** folder.  
  - Transforms raw data into relational tables ready for analytics.  
  - Moves processed data to the appropriate S3 folder.  

### **Data Cataloging and Analytics**  
- **AWS Glue**: Crawlers dynamically create a **data catalog** for songs, artists, and albums.  
- **AWS Athena**: Enables SQL-based querying and insights.  

### **Analysis: Best of 2024 Songs in India**  
Using the transformed data, an in-depth analysis was conducted on **Spotify's Best of 2024 songs in India**, revealing key insights into the most streamed songs, popular artists, and trends shaping the Indian music scene.  

## Technologies and Tools Used  
- **Spotify API**: Data source for Indian top songs 2024.  
- **Python**: Data extraction and transformation using **Pandas**.  
- **AWS Lambda**: Serverless functions for automation of extraction and transformation.  
- **AWS S3**: Storage of raw and processed data.  
- **AWS Glue**: Automatic schema detection and data catalog creation.  
- **AWS Athena**: Serverless SQL querying for analytics.  

## Project Features  
✅ **Automated ETL Pipeline**: Fully event-driven workflow.  
✅ **Scalable Design**: AWS Lambda ensures cost-effective scaling.  
✅ **Data Organization**: Logical folder structure in S3 for easy data management.  
✅ **Real-Time Transformation**: Immediate processing upon data ingestion.  
✅ **Advanced Querying**: SQL-based queries via Athena for insights, including the Best of 2024 songs in India.  
