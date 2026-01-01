---
layout: default
title: 2025 Monthly Meetings
permalink: /2025-meetings/
---

<h1>Monthly Meetings</h1>

<p>Below is a summary of upcoming and past monthly meetings. If you would like to nominate a speaker or suggest a discussion topic, please <a href="/contact/">contact us</a>. Zoom link to the meeting will be advertised on the google group mailing list or via the LMA email newsletter. </p>

<table class="meeting-table">
  <thead>
    <tr>
      <th>Date</th>
      <th>Speaker(s)</th>
      <th>Discussion Topic(s)</th>
    </tr>
  </thead>
  <tbody>
      {% for meeting in site.data.2025_monthly_meetings %}
      <tr>
      <td>  {{ meeting.date | date: "%B %d, %Y" }}
            {% if meeting.time %}
             <br><small>{{ meeting.time }}</small>
            {% endif %}</td>
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
    </tr>
    {% endfor %}
  </tbody>
</table>



