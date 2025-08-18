---
layout: single
title: "Projects"
permalink: /projects/
classes: wide
author_profile: true
---

{% assign items = site.projects %}
{% include documents-collection.html
   entries=items
   sort_by="title"
   sort_order="forward"
   type="grid"   # or "list"
%}
