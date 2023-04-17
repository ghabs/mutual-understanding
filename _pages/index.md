---
layout: page
title: Home
id: home
permalink: /
---


<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  A podcast where Divia Eden and Ben Goldhaber seek to understand their mutuals.
</p>

<strong>Recently Episodes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    {% if note.category == "podcast" %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
    {% endif %}
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
