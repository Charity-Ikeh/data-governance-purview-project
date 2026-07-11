# Enterprise Data Governance Project — Microsoft Purview Implementation

## Status
🚧 In Progress — build started July 2026

## Overview
This project demonstrates the practical implementation of enterprise data governance using Microsoft Purview, applied to a representative banking transaction dataset. It covers the core disciplines of modern data governance: data cataloguing, classification, business glossary development, data ownership and stewardship definition, and data lineage documentation.

The project reflects how data governance functions operate in regulated environments such as banking and financial services, where trust, traceability, and accountability over data are business-critical, not optional.

## Objectives
- Establish a governed data catalog for a banking transaction dataset using Microsoft Purview
- Apply data classification and sensitivity labelling aligned with UK GDPR and data protection principles
- Define a business glossary of Critical Data Elements relevant to banking operations
- Assign and document data ownership and stewardship roles
- Document end-to-end data lineage to support audit readiness and regulatory traceability
- Demonstrate the operational, day-to-day discipline of data governance practice, not just theoretical frameworks

## Dataset
Banking transaction dataset (NIBSS dataset, 20,000 records), covering customer transaction data across multiple channels — used here purely as the subject of governance activity: cataloguing, classification, glossary definition, and lineage mapping.

## Governance Framework Applied

### 1. Data Ownership & Stewardship
Defining clear data ownership across the dataset's domains, identifying data stewards responsible for data quality and definition accuracy, and establishing accountability structures consistent with DAMA-DMBOK principles.

### 2. Data Cataloguing
Registering the dataset within Microsoft Purview's Data Map, scanning to surface schema, structure, and metadata, and establishing a searchable, governed catalog entry.

### 3. Data Classification & Sensitivity Labelling
Applying classification labels to fields containing customer-identifiable and financially sensitive information, in line with UK GDPR data protection principles and standard KYC data handling practice.

### 4. Business Glossary
Defining a business glossary of Critical Data Elements — including transaction type, customer identifier, account reference, transaction value, and fraud indicator fields — establishing shared, unambiguous definitions between business and technical stakeholders.

### 5. Data Lineage
Mapping the data's journey from source system through to its governed, catalogued state, capturing transformation points to support traceability and regulatory audit requirements.

### 6. Data Quality & Governance Standards
Applying data quality dimensions (completeness, accuracy, consistency, timeliness) as governance controls, consistent with practice in regulated banking environments.

## Why This Project
Data governance depends on practitioners who can operationalise policy: cataloguing data, defining shared business language, assigning accountability, and making data traceable and trustworthy. This project applies that discipline directly, using industry-standard tooling, to demonstrate practical, hands-on data governance capability beyond framework knowledge alone.

## Tools & Technologies
- **Microsoft Purview** — data cataloguing, classification, business glossary, lineage
- **DAMA-DMBOK principles** — governance framework alignment

## Methodology
This project follows a structured governance implementation approach: establishing the governance environment, cataloguing and classifying data, defining business terminology and ownership, and documenting lineage, mirroring the operating model used in enterprise data governance functions.

## About
Built as part of ongoing professional development in data governance, alongside data governance training through the Berkeley Data Strategists DMP Cohort.

---
**Charity Ikeh** | Data Governance & Data Quality Analyst |[https://www.linkedin.com/in/charityikeh/]
