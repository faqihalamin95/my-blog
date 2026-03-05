---
title: Closing Phase 1 - Building My Data Engineering Foundation
summary: After publishing my “ Data Engineering Roadmap as a Data Science Student ”, I committed to executing the first phase. Phase 1 was designed as a foundation phase, and now it has reached a natural closing point.
date: 2025-12-22
authors:
  - me
tags:
  - Blog
  - Data Engineering
  - Career Journey
image:
  filename: featured.jpg
  caption: 'Image credit: Photo by [**Philippe Surber**](https://unsplash.com/@surber) on [**Unsplash**](https://unsplash.com)'
---

**After publishing my *“ Data Engineering Roadmap as a Data Science Student ”*, I committed to executing the first phase. Phase 1 was designed as a foundation phase, and now it has reached a natural closing point.**

### This post serves two purposes:

* To document what I actually learned from Phase 1
    
* To formally close the foundation phase and transition into **Phase 2: Local ETL & Data Modeling**
    

---

## What Phase 1 Was About

Phase 1 focused on **core fundamentals**, not speed or scale.

The objective was simple but strict:

> Understand how data moves from raw form into a structured, queryable system.

### Courses Completed

During this phase, I completed:

* **Cisco – Python Essentials 1**
    
* **Cisco – Linux Unhatched**
    
* **Codecademy – Learn SQL**
    
* **Codedex – Learn Git & GitHub**
    

These courses provided syntax and tooling familiarity, but the real learning happened when everything had to work together inside a single project.

---

## Phase 1 Project: Movie Data Pipeline & Foundation Analysis

### Project Overview

This project was part of the **Data Engineer Foundation Phase (Months 1–2)**.

The goal was to build a **local ETL pipeline** that processes raw movie datasets into a structured SQLite database.

The complete project, including scripts and documentation, is available here:  
[https://github.com/faqihalamin95/movie-genre-analysis](https://github.com/faqihalamin95/movie-genre-analysis)

Rather than focusing on advanced analytics, this project emphasized the **engineering workflow**:

* Cleaning semi-structured CSV data
    
* Handling multi-valued attributes
    
* Designing a relational schema
    
* Ensuring correct data types for SQL storage
    

### Core Objectives

* **Data Cleaning**  
    Automated preprocessing using pandas
    
* **Schema Design**  
    Designing a flat relational table in SQLite
    
* **ETL Workflow**  
    Raw CSV → clean CSV → SQLite database → query-ready output
    

This project intentionally stayed local and simple, because the goal was correctness and reproducibility, not scale.

It sounded simple and easy, right? At least on paper.  
In reality, it was neither (well, for a beginner, obviously).

---

## Key Reflections from Phase 1 (Movie Project Only)

### 1\. Python → Data Engineer Is Not a Straight Line

Turning fundamental Python skills into something usable for data engineering turned out to be harder than expected.

The gaps became obvious pretty quickly:

* Dataframe operations that go beyond the basics (`explode`, `groupby`, explicit type casting)
    
* Writing scripts that can be rerun, not just notebooks that worked once
    
* Connecting Python workflows to a real relational database
    

This project made one thing clear: knowing Python syntax is only the starting point.

---

### 2\. SQL Feels Different Inside a Real Database

SQL felt comfortable while taking courses. It felt very different once I had to run it against an actual database.

The main challenges were:

* Writing queries that matched the *real* table schema
    
* Getting joins and aggregations right
    
* Making sure data types didn’t break during table creation or insertion
    

Most problems weren’t about SQL syntax. They came from wrong assumptions about the schema.

---

### 3\. Schema Design Controls Everything Downstream

If there’s one lesson that keeps repeating itself, it’s this: schema decisions matter early.

Some hard-earned lessons:

* Multi-valued attributes (like movie genres) need deliberate handling
    
* Table structure should reflect how the data will be queried later
    
* Poor schema choices lead to failed imports, mismatched data, or misleading results
    

Once data is loaded, the schema becomes the single source of truth (no negotiations).

---

### 4\. GitHub Is Part of the Engineering Workflow

Version control wasn’t a separate task in this project. It was part of the pipeline.

A few practical takeaways:

* Start repositories clean and minimal
    
* Push code only after the structure is reasonably stable
    
* Use `.gitignore` to keep databases, cache files, and large data out of the repo
    

A clean repository makes everything else easier to maintain and extend.

---

### 5\. Debugging Is Part of the Job Description

Errors showed up everywhere:

* CSV import failures
    
* SQLite CLI and PATH issues
    
* Data type mismatches during inserts
    

Instead of treating these as failures, the project reinforced a more practical mindset:  
Break the problem down step by step.

**Python → CSV → Transform → SQL → Query**

---

### 6\. Documentation Completes the Pipeline

Documentation wasn’t optional (it was necessary).

Good documentation:

* Makes pipelines reproducible
    
* Speeds up debugging
    
* Turns learning projects into reusable references
    

README files and clear project structure are part of the engineering work, not an afterthought.

---

## Phase 1 Summary

Phase 1 was never about mastering every tool or memorizing syntax.

It was about understanding how things connect:

* How data moves from raw files into something structured and queryable
    
* Why schema decisions quietly affect everything downstream
    
* Why small habits (naming, structure, and documentation) matter more than they first appear
    

More importantly, Phase 1 helped shift my mindset. From learning Python, SQL, and Git as separate pieces to seeing how they come together in a single, simple pipeline.

With that foundation in place, Phase 1 feels complete.

---

## What’s Next → Move to Phase 2

Phase 2 builds on the same ideas from Phase 1, but with slightly more structure and intention.

The focus will move beyond a single, simple pipeline into:

* Working with local databases more deliberately
    
* Applying basic data modeling and normalization concepts
    
* Building simple, repeatable local ETL flows
    
* Introducing light automation using scripts and the command line
    

This phase is still very much about learning by doing, experimenting, breaking things, and understanding why certain patterns work better than others.

At the end of Phase 2, I’ll write a reflection post reviewing what worked, what broke, and what I actually learned from building these pipelines.