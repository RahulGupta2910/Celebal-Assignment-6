# Celebal-Assignment-6

## 🌐 Azure Data Factory Projects
This repository contains five end-to-end Azure Data Factory (ADF) projects that demonstrate various data integration and automation scenarios using Azure services. Each project showcases a real-world use case involving on-premises data, FTP/SFTP extraction, incremental loading, custom scheduling, and retry logic for fault tolerance.

## 📁 Projects Overview
1. Self-hosted Integration Runtime (SHIR) for Local to Cloud Data Flow
Objective: Extract data securely from an on-premises/local SQL Server and load it into an Azure SQL Database.

     Key Features:
    
       Self-hosted Integration Runtime (SHIR) setup on a local machine.
       
       Secure data movement using encrypted connection.
       
       Pipeline to read from local SQL Server and load to Azure SQL Database.
       
       Enables cloud-based analytics for on-prem data.

2. FTP/SFTP Data Extraction to Azure
Objective: Connect to an FTP/SFTP server, extract files (e.g., .csv, .json), and load them into Azure SQL Database.

Key Features:

   SFTP/FTP server setup and connectivity via ADF linked service.
   
   Pipeline to read and process files into structured format.
   
   Integration with external partners/systems via file sharing.
   
   Option to parameterize file paths and dynamically read files.

3. Incremental Load with Daily Automation
Objective: Build a pipeline that performs daily incremental loads from source to Azure SQL using watermarking.

Key Features:

   Watermark column logic to detect new/changed records.
   
   Lookup and variable activities to maintain watermark state.
   
   Data copy only for delta records, optimizing resources.
   
   Triggered daily via time-based schedule.

4. Trigger Pipeline on Last Saturday of the Month
Objective: Automate a pipeline that runs only on the last Saturday of every month.

Key Features:
   
   Custom dynamic expression using utcNow() and addDays() to detect last Saturday.
   
   Pipeline trigger with conditional logic.
   
   Ideal for batch reporting, monthly snapshots, or financial roll-ups.

5. Graceful Retry Logic for Transient Failures
Objective: Implement retry mechanisms for temporary failures during data movement or transformation.

Key Features:

   Wait activity to introduce delay before retry.
   
   Error handling using ifCondition and setVariable.
   
   Enhances reliability and fault tolerance of pipelines.
   
   Helpful in scenarios with intermittent network or service errors.

## 🧰 Technologies Used
Azure Data Factory (V2)

Azure SQL Database

Self-hosted Integration Runtime

FTP/SFTP server (tested with WinSCP/FileZilla)

JSON & CSV datasets

Parameterized pipelines and triggers

Azure Monitor for logging and alerts

🚀 How to Use
Each project folder contains:

ADF pipeline JSON templates (ARM or export format)

Linked service definitions

Dataset configurations

You can import these into your own ADF instance using:

Azure Portal > Data Factory > Manage > ARM Template > Import ARM Template
