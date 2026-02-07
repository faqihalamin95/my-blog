---
title: My Data Engineering Roadmap as a Data Science Student
summary: After sharing my motivation for pursuing Data Engineering, I wanted to put that passion into a structured plan. Something that connects what I learn in university, online courses, and real-world practice.
date: 2025-10-19
authors:
  - me
tags:
  - Roadmap
  - Data Engineer
  - Learning Journey
  - SQL
  - Python
cover:
  image: "cover.jpg"
image:
  filename: featured.jpg
  caption: "Image credit: Photo by [**Wes Hicks**](https://unsplash.com/@sickhews) on [**Unsplash**](https://unsplash.com)"
content_meta:
  trending: false
featured: true
---

 **After sharing my motivation for pursuing Data Engineering, I wanted to put that passion into a structured plan. Something that connects what I learn in university, online courses, and real-world practice.**

---

## Overview

I designed this roadmap to align with eight semesters of my Data Science degree, combining theory from coursework and technical depth from self-learning. Each semester focuses on a specific layer of data engineering, from local experimentation to production-grade cloud systems.

This roadmap isn’t just a checklist, it’s a direction map. Flexible enough to adapt as I grow, but clear enough to keep me focused.

As a Data Science student, my goal is to *build solid* ***foundations first***, ***automate second***, and ***scale last***.

---

## Roadmap Table

### Foundation (Phase 1-2) ✅

| Phase | Phase 1 - Foundation Basics (2 months) | Phase 2 - Local ETL & Modeling (2 months) |
| --- | --- | --- |
| **Status** | ✅ Completed | ✅ Completed |
| **Main Focus** | Python & SQL Fundamentals | Databases & Local Data Handling |
| **Learning Resources** | Cisco - (Python Essentials 1, Linux Unhatched), Codecademy - Learn SQL, Codedex - Learn Git & Github | Databricks Academy, pandas docs, PostgreSQL tutorial, The Data Warehouse Toolkit (3rd Edition) by Ralph Kimball |
| **Key Skill & Topics** | Basic statistics, Python basics, SQL fundamentals, Intro to Git & Linux | CSV/JSON ingestion, Pandas ETL, Bash automation, Data modeling, Normalization, Basic ETL patterns, Makefile-based orchestration |
| **Tools / Platform** | Python, Jupyter Notebook, GitHub, Linux Shell, PostgreSQL/MySQL | PostgreSQL/MySQL, GitHub, Pandas & NumPy, Bash CLI |
| **Project / Portfolio Output** | **Project 1**: [**Movie Data ETL Pipeline**](https://datadonut.netlify.app/projects/movie-data-etl-pipeline/) | **Project 2:** [**E-commerce Data Pipeline**](https://datadonut.netlify.app/projects/ecommerce-data-pipeline/) |

---

### Cloud (Phase 3-4) ⏳

| Phase | Phase 3 - Cloud Infrastructure & Serverless Pipelines (4 months) | Phase 4 - Big Data & Advanced Orchestration (5 months) |
| --- | --- | --- |
| **Status** | ⏳ In Progress | 🗓️ Planned |
| **Main Focus** | Cloud infra, Containerized workloads, Event-driven pipelines | Big data, Cloud ETL & Basic streaming |
| **Learning Resources** |  |  |
| **Key Skill & Topics** | IAM (least privilege), S3 (raw/staging zones), VPC & networking basics, Dockerized Python apps, Terraform IaC, Lambda execution model, SQS-based decoupling, Idempotent ETL, CI-ready infra | Spark DataFrames, Distributed processing, Glue ETL workflows, Redshift integration, dbt SQL modeling, Airflow DAG orchestration, Data quality frameworks |
| **Tools / Platform** | AWS S3, IAM, VPC, Docker, Python, Terraform, AWS Lambda, SQS, GitHub Actions (basic) | Apache Spark (PySpark), AWS Glue, Redshift, Airflow/Step Functions, Kafka/Kinesis, dbt |
| **Project / Portfolio Output** | **Project 3:** End-to-end cloud data pipeline (Docker + Lambda) deployed fully via Terraform | **Project 4:** Cloud ETL, raw → Glue → Redshift/S3 + basic streaming ingestion + data quality checks |

---

### Advanced (Phase 5-6) 🗓️

| Phase | Phase 5 - DevOps & Production (4 months) | Phase 6 - Lakehouse & Capstone (8 months) |
| --- | --- | --- |
| **Status** | 🗓️ Planned | 🗓️ Planned |
| **Main Focus** | CI/CD, Observability & Container orchestration | Lakehouse, Advanced streaming & ML integration |
| **Learning Resources** |  |  |
| **Key Skill & Topics** | Infrastructure automation, Secret management, GitHub Actions pipelines, Test workflows, Monitoring & logging, Container orchestration (K8s) | Delta Lake/Hudi, ACID ingestion, Spark optimization, Incremental loads, Real-time streaming (Flink/Spark Streaming), Data governance, Feature stores, ML pipeline integration |
| **Tools / Platform** | Terraform, GitHub Actions, CloudWatch, Docker, Kubernetes | Databricks, Delta Lake, Flink/Spark Streaming, Great Expectations, MLflow, Terraform, Airflow, Power BI/Metabase |
| **Project / Portfolio Output** | **Project 5:** Production-grade ETL with CI/CD, tests, monitoring, containerized deployment | **Capstone:** Full data platform — ingestion → processing → catalog → quality → dashboard + ML pipeline |

---

## How I’ll Use This Roadmap

* **As a compass**, to keep me aligned with my long-term goal: becoming a professional Data Engineer.
    
* **As a progress tracker**, to document what I’ve learned and what still needs improvement.
    
* **As content inspiration**, for future blog posts and portfolio updates.
    

This roadmap isn’t final, it’s something I’ll refine every semester as I gain experience through university projects, certifications, and my ongoing work in the data industry.

---

## What’s Next

Phase 1 and Phase 2 are **completed**, covering foundational skills and local ETL workflows—from basic Python and SQL to structured data modeling and reproducible pipelines.

I am currently **in progress with Phase 3**, focusing on **Cloud Infrastructure & Serverless Pipelines**. This phase marks the transition from local environments to cloud-native systems, emphasizing infrastructure-as-code, containerized workloads, and event-driven data pipelines.

At the end of Phase 3, I plan to document key learnings around cloud infrastructure design, deployment trade-offs, and lessons learned when moving ETL workloads into a serverless environment.

---

## **Roadmap Update Log**

**v2.2 Phase Progress & Vertical Layout Update (February 2026)**

* Roadmap structure adjusted: Phase 3 expanded to include production-ready orchestration foundations (total phases reduced to 6).
* Updated roadmap status: Phase 2 marked as Completed, Phase 3 marked as In Progress.
* Refactored roadmap tables into a vertical layout for better readability in blog and document formats.
* Updated *What’s Next* section to reflect current execution focus on cloud infrastructure.

**v2.1 Phase 2 Learning Resources Update (December 2025)**

* Changed and refined Phase 1 status and documentation.
* Added Phase 2 learning resources.
* Updated *What’s Next* section.  

**v2.0 Major Revision (December 2025)**

* Roadmap structure changed: semester-based → phase-based (7 phases).
* Cloud section updated: combined Cloud Foundations & Serverless Pipelines.
* Big Data phase revised: PySpark, dbt, and Airflow integrated into a single project.
* Added Workload Management & Burnout Prevention guidance.
* Capstone scope clarified: full data platform + ML integration.
    
**v1.1 Tooling Update (November 2025)**

* Introduced Terraform basics for early IaC exposure. 
* Added Docker containerization in Phase 3.
    

**v1.0 Initial Structure (October 2025)**

* First version of the roadmap published.
* Added foundation milestones and basic Python/SQL projects.