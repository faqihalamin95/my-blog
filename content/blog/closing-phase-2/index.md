---
title: Closing Phase 2 - Why My First End-to-End Pipeline Broke Until I Learned Data Modeling
summary: Phase 2 of my data engineering journey was all about putting theory into practice by building an end-to-end data pipeline project while learning why architectural decisions matter (not just how).
date: 2026-02-04
authors:
  - me
tags:
  - Blog
  - Data Engineering
  - Career Journey
image:
  filename: featured.jpg
  caption: 'Image credit: Photo by [**Michele De Pascalis**](https://unsplash.com/@micheledp93) on [**Unsplash**](https://unsplash.com)'
---

**Phase 2 of my data engineering journey was all about putting theory into practice by building an end-to-end data pipeline project while learning why architectural decisions matter (not just how).**

## What I Built: E-commerce Data Pipeline

In Phase 1, I laid my foundation with core skills. In Phase 2, I applied them to a real pipeline: transforming raw e-commerce data into analytics-ready tables that simulate real-world workflows.

For this Phase, I developed an **end-to-end pipeline project** hosted on GitHub: 
👉 [**E-Commerce Data Warehouse Pipeline**](https://github.com/faqihalamin95/ecommerce-data-pipeline)

This pipeline ingests raw e-commerce datasets, performs layered transformations (raw → staging → foundation → marts), and applies basic quality checks.

### Core components of the project

* **Ingestion layer:** Reads raw CSV data and structures it into initial tables.
* **Staging layer:** Cleans and standardizes the ingested data.
* **Foundation layer:** Builds fact and dimension tables using a **star schema**.
* **Marts Layer:** Produces analytics-ready tables designed for user consumption.
* **Basic quality checks:** Ensures non-empty tables and referential integrity.
* **Orchestration:** Local pipeline steps coordinated with a Makefile.

In short, this project simulates **core data engineering workflow patterns** from ingestion through transformation to marts, a foundational pattern in real industry pipelines.

---

## What I Learned During Phase 2

### Learning by Doing Works - But Only Up to a Point

At the beginning of Phase 2, my learning approach was familiar: reading documentation, following tutorials, and trying to understand concepts in isolation. But fairly quickly, I realized that this wasn’t enough. I learn best when I can **immediately apply what I’m studying.**

Instead of waiting until all the theory felt "complete," I started building a simple data pipeline template while learning. The idea was straightforward: build something minimal first, then iterate as my understanding improved.

This approach helped concepts stick faster. Abstract ideas around ingestion, transformation, and orchestration became easier to grasp once they were attached to real code and a real project.

**However, this approach also exposed a limitation.**

---

### A Pipeline Can Grow Faster Than Your Design

As I kept adding features and improvements, the pipeline started to grow without a clear boundary. New ideas, tweaks, and adjustments kept piling up. What began as a simple learning template slowly turned into something more complex than originally planned.

At that point, the technical difficulty never really went away, and the lack of structure made it worse. It was becoming harder to reason about:

* *What belongs in which layer?*
* *Which transformations are essential, and which are just experiments?*
* *What assumptions does this pipeline actually rely on?*

This was the moment where I realized that **building first without a clear design only works for a while.**

---

### Discovering Data Modeling

In my roadmap, there was a section called **data modeling**. At the time, I realized I didn’t actually understand what that meant in practice.

So I started searching for explanations and references, and that’s how I found **Kimball’s *The Data Warehouse Toolkit***. This book was a great discovery (*chef’s kiss*). I read Chapter 1 to Chapter 3, including the Retail Sales case, to understand how analytical systems are supposed to be designed from the ground up.

**That was the turning point.**

Instead of thinking in terms of scripts and transformations, I started thinking in terms of:

* What the **data represents**.
* The **grain** of each table.
* The role of **facts and dimensions**.
* How downstream consumers are expected to use the data.

For the first time, the pipeline had a conceptual backbone.

---

### Architecture First, Then Code

Once I understood the importance of data modeling, I shifted my focus to **pipeline architecture** and **explicit design decisions** before continuing implementation.

I defined the responsibilities of each layer, clarified what assumptions were allowed, and documented these decisions as a **design contract**. This wasn’t about making the system more advanced; it was about making it *intentional*.

The code itself was still difficult. That didn’t magically disappear. But the difference was this:

**Without architecture, I was coding without direction. With architecture, code became a tool to realize the design, not something that dictated it.**

Instead of asking “what should I try next?”, I could ask:
* *Does this align with the architecture?*
* *Does this belong in this layer?*
* *Is this complexity actually needed?*

---

### Clear Architecture Doesn’t Remove Difficulty - It Removes Confusion

A clear architecture didn’t make the work easy. The code was still hard. Debugging still took time. Progress was still slow at moments.

**What changed was not the level of difficulty, but the sense of direction.**

Before, problems felt messy because I wasn’t sure whether they came from the data, the logic, or the overall design. After defining the architecture, even hard problems became easier to locate. I knew where an issue belonged and what it affected.

I still struggled, but I wasn’t wandering. Every change had a reason, and every decision had a boundary.

---

### The Core Lesson of Phase 2

Phase 2 reinforced one fundamental idea for me:

> [!NOTE]
> **Architecture defines the destination. Code helps you to move toward it.**

Without a clear architecture, writing code feels like patchwork, you keep fixing things locally without knowing whether you’re getting closer to the right system. With architecture in place, the code may still be heavy, but at least it moves in a direction you understand.

**This is the lesson I’ll carry forward into the next phases.**

---

## What’s Next → Move to Phase 3

With Phase 2 complete, my focus moves to **Phase 3: Cloud and Pipelines**, a unified step toward cloud platforms, infrastructure patterns, and production-oriented data workflows.

This phase will cover three tightly connected areas:

1.  **Cloud foundations:** Object storage, IAM, networking basics, and containerized environments.
2.  **Serverless & IaC:** Infrastructure as Code to provision and manage resources in a reproducible way.
3.  **Pipeline orchestration:** Connecting ingestion, transformation, and analytics workflows into systems that resemble real production pipelines.

Instead of committing to a single tool stack, I plan to follow a **dual-track strategy**:

* **An open-source based stack:** Prioritizing flexibility and cost efficiency.
* **A modern managed stack:** Using cloud-native services and tools such as Databricks.

The goal of this approach is adaptability. By understanding both open-source and managed ecosystems, I want to stay flexible, whether that means adopting new tools in the future or choosing cost-efficient solutions depending on organizational needs.