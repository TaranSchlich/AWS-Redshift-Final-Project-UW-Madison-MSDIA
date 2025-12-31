# MCPD Crime Data Warehouse – (Part 1)  

**By: Taran Schlichtmann** 

**Date: 12/08/2025**

Acting as a data consultant for the Metro City Police Department (MCPD), I designed and populated a cloud‑native data warehouse using Amazon Redshift to centralize and analyze nearly 8 million criminal incident records. The goal was to answer key questions about crime trends and provide MCPD with a scalable, reliable reporting foundation.

1. Building a cloud‑native data warehouse in **Amazon Redshift** to analyze nearly 8 million crime records for the Metro City Police Department (MCPD).  
2. Creating an **AWS cost estimate** for storing and processing MCPD’s criminal incident data using S3 and Redshift, including support plan costs.

---

# Part 1 – AWS Redshift Crime Data Warehouse

## Project Overview

The objectives of Part 1 were to:

- Build a Redshift data warehouse in AWS  
- Load large‑scale crime data directly from S3  
- Execute analytical SQL queries to answer MCPD’s business questions  
- Export query results for submission  

This work supports MCPD’s goal of centralizing crime data for faster, more accurate reporting.

---

## AWS Services Utilized

### Amazon S3
- Crime data stored in: `s3://crime-reporting`
- Loaded directly into Redshift using COPY

### Amazon Redshift
- Region: Oregon  
- Cluster type: **Two-node dc2.large**  
- IAM Role: **LabRole**  
- Tasks completed:
  - Created crime reports table  
  - Loaded ~8 million records  
  - Executed analytical SQL queries  
  - Exported results to CSV  

---

## Key SQL Queries & Results

### Query #1 – Most Common Crime Types
Identified the top 5 crime categories.

**Top 3 Crime Categories:**
- Assault 3 & related offenses  
- Petit larceny  
- Harassment 2  

**Most common crime total:**  
**1,331,246**

---

### Query #2 – Felonies in Houses of Worship
Filtered felony crimes in:
- CHURCH  
- MOSQUE  
- SYNAGOGUE  
- OTHER HOUSE OF WORSHIP  

**Results:**  
- Synagogues: **1,021**  
- Mosques: **321**

---

### Query #3 – Crime Counts by Year (2010–2020)
Counted crimes by year using “Complaint From Date”.

**Selected Results:**  
- 2015: **478,831**  
- 2020: **412,221**

---

# Part 2 – AWS Cost Estimate

MCPD requested a cost estimate for storing and processing their criminal incident data in AWS using S3 and Redshift. The AWS Pricing Calculator was used to generate the estimate.

---

## Cost Estimate Configuration

### Region
- **us-east-1 (N. Virginia)**

### Amazon S3 (Data Lake)
- **75 TB per month** of S3 Standard storage  
- Data transfer costs **excluded**  

### Amazon Redshift (Data Warehouse)
- **4-node cluster**  
- Instance type: **ra3.xlplus**  
- **100% utilization**  
- On‑Demand pricing  

### AWS Support Plan
- MCPD requires:
  - Self-service support  
  - High-severity response time: **< 4 hours**  
- Selected plan: **Business Support** (lowest-cost option meeting requirements)

---

## Cost Estimate Results

### 1. Monthly Cloud Architecture Cost (S3 + Redshift)
**4,911.92**

### 2. Monthly AWS Support Cost
**491.19**

### 3. Final Annual Cost (Including Support)
**64,837.32**

---

## Tools & Technologies

- Amazon Redshift  
- Amazon S3  
- AWS Pricing Calculator  
- SQL (DDL, DML, COPY)  
- Cloud cost modeling  
- Data warehousing concepts  

---

## Skills Demonstrated

- Cloud data warehouse design  
- Large-scale data ingestion  
- Analytical SQL querying  
- AWS cost estimation  
- Understanding of cloud pricing models  
- AWS resource planning and budgeting  

---

## Summary

This final project delivered:

- A fully functional Redshift data warehouse containing nearly 8 million crime records  
- Analytical insights into crime types, felony locations, and yearly crime trends  
- A complete AWS cost estimate for MCPD’s cloud architecture, including support costs  

Together, these deliverables provide MCPD with a scalable, centralized, and cost‑transparent cloud solution for ongoing crime analysis and reporting.
