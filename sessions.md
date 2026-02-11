---
layout: page
title: Sessions
description: Session summaries and campaign chronicle
permalink: /sessions/
---

Below are session summaries documenting the convoy's desperate journey west through Death March, ordered chronologically.

{% assign items = site.sessions | sort: 'index' %}

{% if items.size > 0 %}
<ul>
{% for doc in items %}
  <li><strong>Session {{ doc.index }}:</strong> <a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% else %}
<p><em>No sessions have been recorded yet. Check back after the convoy rolls out!</em></p>
{% endif %}

---

*Summaries are added after each session to track the convoy's progress, losses, and hard-won miles.*
