---
layout: default
title: 2026 Monthly Meeting
permalink: /DRAFT-monthly-meeting/
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
      {% for meeting in site.data.2026_monthly_meetings %}
      <tr>
      <td>  {{ meeting.date | date: "%B %d, %Y" }}
            {% if meeting.time %}
             <br><small>{{ meeting.time }}</small>
            {% endif %}</td>
      <td> {% for h in meeting.host %}
                {% if h.url %}
                <a href="{{ h.url }}">{{ h.name }}</a>{% unless forloop.last %}, {% endunless %}
                {% else %}
                {{ h.name }}{% unless forloop.last %}, {% endunless %}
                {% endif %}
            {% endfor %}
      </td>
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

