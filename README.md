# Xander Intelligence – Analytics & Developer Portfolio

This repository powers my personal portfolio as a **Business Intelligence Solutions Engineer**.

The site is designed to do more than look good. It exists to show how I think about data, how I build analytics products, and how I communicate insights to real people who make decisions. Under the hood it uses **Next.js**, **Tailwind CSS**, and **Netlify**, with content wired into the **Netlify Visual Editor** so stakeholders can change copy and content without touching code.

---

## What this repository is

This project is a production-style portfolio site that behaves like a small internal product.

It brings together a modern React frontend, a content model that treats case studies as data, and an editing workflow that feels natural for non-developers. The goal is to showcase real analytics and BI work: dashboards, stories, tradeoffs, and the decisions that followed.

For hiring managers and collaborators, this repo is both a code sample and a working example of how I would structure an internal analytics portal or executive dashboard site.

---

## Auto-annotated editing with the Netlify Visual Editor

The portfolio integrates with the **Netlify Visual Editor**, which allows inline editing directly on the rendered page. When someone wants to change text, images, or content blocks, they can click on the element, edit it, and commit the change through Git.

This is powered by an auto-annotation pattern rather than sprinkling attributes manually across the codebase.

Content is loaded and normalized in utilities such as `src/utils/content.ts`. As part of that process, content objects are decorated with extra metadata that describes how they should be mapped to components and how the editor should treat them.

When pages render, `src/components/components-registry.tsx` connects those content objects to the right React components and wraps them with the annotation logic used by the Visual Editor. This approach keeps annotation code centralized, predictable, and scalable as new content types are added.

From an engineering point of view, this demonstrates comfort with content modeling, separation of concerns, and building systems that editors can use safely without breaking layouts.

---

## Portfolio focus: analytics and BI storytelling

Although this is a web app, the primary focus of the portfolio is **analytics and business intelligence**.

The site is structured around projects and case studies that show how a problem was framed, what data and tools were used, and how insights turned into action. Domains include banking, consumer lending, call center operations, and applied analytics such as sports decision-making.

Each project is written for stakeholders who care about outcomes, not jargon. The code supports that by making it easy to stitch together narrative, visuals, and embedded dashboards in a single coherent page.

---

## Tech stack overview

The portfolio is built with a modern, pragmatic stack:

- **Next.js** for routing, server-side rendering capabilities, and overall app structure  
- **React** for composing UI into reusable components  
- **Tailwind CSS** for fast, consistent styling with a clean utility-first approach  
- **Netlify** for hosting, CI/CD, preview builds, and deployment automation  
- **Netlify Visual Editor + Git Content Source** for inline editing with Git as the single source of truth for content  

On top of that, the site is designed to host and embed tools like **Tableau** so that analytics work can be experienced as it would be inside a production environment.

---

## Live site and deployment

The original starter for this project comes from Netlify’s auto-annotated portfolio example:

https://auto-annotated-portfolio.netlify.app

This repository adapts and extends that starter into a portfolio focused on analytics, BI engineering, and data storytelling.

You can deploy this repository to your own Netlify account using the standard one-click flow:

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/R3dFruitRollUp/auto-annotated-portfolio)

The deploy flow connects the site to this GitHub repository, configures a Netlify pipeline, and sets up automatic builds for future commits.

---

## Developing locally

To work with the project locally, clone the repository and install dependencies:

    git clone https://github.com/R3dFruitRollUp/auto-annotated-portfolio.git
    cd auto-annotated-portfolio
    npm install

Start the Next.js development server:

    npm run dev

By default, the site will be available at:

    http://localhost:3000

This local setup is the same environment used for iterating on layouts, components, and content architecture.

---

## Using the Netlify Visual Editor

The Netlify Visual Editor can also be run alongside the Next.js dev server.

Install the CLI:

    npm install -g @stackbit/cli

From the project root, start the Visual Editor dev server:

    stackbit dev

The CLI will output a dedicated Visual Editor URL. Opening that URL in a browser allows you to sign in, connect the project, and edit content visually while the underlying changes are captured as Git commits.

This is aligned with how I want internal analytics tools to behave: editors should be able to change text, labels, and content safely, while engineering controls the structure and integrity of the system.

---

## How analytics and Tableau projects are presented

The portfolio is set up to present analytics work in a way that feels natural to stakeholders.

Each project page is written to answer a few core questions in plain language.

**What problem were we solving?**  
The narrative describes the business context, the constraints, and what was at risk. This might be call center performance, lending strategy, operational efficiency, or even a sports decision framework.

**What data and methods were used?**  
The writeup summarizes how data was sourced and modeled, which BI tools were involved, and how business rules were encoded. The underlying work might live in SQL, Tableau, Python, R, or a data warehouse, but the story remains accessible.

**What does the dashboard or visual actually show?**  
Embedded dashboards, such as Tableau views, are accompanied by explanations of key metrics, filters, definitions, and how the visual is intended to be used.

**What impact did this have?**  
The focus is on how the work changed decisions, clarified tradeoffs, or made risk more visible. When possible, the pages describe operational or financial outcomes.

The code in this repository supports that storytelling by making it straightforward to embed external visual tools, write content in a structured way, and keep everything editable over time.

---

## Project structure

The project uses a standard Next.js layout with a content-oriented twist.

Routing and top-level pages live under `src/pages`. This includes the homepage and any top-level routes for projects, about pages, and similar sections.

Reusable UI and layout pieces live under `src/components`. This includes navigation, layout wrappers, content section components, and the Visual Editor annotation wrappers that make the site editable.

Content loading and annotation helpers are in `src/utils/content.ts`. These functions normalize raw content and attach metadata that the Visual Editor and component registry rely on.

The registry that connects content types to React components is defined in `src/components/components-registry.tsx`. This is the central place where new content block types are introduced and wired up, keeping the rest of the codebase focused on layout and styling.

Static assets such as images and icons live under `public`, and any structured content folders (for example, `content` or `data`) are used to hold Markdown, JSON, or similar content files that drive pages.

---

## Customization and extension

This project is intended to evolve along with the portfolio.

Branding can be adjusted through Tailwind configuration and shared layout components, allowing typography, spacing, and color systems to be tuned to match a personal or organizational identity.

The content model can be extended by adding new block types, such as a dedicated Tableau embed component, metric callout sections, or case study headers. These new blocks are registered in the components registry and immediately become editable units in the Visual Editor.

Site structure can expand to include additional project collections, blog posts, or speaking and writing pages. Each new section benefits from the same content system and editing workflow.

Integrations such as analytics tracking, contact forms, or lightweight serverless endpoints on Netlify can also be layered in to support lead capture, experimentation, or internal tooling.

---

## Why this matters to employers

This repository is intentionally structured as more than a static splash page.

It shows how I approach building a front-end experience that feels like a product, not a slide deck. It demonstrates how I design content systems that non-developers can own without putting the site at risk. It presents analytics and BI work with enough technical depth to be credible and enough clarity to be used.

The codebase is organized around patterns and registries instead of one-off exceptions. The editing experience is designed so that stakeholders can evolve the content without breaking the structure. The portfolio itself mirrors how I like to build internal analytics tools: opinionated where it needs to be, flexible where it can be, and always focused on the decisions people need to make.

If you are reviewing this as part of a hiring or partnership conversation, this repo is a concrete example of how I think about data products, stakeholder experience, and long-term maintainability.

---

## Contact

This is a customized version of Netlify’s `auto-annotated-portfolio` starter, adapted to my analytics and BI portfolio needs.

To discuss the implementation, analytics work, or potential opportunities, you can open an issue in this repository or use the contact section on the deployed portfolio site.

---
