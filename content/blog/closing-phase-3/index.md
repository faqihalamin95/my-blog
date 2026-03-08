---
title: Phase 3 - Moving from Local Data Pipelines to Cloud Analytics Engineering
summary: Phase 3 of my data engineering journey focused on moving beyond local experimentation and into a cloud-based analytics pipeline, while learning how to work within real-world constraints such as cost, operational complexity, and scope management.
date: 2026-03-07
authors:
  - me
tags:
  - Blog
  - Data Engineering
  - Career Journey
image:
  filename: featured.jpg
  caption: 'Image credit: Photo by [**Colin Watts**](https://unsplash.com/@colinwatts) on [**Unsplash**](https://unsplash.com)'
---

**Phase 3 of my data engineering journey focused on moving beyond local experimentation and into a cloud-based analytics pipeline, while learning how to work within real-world constraints such as cost, operational complexity, and scope management.**

## What I Built: SaaS Analytics Engineering Pipeline

After completing my earlier [e-commerce pipeline project](https://datadonut.netlify.app/blog/closing-phase-2/), I wanted to
explore a different analytical domain: **SaaS subscription analytics**.

Instead of focusing on dashboards or visualization, this project focused
on **building a structured analytics pipeline** that simulates
challenges commonly found in real SaaS systems.

For this phase, I developed a full project hosted on GitHub:

👉 [SaaS Analytics Pipeline](https://github.com/faqihalamin95/saas-simulation)

The pipeline simulates operational SaaS activity, ingests the generated
data into a warehouse, and transforms it into a structured dimensional
model suitable for analytics workloads.

### Core components of the project

-   **Synthetic SaaS data generator:** Python scripts simulate
    subscription, payment, and product usage events.
-   **Object storage layer:** Event data is stored in object storage
    before ingestion.
-   **Data warehouse:** Raw and transformed data are stored in
    Snowflake.
-   **Transformation framework:** Analytical models are built using dbt.
-   **Orchestration:** Apache Airflow coordinates ingestion,
    transformations, and tests.
-   **Monitoring:** Pipeline execution status is reported through
    Telegram alerts.

Together, these components simulate a **modern analytics engineering workflow**, from raw event ingestion to business-ready analytical
datasets.

------------------------------------------------------------------------

## What I Learned During Phase 3

### Building Pipelines Became More Familiar - But Memory Is Still a Bottleneck

By the time I reached this phase, building pipelines no longer felt
completely unfamiliar. I had already developed a rough mental model of
what a typical pipeline should include.

Certain patterns were starting to repeat:

-   layered transformations
-   explicit data models
-   data quality checks
-   reproducible execution

However, a new problem appeared: **I sometimes forgot things.**

Not the big ideas, but the smaller structural decisions that keep a
pipeline reliable. When working on complex systems, it is easy to
overlook details such as idempotency, raw data preservation, or
validation rules.

To reduce this cognitive overhead, I decided to create a **personal data engineering playbook**.

The playbook captures the core principles I want every pipeline to
follow:

1.  **System design discipline**
2.  **Pipelines must be idempotent**
3.  **Raw layers must remain immutable**
4.  **Every pipeline requires an explicit data model**
5.  **Validate data quality before publishing**

The goal is simple: instead of relying on memory, I can rely on
**documented principles**.

Alongside this playbook, I also created a **pipeline checklist** that
helps guide the implementation process for each stage of the pipeline.

This small change significantly reduced mental friction. Instead of
constantly asking *"what might I be missing?"*, I can simply consult the
checklist.

------------------------------------------------------------------------

### Cloud Tools Introduce a New Constraint: Cost

Moving into cloud-based tools introduced something that did not exist in
local experiments: **cost awareness**.

Platforms such as Snowflake are powerful, but they are not free. Running
queries, storing data, and experimenting carelessly can quickly create
unnecessary expenses.

Because of this, I adopted a **local-first development strategy**.

The idea was straightforward:

1.  Develop the analytical model locally.
2.  Explore the SaaS business logic and metrics.
3.  Stabilize the pipeline structure.
4.  Only then migrate the pipeline to the cloud stack.

Working locally made experimentation much easier. I could iterate on the
dimensional model and transformations without worrying about compute
credits or warehouse usage.

Once the architecture felt stable, transitioning the pipeline to the
cloud became more of a **deployment step rather than a design experiment**.

------------------------------------------------------------------------

### Scope Creep Is Real in the Modern Data Stack

One surprising challenge of working with modern data tools is the
**sheer number of available features**.

While building this pipeline, I discovered many interesting capabilities
across the tools I was using.

For example, **dbt includes features such as snapshots**, which can
automatically capture historical changes in source tables. This is
extremely useful for tracking how data evolves over time.

The temptation is to explore everything at once.

However, that quickly leads to **scope creep**. The project can grow
endlessly if every interesting feature becomes part of the
implementation.

To avoid this, I deliberately limited the scope of the project. The goal
was not to use every feature available, but to **build a coherent pipeline architecture first**.

Additional features can always be explored later.

------------------------------------------------------------------------

### Learning Orchestration Was the Hardest Part

The most technically challenging part of this phase was learning
**Apache Airflow**.

Compared with SQL modeling or transformation logic, orchestration felt
much more operational and fragile. Many small details can cause
failures:

-   DAG configuration errors
-   task dependency issues
-   environment setup problems
-   scheduling misconfigurations

During development, the pipeline failed many times before it finally ran
correctly.

However, once the system started working reliably, the payoff became
very clear.

Airflow allowed the entire pipeline to run automatically, executing
ingestion, transformations, and data quality checks in a structured
workflow.

One feature I particularly enjoyed was adding **Telegram alerts**. Now
the pipeline sends a message directly to my phone whenever it succeeds
or fails.

In a real production environment, monitoring would likely involve more
sophisticated tools. But even this lightweight alerting system
demonstrates an important concept:

**data pipelines should be observable.**

------------------------------------------------------------------------

### The Power of Templates and Boilerplates

Another lesson from this phase was the value of **saving reusable structures**.

Complex setups often require significant effort to design correctly.
Once something finally works, such as: 

- a project structure
- orchestration pattern 
- transformation layout 

It would be wasteful
to rebuild it from scratch every time.

So instead of treating each project as a completely new start, I began
saving working structures as **templates or boilerplates**.

These templates act as reusable foundations for future projects.

They help prevent two common problems:

-   forgetting important architectural pieces
-   **reinventing the wheel** for every new pipeline

Over time, this collection of templates becomes a form of **personal engineering toolkit**.

------------------------------------------------------------------------

### The Core Lesson of Phase 3

Phase 3 reinforced an important idea for me:

> [!NOTE]
> Good engineering practices are not only about correctness 
> they are also about reducing cognitive load when working with complex
> systems.

Playbooks, checklists, templates, and architectural discipline all serve
the same purpose: allowing engineers to focus on meaningful problems
rather than repeatedly rediscovering the basics.

------------------------------------------------------------------------

## What's Next → Phase 4: Cloud Infrastructure Foundations

With Phase 3 completed, the next step in my roadmap is **Phase 4: Cloud Infrastructure Basics**.

This phase will focus on the infrastructure side of modern data
platforms, including:

-   **Containerized pipelines with Docker**
-   **Infrastructure as Code using Terraform**
-   **Basic cloud networking and IAM concepts**
-   **CI/CD automation using GitHub Actions**

The goal is to move beyond building pipelines locally or manually and
start learning how **data infrastructure can be provisioned, deployed, and maintained in a reproducible way**.

### A Short Detour: Exploring the Full Data Stack

Before diving fully into infrastructure topics, I also plan to briefly
explore two additional parts of the data stack: **data ingestion and data visualization**.

Tools such as **Airbyte** can help automate ingestion from external data
sources, while **Power BI** can be used to visualize and validate the
analytical outputs produced by the pipeline.

This short detour is mainly about understanding the **end-to-end flow of a data system**, from raw data sources all the way to analytical
dashboards.

Once that perspective is clearer, Phase 4 will continue focusing on the
infrastructure layer and the operational foundations of cloud-based data
platforms.
