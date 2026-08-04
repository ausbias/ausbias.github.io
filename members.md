---
layout: default
title: Members
---

<h2>Our Members</h2>

We respect the privacy and preferences of all our members. This directory includes only those who have chosen to be listed. If you're a member and would like to be included, [contact us](/contact/) and we’d love to add you.

<div class="member-grid">
  {% for member in site.data.members %}
    <a class="member-card" href="/members/{{ member.username }}/">
      {% if member.photo %}
        <img src="{{ member.photo | relative_url }}" alt="{{ member.name }}" class="member-card-photo">
      {% else %}
        <div class="member-card-photo member-card-photo-placeholder">{{ member.name | slice: 0 }}</div>
      {% endif %}
      <div class="member-card-name">{{ member.name }}</div>
      <div class="member-card-affiliation">{{ member.affiliation }}</div>
    </a>
  {% endfor %}
</div>
