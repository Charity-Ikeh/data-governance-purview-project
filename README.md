# Enterprise Data Governance Project — Microsoft Purview Implementation

## Status
✅ Complete — Governance domain, business glossary, data cataloguing, and lineage documentation all finished. Built as hands-on practice with Microsoft Purview for data governance.

## Overview
This project shows practical, hands-on data governance work using Microsoft Purview, applied to a sample banking transaction dataset. It covers the core areas of data governance in practice: cataloguing data, defining a business glossary, assessing classification, assigning ownership, and documenting lineage.

The work reflects how data governance is actually carried out in regulated environments like banking, where knowing what your data means, who owns it, and where it came from isn't optional, it's part of doing the job properly.

## Objectives
- Set up a governed data catalog for a banking transaction dataset in Microsoft Purview
- Assess data classification against the dataset's actual fields, applying labels only where they genuinely fit
- Build a business glossary covering the key data elements used in banking operations
- Assign clear ownership at the governance domain level
- Document data lineage, including being honest about what could and couldn't be automated
- Show the day-to-day discipline of data governance work, not just the theory behind it

## Dataset
A sample of a banking transaction dataset (NIBSS dataset, 20,000 records originally), used here as the subject of governance work: cataloguing, glossary definition, classification review, and lineage documentation.

## Governance Work Carried Out

### 1. Data Ownership
Assigned ownership at the governance domain level in Microsoft Purview, so there's clear accountability for the domain's data assets, glossary terms, and definitions.

### 2. Data Cataloguing
Registered the dataset as a data source in Purview and ran a full scan, which detected and catalogued all 42 columns along with their data types.

### 3. Data Classification Review
Checked the dataset's fields against Purview's built-in classification options to see which, if any, genuinely applied. Rather than forcing a label onto a field just to have something there, fields like customer_id and transaction_id were assessed and correctly left unclassified, since they're internal, engineered identifiers, not the kind of real-world data (like an actual national insurance number or card number) that Purview's built-in classifiers are designed to catch. Knowing when not to apply a classification is as much a part of the job as knowing when to apply one.

### 4. Business Glossary
Built a glossary of 9 terms covering the key data elements in this dataset: transaction value, customer identifier, fraud flag, transaction type, account reference, transaction channel, transaction date, currency code, and beneficiary bank. Each term has a plain-English definition and an assigned owner.

### 5. Data Lineage
Documented how the data actually moved, from the original dataset through to being catalogued in Purview, since automated lineage tracking wasn't set up for this project (more on that below).

## Why I Did This Project
Data governance isn't just policy documents, it's the actual work of cataloguing data, agreeing on shared definitions, assigning ownership, and being able to trace where data came from. This project was about doing that work hands-on with real tooling, rather than just knowing the theory.

## Tools Used
- **Microsoft Purview** — data cataloguing, classification review, business glossary, lineage
- **Azure Blob Storage** — used as the data source connected to Purview for scanning
- **DAMA-DMBOK principles** — used as a general reference for governance practice

## How I Approached It
Set up the governance environment first, then worked through cataloguing and classification, built out the glossary and ownership, and finished with lineage documentation, roughly following how a governance function would actually be stood up in practice.

## Outcomes

**Governance domain and business glossary**
- Created and published a governance domain ("Banking Operations") in Microsoft Purview's Unified Catalog
- Built and published a business glossary of 9 terms covering the core banking transaction data elements
- Each term has a clear definition and an assigned owner

**Data source connection and scanning**
- Set up Azure Blob Storage and connected it to Purview as a registered data source
- Configured the access permissions (Storage Blob Data Reader role) needed for Purview to actually scan it
- Ran a full scan on the sample dataset, which correctly detected and catalogued all 42 columns and their data types

**Classification review**
- Checked Purview's built-in classifications against the dataset's actual fields
- Decided not to apply classifications that didn't genuinely match the data, since the sample's identifiers are engineered fields, not real-world PII patterns

See `/screenshots` for evidence of the published governance domain, glossary terms, and scanned data schema.

## Data Lineage

Automated lineage tracking in Purview needs a connected data pipeline (like Azure Data Factory) actively moving data between systems, which wasn't set up for this project. Instead, here's the actual journey of the data, documented manually:

1. **Source**: NIBSS banking transaction dataset (20,000 records), originally used in my `banking-operations-analytics` project
2. **Sampling**: Took a 200-row sample, keeping all the original columns and data types
3. **Storage**: Uploaded the sample to Azure Blob Storage (`charitypurviewstore` account, `banking-sample` container)
4. **Cataloguing**: Registered it as a data source in Purview and scanned it, which picked up the full schema across 42 columns

This is a common situation in real data governance work, documenting lineage by hand when the source systems aren't set up for automatic tracking yet.

## About
A hands-on data governance project built to demonstrate practical experience with Microsoft Purview, covering data cataloguing, business glossary development, classification review, and lineage documentation.

---
**Charity Ikeh** | Data Governance & Data Quality Analyst | [https://www.linkedin.com/in/charityikeh/]

---
**Charity Ikeh** | Data Governance & Data Quality Analyst | [https://www.linkedin.com/in/charityikeh/]
