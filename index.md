---
layout: home
title: Torp i Ås Socken
---

## Förteckning

{% assign torp_pages = site.pages | where_exp: "item", "item.path contains 'torp/'" | sort: "nr" %}

Typ | Nr | Beskrivning
-- | -- | --
{% for item in torp_pages %}{{ item.typ }} | {{ item.nr }} | [{{ item.beskrivning }}]({{ item.url | relative_url }})
{% endfor %}
