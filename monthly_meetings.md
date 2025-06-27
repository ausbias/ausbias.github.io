---
layout: default
title: Monthly Meeting
permalink: /monthly-meeting/
---

<h1>Monthly Meetings</h1>

<p>Below is a summary of upcoming and past monthly meetings. If you would like to nominate a speaker or suggest a discussion topic, please <a href="/contact/">contact us</a>.</p>

<table class="meeting-table">
  <thead>
    <tr>
      <th>Date</th>
      <th>Speakers</th>
      <th>Discussion</th>
      <th>Contact</th>
    </tr>
  </thead>
  <tbody>
      {% for meeting in site.data.monthly_meetings %}
      <tr>
      <td>{{ meeting.date }}</td>
      <td>
            {% for sp in meeting.speakers %}
                {% if sp.url %}
                <a href="{{ sp.url }}">{{ sp.name }}</a>{% unless forloop.last %}, {% endunless %}
                {% else %}
                {{ sp.name }}{% unless forloop.last %}, {% endunless %}
                {% endif %}
            {% endfor %}
      </td>
      <td>{{ meeting.discussion }}</td>
      <td><a href="{{ meeting.contact }}">Nominate</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>

