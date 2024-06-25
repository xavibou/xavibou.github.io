---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
I am a PhD Candidate in Image Processing and Computer Vision at Centre Borelli, Ecole Normale Superieure Paris-Saclay

Research
======
<table>
  {% for post in site.posts %}
    {% for cat in post.categories %}
      {% if cat == 'research' %}
        <tr>
          <td style="padding:2.5%;width:25%;vertical-align:middle;min-width:120px">
            <img src="{{ post.image }}" alt="project image" style="width:auto; height:auto; max-width:100%;" />
          </td>
          <td style="padding:2.5%;width:75%;vertical-align:middle">
            <h3>{{ post.title }}</h3>
            <br>
            {{ post.authors }}
            <br>
            <em>{{ post.venue }}</em>, {{ post.date | date: "%Y" }}
            <br>
            {% if post.paper %}
              <a href="{{ post.paper }}">paper</a> /
            {% endif %}
            {% if post.video %}
              <a href="{{ post.video }}">video</a> /
            {% endif %}
            {% if post.code %}
              <a href="{{ post.code }}">code</a> /
            {% endif %}
            {% if post.poster %}
              <a href="{{ post.poster }}">poster</a> /
            {% endif %}
            {% if post.slides %}
              <a href="{{ post.slides }}">slides</a> /
            {% endif %}
            <p></p>
            {{ post.excerpt }}
          </td>
        </tr>
      {% endif %}
    {% endfor %}
  {% endfor %}
</table>
