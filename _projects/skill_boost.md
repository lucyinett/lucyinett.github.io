---
title: "Skill Boost"
excerpt: "NLP + content-based + collaborative filtering to guide student skill growth."
image: /assets/img/projects/skill-boost-page.png   # optional card image
permalink: /projects/skill-boost/
classes: wide
layout: single
author_profile: true
---


**Skill Boost** is a full-stack recommendation platform that helps Computer Science learners discover the **right skills, courses, and events** at the right time.  
It combines **NLP** to understand goals, **content-based ranking** for relevant resources, and **collaborative filtering** to surface skills liked by similar users, all wrapped in a clean web app and containerised for easy deployment.  

I created this tool to help learners enhance their skills through available online material. Skill Boost interprets **free-text goals**, mapping them to a CS skill and returning focused, high-quality recommendations that are tailored specifically to the Universitly of Warwick modules they have taken.  

## Key Features
-  **Understands goals with NLP** — extracts key topics from natural language input and finds context behind domain specific terms.  
- **Recommends resources** with **content-based filtering** (semantic similarity) based on similar users skills.   
- **Suggests next skills** using **collaborative filtering** with **k-means user grouping** based on similar users favourite courses.   
- **Learns from feedback** — re-ranks items based on likes/engagement over time.  

---

## How it works (at a glance)
1. **Parse & profile:** NLP turns a user’s goal into a skill keyword profile.  
2. **Rank:** Compute similarity between the profile and resource embeddings for fast, high-precision matches.  
3. **Broaden:** Use **similar-user clusters (k-means)** to propose adjacent skills users like you have found valuable.   
4. **Refine:** Incorporate user feedback signals to adjust rankings on the fly.  

---

## Architecture
The platform is split into three services: **Frontend**, **Backend API**, and a **Recommender** service. Everything runs locally or in CI via Docker Compose.  
> **Flow:** Frontend (React) → Backend API (FastAPI) → Recommender (Python, NLP & CF) → MongoDB  

![System Architecture](/assets/img/projects/skill-boost-arch.png)  


---

## Highlights
- **Usability & relevance:** Lab testing with students indicated high usability and useful, on-target suggestions.   
- **Data resilience:** Used **synthetic datasets** to simulate realistic interactions for development and evaluation.   
- **Accessibility:** UI guided by WCAG and usability best practices.  

## Tech stack
- **Frontend:** React  
- **API:** FastAPI  
- **Recommender:** Python (NLP, content-based + collaborative filtering)  
- **DB:** MongoDB  
- **DevOps:** Docker & Docker Compose  

---
## Overview
This project allowed me to implement classic machine learning techniques into a real life scenario, allowing me to test out the performances of these techniques and how they interacted with eachother when combined together. This also introduced me to new tools and libraries such as MongoDB and React. This project demonstrated the power of simple, classic machine learning techniques in a real world context.

## Explore more
<div style="margin:1rem 0; display:flex; flex-wrap:wrap; gap:.75rem;">
  <a class="btn btn--primary" href="https://github.com/lucyinett/skill-boost" target="_blank" rel="noopener">View on GitHub</a>
  <a class="btn" href="/assets/docs/project.pdf" target="_blank" rel="noopener">Read the Full Paper</a>
</div>
