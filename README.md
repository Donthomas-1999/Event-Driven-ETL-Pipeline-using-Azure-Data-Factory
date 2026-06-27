# Event-Driven ETL Pipeline using Azure Data Factory

## 📖 Overview

This project demonstrates the design and implementation of an **event-driven ETL (Extract, Transform, Load) pipeline** using Microsoft Azure services. The solution automatically processes CSV files uploaded to Azure Blob Storage, performs data transformation using Azure Data Factory Mapping Data Flows, and stores the cleaned data in a separate Blob Storage container.

The pipeline eliminates manual execution by leveraging Azure Storage Event Triggers, providing an automated and scalable cloud-based data engineering solution.

---

## 🎯 Project Objectives

- Build an end-to-end ETL pipeline using Azure Data Factory.
- Automate data ingestion using Azure Storage Event Triggers.
- Transform raw CSV data into analytics-ready datasets.
- Store processed data in a dedicated output container.
- Gain hands-on experience with cloud-native data engineering services.

---

## 🏗️ Solution Architecture

```text
CSV File Upload
        │
        ▼
Azure Blob Storage (raw-data)
        │
        ▼
Azure Storage Event Trigger
        │
        ▼
Azure Data Factory Pipeline
        │
        ▼
Mapping Data Flow
   • Source
   • Filter
   • Select
   • Derived Column
   • Sink
        │
        ▼
Azure Blob Storage (clean-sales)
```

## ⚙️ Technologies Used

- Microsoft Azure
- Azure Data Factory
- Azure Blob Storage
- Azure Event Grid
- Storage Event Trigger
- Mapping Data Flows
- CSV Dataset
- Azure Monitor

## 🔄 ETL Workflow

### Step 1 — Data Ingestion

A CSV file is uploaded into the **raw-data** Blob Storage container.

### Step 2 — Event Detection

Azure Event Grid detects the newly uploaded file and automatically triggers the Azure Data Factory pipeline.

### Step 3 — Data Extraction

Azure Data Factory reads the CSV file from the Blob Storage source.

### Step 4 — Data Transformation

The Mapping Data Flow performs:
- Filtering unnecessary records
- Selecting required columns
- Creating derived columns
- Preparing clean, analytics-ready data

### Step 5 — Data Loading

The transformed dataset is written into the **clean-sales** Blob Storage container.

### Step 6 — Monitoring

Pipeline execution, activity status, and data flow performance are monitored using Azure Data Factory Monitor.
