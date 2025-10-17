🧾 RECON Web App Architecture
📖 Overview

The RECON Web Application is designed to automate and streamline the reconciliation process between multiple financial data sources such as CBS (Core Banking System), Switch, and NPCI.
It ensures accurate matching, reporting, and compliance through an end-to-end data processing pipeline — from ingestion to reconciliation and reporting.

🏗️ System Architecture

The system follows a modular, layered architecture, enabling scalability, automation, and high data accuracy.

🧩 Architecture Layers

NPCI / Bank / RBI Feeds (Source Layer)

Ingests transaction data from multiple external sources.

Includes daily settlements, CBS data, switch logs, and NPCI feeds.

Data Ingestion Layer

Automates fetching of raw input data from different formats and locations.

Standardizes input data for uniform downstream processing.

Staging Store

Acts as a temporary object storage for unprocessed data.

Provides isolation before ETL operations begin.

Validation & ETL Layer

Performs data cleaning, schema validation, deduplication, and data enrichment.

Converts raw data into structured, standardized records.

Processed Data Layer

Organizes data into Valid and Invalid buckets.

Enables error tracking and quality control.

Database Layer

Stores validated and reconciled datasets.

Supports querying, reporting, and auditing.

Reconciliation Engine

Core logic that compares CBS vs Switch vs NPCI transaction data.

Identifies matched, unmatched, and exception transactions.

TTUM Generation

Generates accounting entries for reversals and settlements.

Outputs standardized TTUM files for upload to CBS or accounting systems.

Reporting & Dashboards

Provides visualization of reconciliation results, exceptions, and operational trends.

Enables business and audit reporting.

Archival / Backup (Optional)

Archives processed data, logs, and reports for regulatory compliance and historical audit.
