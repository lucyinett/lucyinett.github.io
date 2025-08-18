---
title: "Skill Boost — Personalised Recommendations for Student Skill Growth"
excerpt: "NLP + content-based + collaborative filtering to guide student skill growth."
image: /assets/img/projects/skill-boost-cover.png   # optional card image
permalink: /projects/skill-boost/
---


**Skill Boost** is a full-stack recommendation platform that helps Computer Science learners discover the **right skills, courses, and events** at the right time.  
It combines **NLP** to understand goals, **content-based ranking** for relevant resources, and **collaborative filtering** to surface skills liked by similar users — all wrapped in a clean web app and containerised for easy deployment.  

---

## Why it matters
Learners face an overwhelming amount of content.  
Skill Boost cuts through the noise by interpreting **free-text goals**, mapping them to a CS skill taxonomy, and returning focused, high-quality recommendations that adapt as users engage.  

---

## What it does
- 🧠 **Understands goals with NLP** — extracts key topics from natural language input.  
- 🎯 **Recommends resources** with **content-based filtering** (semantic similarity).   
- 🤝 **Suggests next skills** using **collaborative filtering** with **k-means user grouping**.   
- 🔄 **Learns from feedback** — re-ranks items based on likes/engagement over time.  

---

## How it works (at a glance)
1. **Parse & profile:** NLP turns a user’s goal into a skill keyword profile.  
2. **Rank:** Compute similarity between the profile and resource embeddings for fast, high-precision matches.  
3. **Broaden:** Use **similar-user clusters (k-means)** to propose adjacent skills users like you have found valuable.   
4. **Refine:** Incorporate user feedback signals to adjust rankings on the fly.  

---

## Architecture
The platform is split into three services: **Frontend**, **Backend API**, and a **Recommender** service. Everything runs locally or in CI via Docker Compose.  

![System Architecture](/assets/img/projects/skill_boost_arch.png)  

> **Flow:** Frontend (React) → Backend API (FastAPI) → Recommender (Python, NLP & CF) → PostgreSQL  

---

## Highlights
- ✅ **Usability & relevance:** Lab testing with students indicated high usability and useful, on-target suggestions.   
- 🛠️ **Data resilience:** Used **synthetic datasets** to simulate realistic interactions for development and evaluation.   
- ♿ **Accessibility:** UI guided by WCAG and usability best practices.  

---

## Tech stack
- 💻 **Frontend:** React  
- ⚡ **API:** FastAPI  
- 🧩 **Recommender:** Python (NLP, content-based + collaborative filtering)  
- 🗄️ **DB:** MongoDB  
- 🐳 **DevOps:** Docker & Docker Compose  

---

## Roadmap
- ✨ **Smarter intent handling** (e.g., distinguishing *“already know AI → want Deep Learning”*).   
- 🔗 **Profile integrations** (e.g., LinkedIn) for dynamic skill paths.   
- 📊 **Progress tracking & exportable transcripts** to showcase skill growth.  

---

## Explore more
<div style="margin:1rem 0; display:flex; flex-wrap:wrap; gap:.75rem;">
  <a class="btn btn--primary" href="https://github.com/lucyinett/skill-boost" target="_blank" rel="noopener">View on GitHub</a>
  <a class="btn" href="/assets/docs/project.pdf" target="_blank" rel="noopener">Read the Full Paper</a>
</div>
