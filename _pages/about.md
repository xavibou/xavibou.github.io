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
<table style="border-collapse: collapse; width: 100%; border: none;">
  {% for post in site.posts %}
    {% for cat in post.categories %}
      {% if cat == 'research' %}
        <tr style="border: none;">
          <td style="padding:1%;width:35%;vertical-align:middle;min-width:200px;border: none;">
            <img src="{{ post.image }}" alt="project image" style="width:100%; height:auto; max-width:100%;" />
          </td>
          <td style="padding:1%;width:65%;vertical-align:middle;border: none;">
            <h3 style="margin: 5px 0;">{{ post.title }}</h3>
            <p style="margin: 5px 0;">{{ post.authors }}</p>
            <p style="margin: 5px 0;"><em>{{ post.venue }}</em>, {{ post.date | date: "%Y" }}</p>
            <p style="margin: 5px 0;">
              {% if post.paper %}<a href="{{ post.paper }}">paper</a> / {% endif %}
              {% if post.video %}<a href="{{ post.video }}">video</a> / {% endif %}
              {% if post.code %}<a href="{{ post.code }}">code</a> / {% endif %}
              {% if post.poster %}<a href="{{ post.poster }}">poster</a> / {% endif %}
              {% if post.slides %}<a href="{{ post.slides }}">slides</a> / {% endif %}
            </p>
            <p style="margin: 5px 0;">{{ post.excerpt }}</p>
          </td>
        </tr>
      {% endif %}
    {% endfor %}
  {% endfor %}
</table>
