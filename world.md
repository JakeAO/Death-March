---
layout: page
title: World
description: Setting, factions, and what remains in the zombie apocalypse
permalink: /world/
---

This page contains all player-facing information about the world of Death March – the apocalypse, the journey west, factions encountered, and the desperate hope called Rockies Haven.

Information is added here as it's discovered during the campaign.

{% assign groups = site.world | group_by: "topic" | sort: 'name' %}
{% for group in groups %}

  {% if group.items.size > 0 %}
  <h2>{{ group.name }}</h2>
  <ul>
  {% assign items = group.items | sort: 'title' %}
  {% for doc in items %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

*This section grows as the convoy pushes west and encounters the remnants of civilization.*
