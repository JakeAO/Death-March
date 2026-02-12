---
layout: page
title: Rules & Info
description: Savage Worlds rules, survival mechanics, vehicle rules, and cheat sheets
permalink: /info/
---

This page contains player-facing rules clarifications, cheat sheets, and game mechanics for the Death March campaign.

## Core Resources

- **[Core Rulebook]({{ '/info/mechanics/rulebook/' | relative_url }})** – The core rulebook (Digital Copy)
- **[Savage Worlds Adventure Edition](https://peginc.com/product/savage-worlds-adventure-edition-core-rules-pdf-swade/)** - Rulebook from Pinnacle Entertainment
- **[Savage Worlds Test Drive](https://peginc.com/store/deadlands-the-weird-west-blood-on-the-range-savage-worlds-test-drive-swade/)** – Free quick-start rules
- **[Character Sheet PDF](https://peginc.com/wp-content/uploads/2019/09/SWADE_Character_Sheet.pdf)** - Official, editable character sheet

## Quick Reference

Below are campaign-specific resources and rules clarifications, organized by topic.

{% assign groups = site.info | group_by: "topic" | sort_natural: "name" %}
{% for group in groups %}

  {% assign has_content = false %}
  {% for doc in group.items %}
  {% unless doc.tags contains "nested" %}
  {% assign has_content = true %}
  {% endunless %}
  {% endfor %}

  {% if has_content %}
  <h3>{{ group.name }}</h3>
  <ul>
  {% assign items = group.items | sort: "title" %}
  {% for doc in items %}
  {% unless doc.tags contains "nested" %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endunless %}
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

*New to Savage Worlds? Check out the quick reference and new player advice pages to get started.*
