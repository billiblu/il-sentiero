---
layout: default
title: Iniziative ed eventi
description: Iniziative organizzate o partecipate da ASD Il Sentiero.
permalink: /iniziative-eventi/
---

<section class="page">
  <div>
    <p class="eyebrow">Appuntamenti</p>
    <h1>Iniziative ed eventi</h1>
    <p class="lead">Incontri, seminari e iniziative organizzate dall'associazione o a cui partecipiamo.</p>

    {% assign published_events = site.events | where_exp: "event", "event.published != false" | sort: 'date' | reverse %}
    {% if published_events.size > 0 %}
    <ul class="event-list">
      {% for event in published_events %}
      <li>
        {% if event.date %}<span class="event-date">{{ event.date | date: "%d/%m/%Y" }}</span>{% endif %}
        <strong>{{ event.title }}</strong>
        {% if event.location %}<span> — {{ event.location }}</span>{% endif %}
        {% if event.excerpt %}<p>{{ event.excerpt }}</p>{% endif %}
      </li>
      {% endfor %}
    </ul>
    {% else %}
    <div class="callout"><p>Le prossime iniziative saranno pubblicate qui.</p></div>
    {% endif %}
  </div>
</section>
