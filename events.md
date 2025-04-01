---
layout: default
title: Events
---
# Events

AusBIAS organises monthly meetings, usually online, where often one member will lead discussion of a paper, method, or problem of the day. We are also involved in hosting training courses at our various institutions, and supporting local conferences.

<h2>Upcoming Events</h2>

<div class="events-list">
  {% assign today = 'now' | date: '%Y-%m-%d' %}
  {% assign upcoming_events = site.data.events | sort: 'date' %}
  {% for event in upcoming_events %}
    {% if event.date >= today %}
      <div class="event-item">
        <div class="event-logo">
        {% if event.logo %}
            <img src="{{ event.logo | relative_url }}" alt="{{ event.title }} logo">
        {% endif %}
        </div>
        <div class="event-info">
          <strong>{{ event.title }}</strong><br>
          <small>{{ event.date | date: "%B %d, %Y" }} – {{ event.location }}</small><br>
          <a href="{{ event.url }}" target="_blank">Link</a>
          <p>{{ event.description }}</p>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>

<hr class="section-divider">
<h2>Past Events</h2>

<div class="events-list past-events">
  {% assign today = 'now' | date: '%Y-%m-%d' %}
  {% assign past_events = site.data.events | sort: 'date' | reverse %}
  {% assign past_events_filtered = past_events | where_exp: "event", "event.date < today" %}
  {% for event in past_events_filtered limit:3 %}
    <div class="event-item">
        <div class="event-logo">
        {% if event.logo %}
            <img src="{{ event.logo | relative_url }}" alt="{{ event.title }} logo">          
        {% endif %}
        </div>
        <div class="event-info">
          <strong>{{ event.title }}</strong><br>
          <small>{{ event.date | date: "%B %d, %Y" }} – {{ event.location }}</small><br>
          <a href="{{ event.url }}" target="_blank">More info</a>
          <p>{{ event.description }}</p>
        </div>
      </div>
{% endfor %}
</div>
