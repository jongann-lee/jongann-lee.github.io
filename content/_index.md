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
        - title: Visiting Researcher
          company: Polytechnique Laboratory for Assistive and Rehabilitation technologies (Prof. Abolfazl Mohebbi)
          company_url: https://www.polarlab.ca/about
          company_logo: polymtl
          location: Montréal, QC, Canada
          date_start: '2024-06-15'
          date_end: '2024-10-14'
          description: |2-
              * Designed a novel 2‑DoF ankle exoskeletonwith a compliantmechanism to enable inversion and eversionmovements aswell as dorsiflexion and plantarflexion.
              * Built a prototype using 3D printing and integrated it with the existing PERL ankle exoskeleton to confirm the desired performance

        - title: Undergraduate Intern
          company: Interactive and Networked Robotics Laboratory(Prof. Dongjun Lee)
          company_url: https://www.inrol.snu.ac.kr/
          company_logo: SNU
          location: Seoul, Republic of Korea
          date_start: '2023-03-01'
          date_end: '2024-06-14'
          description: |2-
              * Created a geometric tracking controller for the 5‑CDoF multirotor capable of tracking a 5‑variable trajectory consisting of position, yaw, and pitch, which was shown to be differentially flat outputs of the vehicle dynamics.
              *  Proved the almost global exponential attractiveness of the controlled vehicle dynamics using Lyapunov analysis, and demonstrated the stability using a Matlab numerical simulation.
              * Created a novel adaptive quadrotor controller by adapting an adaptive control scheme based on the geodesic distance of the manifold of physically consistent inertial parameters, to the geometric tracking controller. 
        
        - title: Research Intern
          company: J.Maple
          company_url: https://jmarple.ai/ko/
          company_logo: JMaple
          location: Seoul, Republic of Korea
          date_start: '2023-09-01'
          date_end: '2023-12-01'
          description: |2-
              * Implemented various LiDAR inertial odometry(LIO) algorithms for quadrotor navigation without GPS.
              * Tested the algorithm’s computational and tracking performance using pre‑recorded LiDAR data.

        - title: Research Assistant
          company: Data Design Engineering
          company_url: http://datadesign.engineering/
          company_logo: DDE
          location: Seoul, Republic of Korea
          date_start: '2022-06-01'
          date_end: '2022-08-01'
          description: |2-
              * Performed research on satellites and their payload, specifically focusing on Earth observation satellites and synthetic aperture radar(SAR).

        - title: English-Korean Interpreter and Translator
          company: Republic of Korea Air Force (military service)
          company_url: https://rokaf.airforce.mil.kr/
          company_logo: ROKAF
          location: Pyeongtaek, Gyeonggi-do, Republic of Korea
          date_start: '2020-05-01'
          date_end: '2022-02-01'
          description: |2-
              * Worked as an interpreter/translator for the Air Force Operations Command A3, interpreting various operational dialogue between ROK and US air force officers, and translating English USAF documents, doctrines and emails for our ROK members and vice versa.
  
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      # default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      # buttons:
      #   - name: All
      #     tag: '*'
      #   - name: Deep Learning
      #     tag: Deep Learning
      #   - name: Other
      #     tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false

    design:
      columns: '2'
  - block: accomplishments
    content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
      title: 'Honors'
      subtitle:
      # Date format: https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - certificate_url: ''
          date_end: ''
          date_start: '2023-02-01'
          description: ''
          icon: ''
          organization: Kwanjeong Educational Foundation
          organization_url: https://www.ikef.or.kr/
          title: Kwanjeong Domestic Undergraduate Scholarship
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2022-09-01'
          description: 
          icon: ''
          organization: Boeing Korea
          organization_url: https://www.boeing.co.kr/
          title: Boeing Korea Scholarship
          url: ''
        - certificate_url: 
          date_end: 
          date_start: '2019-09-01'
          description: ''
          icon: ''
          organization: Seoul National University College of Engineering
          organization_url: https://www.boeing.co.kr/
          title: College of Engineering Scholarship for Academic Excellence
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2018-03-01'
          description: ''
          icon: ''
          organization: Hanseong Sonjaehan Scholarship Foundation
          organization_url: https://www.sonjaehan.com/
          title: Hanseong Nobel Prodigy Scholarship
          url: ''
    design:
      columns: '2'
  # - block: collection
  #   id: posts
  #   content:
  #     title: Recent Posts
  #     subtitle: ''
  #     text: ''
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 3
  #     # Filter on criteria
  #     filters:
  #       folders:
  #         - post
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: compact
  #     columns: '2'

  - block: collection
    id: publications
    content:
      title: Publications
      count: 3
      filters:
        folders:
          - publication
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
