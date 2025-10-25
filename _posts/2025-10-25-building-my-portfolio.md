---
title: "Building My Personal Portfolio Website with GitHub Pages and Jekyll"
excerpt: "A step-by-step guide (and reflection) on how I built and branded my own portfolio site from scratch."
date: 2025-10-07
layout: single
classes: wide
author_profile: true
header:
  teaser: /assets/img/articles/phello_world_thumb.png
  overlay_image: /assets/img/articles/phello_world_thumb.png
  overlay_filter: 0.25
---
  
---

Creating my own portfolio website has been one of the most rewarding projects I’ve done so far.  
I wanted a site that not only **showcases my projects** and **shares my thoughts**, but also feels *authentically mine* — clean, consistent, and professional.

The best part? I built and customised everything **myself** — using **GitHub Pages**, **Jekyll**, and a bit of CSS and design work.

---

## 🎯 Why I built it
I was applying for graduate technology roles, and I realised how much a personal portfolio can help you stand out.  
Instead of sending recruiters a list of links, I wanted a space that reflected how I think and work — from my **Streamlit apps** to my **research dissertation** and **technical writing**.

---

## 🛠️ Tools and technologies I used
Here’s what powers my site:

- **GitHub Pages** – hosts everything for free, directly from a GitHub repository  
- **Jekyll** – a static site generator that makes writing posts and pages easy  
- **Minimal Mistakes** – a flexible Jekyll theme that I customised to match my branding  
- **Custom domain** – purchased through GoDaddy and connected via DNS  
- **Custom SCSS** – for colours, layout, typography, and responsive tweaks

---

## ⚙️ Step 1 — Setting up GitHub Pages

I started by creating a repository named:
```
lucyinett.github.io
```
GitHub automatically recognises this as a Pages site.

Then I added a minimal Jekyll setup by including:
```yaml
remote_theme: "mmistakes/minimal-mistakes@4.24.0"
plugins:
  - jekyll-feed
  - jekyll-seo-tag
  - jekyll-include-cache
```

This gave me a foundation to build from without needing to host anything myself.

---

## 🖌️ Step 2 — Designing the look and feel

The fun part: **branding**.

I wanted something simple but personal — a teal-based palette with a calm, modern feel.  
Here’s part of my colour scheme from `main.scss`:

```scss
:root {
  --brand-primary: #0ea5a3;
  --brand-accent: #8bd3dd;
  --brand-text: #0f172a;
}
```

I customised the navigation bar, buttons, footer, and page width to keep everything cohesive.  
A small but satisfying detail: I also designed my own **“LI” logo** to use in the header and favicon.

---

## 🧩 Step 3 — Structuring content

I created separate sections for my content:
```
_pages/         → CV, Articles, Home
_projects/      → Project write-ups
_posts/         → Blog-style articles
assets/img/     → Images and logos
assets/docs/    → CV PDFs and papers
```

This structure lets me keep everything modular and easy to update.  
Each project is its own Markdown file under `_projects/`, with full descriptions, screenshots, and links to GitHub.

---

## 🌐 Step 4 — Connecting my custom domain

I bought my domain through **GoDaddy** and linked it to GitHub Pages using DNS records.

GitHub requires:
- 4 `A` records pointing to GitHub’s IPs  
- A `CNAME` record pointing to `lucyinett.github.io`

Once the DNS propagated, I added `lucyinett.co.uk` to the **Custom Domain** section in my repo settings — and it just worked.

---

## 🧭 Step 5 — Adding polish

The last 10% made the biggest difference:
- Replaced generic “Blog” with **Articles** for a more polished tone  
- Added footer social links (GitHub, LinkedIn, Email)  
- Embedded my **CV** directly as a PDF viewer  
- Adjusted margins so project pages are clean and centred  

Here’s a small example of my CV embed:

```html
<iframe src="/assets/docs/LucyInett-CV.pdf" width="100%" height="800px" style="border:none;"></iframe>
```

---

## 💡 What I learned
This project taught me how **front-end design and content structure** go hand in hand.  
Small details — like consistent spacing, tone, and navigation — make a site feel intentional.

It also reminded me that you don’t need to use a heavy framework to build something elegant;  
a bit of CSS and clear organisation can go a long way.

---

## 🚀 For anyone who wants to make their own

If you want to build a similar portfolio:
1. Create a `username.github.io` repo  
2. Add Jekyll via `remote_theme` in `_config.yml`  
3. Write your pages in Markdown  
4. Customise your SCSS for branding  
5. Link a custom domain if you have one  

That’s it — free hosting, full control, and no backend headaches.

---

## ✨ Final thoughts
I built this portfolio completely myself — from the layout and logo to the SCSS theme and structure.  
It’s become my space to grow, reflect, and share my work, and I’d really encourage anyone learning tech to do the same.

[View my site live →](https://lucyinett.co.uk)
