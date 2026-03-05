---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-01-05
type: landing

design:
  # Default section spacing
  spacing: '0'

sections:
  # Developer Hero - Gradient background with name, role, social, and CTAs
  # - block: dev-hero
  #   id: hero
  #   content:
  #     username: me
  #     greeting: "Hi, I'm"
  #     show_status: false
  #     show_scroll_indicator: false
  #     typewriter:
  #       enable: false
  #       prefix: "I build"
  #       strings:
  #         - "full-stack web apps"
  #         - "scalable APIs"
  #         - "beautiful UIs"
  #         - "open source tools"
  #       type_speed: 70
  #       delete_speed: 40
  #       pause_time: 2500
  #     cta_buttons:
  #       - text: View My Work
  #         url: "#projects"
  #         icon: arrow-down
  #       - text: Get In Touch
  #         url: "#contact"
  #         icon: envelope
  #   design:
  #     style: centered
  #     avatar_shape: rounded
  #     animations: true
  #     background:
  #     #   color:
  #     #     light: "#fafafa"
  #     #     dark: "#0a0a0f"
  #     # spacing:
  #     #   padding: ["6rem", "0", "4rem", "0"]
  #       image:
  #         # Add your image background to `assets/media/`.
  #         filename: background.png
  #         filters:
  #           brightness: 0.5
  #         size: cover
  #         position: center
  #         parallax: false
  
  # Filterable Portfolio - Alpine.js powered project filtering
  - block: hero
    content:
      title: Solving Data Problems, One Bite at a Time
      text: 
      primary_action:
        text: View My Work
        url: "#projects"
        icon: rocket-launch
      secondary_action:
        text: Get In Touch
        url: "#contact"
      announcement:
        text: "Hi, I'm Karhomatul Faqih Al Amin."
        link:
          text: "Get to know me"
          url: "/about/"
    design:
      spacing:
        padding: ["6rem", "0", "10rem", "0"]
        margin: [0, 0, 0, 0]
      # For full-screen, add `min-h-screen` below
      css_class: "dark"
      background:
        image:
          # Add your image background to `assets/media/`.
          filename: background.png
          filters:
            brightness: 0.5
          size: cover
          position: center
          parallax: false

  - block: features
    id: features
    content:
      title: Core Capabilities
      text: My data engineering expertise
      items:
        - name: Data Modeling (dbt)
          icon: square-3-stack-3d
          description: Designing staging → foundation → marts layers with star schema and SCD Type 2 using dbt.
        - name: Metric Standardization
          icon: chart-pie
          description: Defining consistent KPIs and reusable metrics across analytical models.
        - name: ELT Pipeline Orchestration
          icon: clock
          description: Building batch pipelines using Airflow with dependency and retry handling.
        - name: Problem Decomposition
          icon: puzzle-piece
          description: Implementing incremental models to reduce runtime and warehouse cost.
        - name: Data Quality Testing
          icon: beaker
          description: Applying dbt tests and validation checks to ensure data reliability.
        - name: Warehouse Optimization
          icon: cube
          description: Structuring transformations efficiently in Snowflake.
    design:
      view: article-grid
      columns: 3
      background:
        # color:
        #   light: "#f5f5f5"
        #   dark: "#08080c"
      spacing:
        padding: ["0", "0", "0", "0"]

  # Visual Tech Stack - Icons organized by category
  - block: tech-stack
    id: skills
    content:
      title: "Tech Stack"
      subtitle: "My go-to stack for data engineering pipelines"
      categories:
        - name: Languages
          items:
            - name: Python
              icon: devicon/python
            - name: SQL
              icon: devicon/azuresqldatabase
        - name: Data Infrastructure & Tools
          items:
            - name: Cloudflare R2
              icon: devicon/cloudflare
            - name: dbt
              icon: custom/dbt
            - name: Snowflake
              icon: custom/snowflake
            - name: Airflow
              icon: devicon/apacheairflow
            - name: PostgreSQL
              icon: devicon/postgresql

    design:
      style: grid
      show_levels: false
      background:
        # color:
          # light: "#f5f5f5"
          # dark: "#08080c"
      spacing:
        padding: ["0", "0", "0", "0"]
  
    # Recent Blog Posts
  - block: collection
    id: projects
    content:
      title: "Featured Projects"
      subtitle: "A selection of my recent work"
      text: ''
      filters:
        folders:
          - projects
        exclude_featured: false
      count: 2
      order: desc
    design:
      view: article-grid
      columns: 2
      background:
        # color:
        #   light: "#f5f5f5"
        #   dark: "#08080c"
      spacing:
        padding: ["0", "0", "0", "0"]

  # - block: portfolio
  #   id: projects
  #   content:
  #     title: "Featured Projects"
  #     subtitle: "A selection of my recent work"
  #     count: 2
  #     filters:
  #       folders:
  #         - projects
  #     # buttons:
  #     #   - name: All
  #     #     tag: '*'
  #     #   - name: Full-Stack
  #     #     tag: Full-Stack
  #     #   - name: Frontend
  #     #     tag: Frontend
  #     #   - name: Backend
  #     #     tag: Backend
  #     # default_button_index: 2
  #     # Archive link auto-shown if more projects exist than 'count' above
  #     # archive:
  #     #   enable: false  # Set to false to explicitly hide
  #     #   text: "Browse All"  # Customize text
  #     #   link: "/work/"  # Custom URL
  #   design:
  #     columns: 2
  #     background:
  #       # color:
  #       #   light: "#ffffff"
  #       #   dark: "#0d0d12"
  #     spacing:
  #       padding: ["4rem", "12rem", "4rem", "12rem"]

  - block: cta-image-paragraph
    id: solutions
    content:
      items:
        - title: Current Focus
          text: "Analytics Engineering"
          feature_icon:   
          features:
            - "**Advanced Modeling**: Implementing **dbt layering** (Staging to Marts) within **Snowflake** for robust data transformation."
            - "**Metric Automation**: Orchestrating **automated pipelines** for business-critical SaaS metrics (MRR, Retention, LTV)."
            - "**Reliable Delivery**: Leveraging **Cloudflare R2** and **Airflow** to ensure data quality and seamless orchestration."
          # Upload image to `assets/media/` and reference the filename here
          image: current-phase.png
          button:
            text: See full roadmap
            url: https://datadonut.netlify.app/blog/data-engineer-roadmap/
          # button:
          #   text: See full roadmap
          #   url: https://datadonut.netlify.app/blog/data-engineer-roadmap/
        # - title: Next Phase Roadmap
        #   text: "Phase 4: Cloud Infrastructure & Automation"
        #   feature_icon:   
        #   features:
        #     - "**Infrastructure as Code**: Provisioning scalable cloud environments and networking using **Terraform**."
        #     - "**Containerized Workloads**: Ensuring pipeline portability and production-ready environments with **Docker**."
        #     - "**CI/CD & DevOps**: Automating deployment lifecycles via **GitHub Actions** for seamless delivery to **AWS/GCP**."
        #   # Upload image to `assets/media/` and reference the filename here
        #   image: next-phase.png
        #   button:
        #     text: See full roadmap
        #     url: https://datadonut.netlify.app/blog/data-engineer-roadmap/
    design:
      # Section background color (CSS class)
      css_class: ""
      spacing:
        padding: ["0", "0", "0", "0"]

  # Recent Blog Posts
  - block: collection
    id: blog
    content:
      title: "Recent Posts"
      subtitle: "Thoughts on web development, tech, and more"
      text: ''
      filters:
        folders:
          - blog
        exclude_featured: false
      count: 2
      order: desc
    design:
      view: article-grid
      columns: 2
      background:
        # color:
        #   light: "#000b49"
        #   dark: "#08080c"
      spacing:
        padding: ["0", "0", "0", "0"]
  
  # Contact Section
  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Let's build something amazing together"
      text: |-
        I'm always interested in hearing about new projects and opportunities.
        Whether you're looking to hire, collaborate, or just want to say hi, feel free to reach out!
      email: karhomatulfakih@gmail.com
      autolink: true
    design:
      columns: '1'
      background:
        # color:
        #   light: "#ffffff"
        #   dark: "#0d0d12"
      spacing:
        padding: ["0", "0", "0", "0"]
  
  # CTA Card
  - block: cta-card
    content:
      title: "Open to Opportunities"
      text: |-
        I'm currently looking for **Analytics Engineer** or **Data Engineer** roles.
        
        Let's connect and discuss how I can help your team.
      # button:
      #   text: 'Download Resume'
      #   url: uploads/resume.pdf
      #   new_tab: true
    design:
      card:
        # Light mode: soft pastel theme gradient | Dark mode: rich deep gradient
        css_class: 'bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700'
        text_color: dark
      background:
        # color:
        #   light: "#f5f5f5"
        #   dark: "#08080c"
      spacing:
        padding: ["0", "0", "0", "0"]
---
