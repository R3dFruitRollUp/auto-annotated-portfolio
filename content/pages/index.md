---
type: PageLayout
title: Home
colors: colors-a
backgroundImage:
  type: BackgroundImage
  url: /images/bg1.jpg
  backgroundSize: cover
  backgroundPosition: center
  backgroundRepeat: no-repeat
  opacity: 75
sections:
  - type: HeroSection
    title: Alexander Floyd Glenn
    subtitle: Business Intelligence & AI Solutions Engineer
    actions: []
    media:
      type: ImageBlock
      url: /images/1761322480544.jpeg
      altText: Image of Alexander Floyd Glenn
      caption: Ai generated Content
      elementId: ''
    colors: colors-f
    backgroundSize: full
    elementId: ''
    styles:
      self:
        height: auto
        width: wide
        padding:
          - pt-36
          - pb-48
          - pl-4
          - pr-4
        flexDirection: row
        textAlign: left
    text: ''
  - type: TextSection
    title: My
    subtitle: Experience
    text: >
      I am an end-to-end data and analytics engineer designing Tableau
      dashboards, SQL and Python data models, ETL pipelines, and AI-driven
      experiments for mortgage, consumer lending, and large-scale contact-center
      operations.My work  showcases how that interdisciplinary, consultative
      solutions engineering approach transfers across domains.. From lending and
      risk to call center science, workforce management, and broader enterprise
      operations. My work supports thousands of agents across multiple countries
      and is grounded in experience inside a super-regional S\&P 500 bank that
      has grown its balance sheet from roughly $120B in assets in 2020 to over
      $200B by 2024, with announced acquisitions positioning it around $276B in
      assets. Expanding its footprint across more than 20 states.  
    colors: colors-d
    variant: variant-b
    elementId: ''
    styles:
      self:
        height: auto
        width: wide
        padding:
          - pt-28
          - pb-28
          - pl-4
          - pr-4
        textAlign: left
  - type: LabelsSection
    title: My Skills
    subtitle: The section subtitle
    items:
      - type: Label
        label: 'WEB 1, 2, 3'
        url: ''
      - type: Label
        label: React
        url: ''
      - type: Label
        label: Microsoft Office
        url: ''
      - type: Label
        label: Next.js
        url: ''
      - type: Label
        label: Netlify
        url: ''
      - type: Label
        label: Pancakes
        url: ''
      - type: Label
        label: C++
        url: ''
      - type: Label
        label: Swift
        url: ''
    colors: colors-d
    elementId: ''
    styles:
      self:
        height: auto
        width: wide
        padding:
          - pt-36
          - pb-36
          - pl-4
          - pr-4
        textAlign: left
  - colors: colors-f
    type: FeaturedProjectsSection
    elementId: ''
    actions:
      - type: Link
        label: See all projects
        url: /projects
    showDate: false
    showDescription: true
    showFeaturedImage: true
    showReadMoreLink: true
    variant: variant-b
    projects:
      - content/pages/projects/NFL.md
    styles:
      self:
        height: auto
        width: wide
        padding:
          - pt-24
          - pb-24
          - pl-4
          - pr-4
        textAlign: left
    subtitle: Projects
  - type: FeaturedPostsSection
    elementId: ''
    colors: colors-f
    variant: variant-d
    subtitle: Featured Posts
    showFeaturedImage: false
    actions:
      - type: Link
        label: See all posts
        url: /blog
    posts:
      - content/pages/blog/stop-fighting-your-spreadsheets.md
    showDate: true
    showExcerpt: true
    showReadMoreLink: true
    styles:
      self:
        height: auto
        width: narrow
        padding:
          - pt-28
          - pb-48
          - pl-4
          - pr-4
        textAlign: left
  - type: ContactSection
    colors: colors-f
    backgroundSize: full
    title: "Rawr \U0001F996"
    form:
      type: FormBlock
      elementId: sign-up-form
      fields:
        - name: firstName
          label: First Name
          hideLabel: true
          placeholder: First Name
          isRequired: true
          width: 1/2
          type: TextFormControl
        - name: lastName
          label: Last Name
          hideLabel: true
          placeholder: Last Name
          isRequired: false
          width: 1/2
          type: TextFormControl
        - name: email
          label: Email
          hideLabel: true
          placeholder: Email
          isRequired: true
          width: 1/2
          type: EmailFormControl
        - name: address
          label: Address
          hideLabel: true
          placeholder: Address
          isRequired: true
          width: 1/2
          type: TextFormControl
        - name: updatesConsent
          label: Sign me up to recieve updates
          isRequired: false
          width: full
          type: CheckboxFormControl
      submitLabel: "Submit \U0001F680"
      styles:
        self:
          textAlign: center
    styles:
      self:
        height: auto
        width: narrow
        margin:
          - mt-0
          - mb-0
          - ml-0
          - mr-0
        padding:
          - pt-24
          - pb-24
          - pr-4
          - pl-4
        flexDirection: row
        textAlign: left
    text: "Share your thoughts please! \U0001F4AC\n"
---
