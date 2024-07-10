---
# Leave the homepage title empty to use the site title
title: ''
date: 2024-07-10
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: English-Korean Interpreter and Translator
          company: Republic of Korea Air Force (military service)
          company_url: https://rokaf.airforce.mil.kr/
          company_logo: images/ROKAF.png
          location: Pyeongtaek, Gyeonggi-do, Republic of Korea
          date_start: '2020-05'
          date_end: '2022-02'
          description: |2-
              * Worked as an interpreter/translator for the Air Force Operations Command A3, interpreting various operational dialogue between ROK and US air force officers, and translating English USAF documents, doctrines and emails for our ROK members and vice versa.

        - title: Research Assistant
          company: Data Design Engineering
          company_url: http://datadesign.engineering/
          company_logo: images/DDE.jpg
          location: Seoul, Republic of Korea
          date_start: '2022-06'
          date_end: '2022-08'
          description: |2-
              * Performed research on satellites and their payload, specifically focusing on Earth observation satellites and synthetic aperture radar(SAR).

        - title: J.Maple
          company: Research Intern
          company_url: https://jmarple.ai/ko/
          company_logo: images/JMaple.png
          location: Seoul, Republic of Korea
          date_start: '2023-09'
          date_end: '2023-12'
          description: |2-
              * Implemented various LiDAR inertial odometry(LIO) algorithms for quadrotor navigation without GPS.
              * Tested the algorithm’s computational and tracking performance using pre‑recorded LiDAR data.
    design:
      columns: '2'
  - block: accomplishments
    content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
      title: 'Accomplish&shy;ments'
      subtitle:
      # Date format: https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - certificate_url: https://www.coursera.org
          date_end: ''
          date_start: '2021-01-25'
          description: ''
          icon: coursera
          organization: Coursera
          organization_url: https://www.coursera.org
          title: Neural Networks and Deep Learning
          url: ''
        - certificate_url: https://www.edx.org
          date_end: ''
          date_start: '2021-01-01'
          description: Formulated informed blockchain models, hypotheses, and use cases.
          icon: edx
          organization: edX
          organization_url: https://www.edx.org
          title: Blockchain Fundamentals
          url: https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals
        - certificate_url: https://www.datacamp.com
          date_end: '2020-12-21'
          date_start: '2020-07-01'
          description: ''
          icon: datacamp
          organization: DataCamp
          organization_url: https://www.datacamp.com
          title: 'Object-Oriented Programming in R'
          url: ''
    design:
      columns: '2'
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Deep Learning
          tag: Deep Learning
        - name: Other
          tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: collection
    id: featured
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card
  - block: collection
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: contact    
    id: contact
    content:
      title: Contact
      # Contact (add or remove contact options as necessary)
      email: johnny3357@snu.ac.kr
      phone: ''
      address:
        street: Gwanak-ro 1
        city: Gwanak-gu
        region: Seoul
        postcode: '08826'
        country: Republic of Korea
        country_code: KR
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '37.4497'
        longitude: '126.9523'  
      contact_links:
        - icon: linkedin
          icon_pack: fab
          name: LinkedIn
          link: www.linkedin.com/in/jongann-lee
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
---
