---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: hero
    content:
      title: Solving Data Problems, One Bite at a Time
      text: 
      primary_action:
        text: #Get Started
        url: #https://hugoblox.com/templates/
        icon: #rocket-launch
      secondary_action:
        text: #Read the docs
        url: #https://docs.hugoblox.com
      announcement:
        text: #"Announcing the release of version 1."
        link:
          text: #"Read more"
          url: #"/blog/"
    design:
    #   spacing:
    #     padding: [0, 0, 0, 0]
    #     margin: [0, 0, 0, 0]
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
          
  - block: collection
    content:
      title: Pinned Post
      count: '1'
      filters:
        folders:
          - blog
        featured_only: true
    design:
      view: showcase
      columns: '1'
  - block: collection
    content:
      title: Recent Posts
      count: '2'
      filters:
        folders:
          - blog
          - projects
        exclude_featured: true
    design:
      view: article-grid
      columns: '2'
      order: desc

  # - block: collection
  #   content:
  #     title: Blog Posts
  #     text: ''
  #     filters:
  #       folders:
  #         - blog
  #       exclude_featured: true
  #     count: '2'
  #     order: desc
  #   design:
  #     view: article-grid
  #     columns: '2'
---
