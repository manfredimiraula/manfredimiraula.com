---
layout: project
vimeoId: 
title: 🚀 Modernizing Content Synchronization with Azure ETL Pipelines
image: "assets/projects/20250721/modernizing_content_synchronization_with_azure_pipeline.webp"
read_time: true
show_date: true
category: Services & Projects
description: How I built a scalable, containerized ETL solution to sync marketing assets across content management systems.
author: Manfredi Miraula
tags:
  - Azure ETL pipeline
  - CMS synchronization
  - Azure Functions ETL
  - Azure Blob Storage use case
  - CosmosDB metadata tracking
  - Service Bus orchestration
  - cloud-native ETL architecture
  - enterprise content management automation
  - python azure microservices
  - dockerized ETL pipeline

---
**How we designed, implemented and delivered a scalable, containerized ETL solution to sync marketing assets across** 

# Project Summary 🧩
A global marketing team needed to automatically synchronize high-value content—presentation decks, PDFs, and promotional materials—between two enterprise content management systems. Manual handling was error-prone and time-consuming. I was brought in to design and deliver a robust, cloud-native ETL pipeline on Azure that would automate the end-to-end process — with traceability, error handling, and performance baked in.

## Industry Context: Pharma Commercial Operations 🏥 
This solution was delivered within a top-tier European pharmaceutical company, specifically in their Commercial division. While the scope didn’t fall under GxP (Good Practice) compliance, there was a strong emphasis on data governance, auditability, and content integrity — especially due to regulatory scrutiny around promotional materials and marketing claims.

The pipeline had to respect strict boundaries around:
  - Access control and traceability
  - Versioned storage of source and destination files
  - Audit logs for all transformations and transfers

This experience is part of my broader capability to deliver enterprise-grade data solutions in industries where compliance, security, and governance are non-negotiable.

## The Challenge ❗
The client was managing thousands of content files across two different platforms, with inconsistent update cycles and complex metadata tagging. Their existing process relied heavily on manual exports and uploads, creating operational overhead and compliance risks.

The main challenges:
  - Variability in file size and format (some >3GB)
  - Need for resilience in file transfer and transformation
  - Cloud-native architecture with CI/CD and version control
  - Fully automated execution, yet traceable and debuggable

## The Solution I Delivered 🛠 

I designed a microservice-oriented ETL pipeline, fully deployed in Azure, using:
  - Azure Functions for modular transformation logic
  - Azure Service Bus for reliable decoupled orchestration
  - CosmosDB to track metadata and sync status
  - Azure Blob Storage to store and stream large marketing files
  - Azure Container Registry and Docker for version control and reproducibility

The entire pipeline is event-driven, fault-tolerant, and modular — making it easy to extend or integrate into other systems down the road.

## Architecture Highlights 🧱 

```css
[CMS A] --> [Cron Job Trigger] --> [Azure Function]
                       ↓
               [Azure Service Bus]
                       ↓
             [Transformation Function]
                       ↓
                [CosmosDB + Blob]
                       ↓
                    [CMS B]

```

- Language & Frameworks: Python, Docker
- Infra: Azure Functions, Storage Account, CosmosDB, Service Bus
- CI/CD: Azure Container Registry for deployment versioning
- Scalability: Stateless functions, message queue architecture
- Resilience: Retry logic, isolated failures, observable state in CosmosDB

## Impact 📈 

  - Removed manual work. The content synchronization became an automated process!
  - Reduced sync lag from days to minutes
  - Eliminated manual errors and compliance gaps
  - Gave marketing leadership confidence in asset consistency across platforms
  - Provided a scalable, containerized foundation for future automation

## How This Reflects My Services 💡 

This project is a great example of my approach to end-to-end product deployment:
  - I don’t just write code — I design resilient systems.
  - I handle the full stack, from infrastructure to logic to delivery.
  - I lead with clarity, aligning technical choices with business needs.

If you're looking to automate, modernize, or scale your data and AI workflows, I can help architect and deliver cloud-native systems that just work.