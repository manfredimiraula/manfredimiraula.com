---
layout: project
vimeoId: 
title: 💬 Building an Internal LLM Chatbot with FastAPI and OpenSearch
image: "assets/projects/20250721/modernizing_content_synchronization_with_azure_pipeline.webp"
read_time: true
show_date: true
category: Services & Projects
description: Built a secure, private chatbot using GPT-4, OpenSearch, and FastAPI to help an HRTech startup automate internal knowledge sharing in under 2 months.
author: Manfredi Miraula
tags:
  - internal chatbot architecture
  - private GPT chatbot
  - FastAPI OpenAI integration
  - OpenSearch vector search
  - DynamoDB session tracking
  - AWS ECS chatbot deployment
  - LLM startup use case
  - internal knowledge automation
  - GPT-4 OpenSearch example
  - self-hosted chatbot AWS


---
**Built a secure, private chatbot using GPT-4, OpenSearch, and FastAPI to help an HRTech startup automate internal knowledge sharing in under 2 months**

# Project Summary 🧩 

In fast-growing startups, internal knowledge tends to live in silos—shared folders, chat threads, Notion docs, or the minds of a few key people. At this HRTech scale-up, I partnered directly with the CTO/founder to solve a recurring pain: teams wasting time looking for information that already existed.

The goal: build a lightweight, private, LLM-powered internal chatbot that could surface answers instantly from curated internal content.

## Startup Context: HRTech at Scale, Bootstrapped 🧪 

This company operates in the HRTech space, helping organizations streamline hiring and workforce management. As a bootstrapped business, every build decision needed to deliver real value fast — with low overhead and zero tolerance for fluff.

I worked hands-on with the CTO to:

    Define an MVP architecture that could scale

    Keep infra lean (AWS-native services, no overengineering)

    Focus on embedding high-signal sources for real utility

This was not a vanity chatbot — it became a core internal tool used daily by operations, product, and support teams.

## The Challenge ❗

    Internal documents were well-organized but scattered across systems

    Support and ops teams were regularly asking repeat questions

    Prior attempts at internal knowledge bases were static and underused

    Security and data privacy were critical (no SaaS plugins)

The key need: a fast, secure, self-hosted AI assistant that could understand questions and return meaningful answers based on curated sources.

## The Solution Delivered 🛠 

I designed and implemented an internal chatbot using:

    FastAPI as the backend interface

    OpenAI (GPT-4) for natural language understanding and answer generation

    OpenSearch for vector-based document retrieval

    DynamoDB for metadata and session tracking

    AWS ECS + Docker for fully containerized deployment

The system allowed the team to upload key documents, which were automatically chunked, embedded, and indexed in OpenSearch. Employees could then ask natural language questions and receive context-rich answers from those internal sources — all within a secure private environment.

## Architecture Overview 🧱

```css
[Curated Docs] --> [Chunking + Embedding] --> [OpenSearch Index]
                                          ↓
                                     [FastAPI API]
                                          ↓
                               [OpenAI (GPT-4) Completion]
                                          ↓
                                   [Web Chat UI (internal)]

    Infra: AWS ECS (Docker), OpenSearch, DynamoDB

    Backend: Python + FastAPI

    LLM: OpenAI API (GPT-4)

    Security: Private deployment, no SaaS storage, API keys locked to VPC

    Flexibility: Easily extendable to new document types or user roles
```

## Impact 📈 

    Reduced Slack back-and-forth and repetitive questions

    Enabled non-technical teams to self-serve information

    Became a trusted internal tool with strong adoption across ops and product

    Delivered in under 4 weeks from first sync to deployment

## How This Reflects My Services 💡

This project highlights my ability to:

    Translate vague business needs into working AI tools

    Own the full stack: architecture → LLM integration → deployment

    Ship fast in resource-constrained environments

If you’re a startup leader looking to productize internal knowledge, automate operations, or ship LLM-powered tools fast, I can help you build what matters — without the bloat.

Would you like me to:

    Create a technical diagram for this one too?

    Write a short teaser for this case (for your homepage or LinkedIn)?

    Move on to article #3 (FreshDesk ticket automation)?

Let me know and I’ll keep the momentum going.