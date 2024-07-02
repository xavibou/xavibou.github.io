---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
  body {
    font-size: 0.9em;
  }
  h1, h2, h3, h4, h5, h6 {
    font-size: 1.3em;
  }
  .research-section {
    font-size: 1.2em; /* Adjust the font size as needed */
  }
</style>

I am a PhD Candidate in Image Processing and Computer Vision at [ENS Paris-Saclay](https://ens-paris-saclay.fr/). I work on change detection on satellite imagery and video. I am interested in problems with limited annotations, i.e. unsupervised, few-shot and self-supervised learning methods.

News
======
- **April 2024**: Our paper [Exploring Robust Features for Few-Shot Object Detection in Satellite Imagery](https://arxiv.org/abs/2403.05381) has been accepted at the EarthVision Workshop at CVPR24.
- **March 2024**: Our paper [Portraying the Need for Temporal Data in Flood Detection via Sentinel-1](https://arxiv.org/abs/2403.03671) has been accepted at IGARSS24.
- **March 2023**: I am visiting [Guillermo Sapiro's group](https://ece.duke.edu/faculty/guillermo-sapiro) at Duke University with a team led by [Jean-Michel Morel](https://sites.google.com/site/jeanmichelmorelcmlaenscachan/).
- **November 2022**: I am starting my PhD at [Centre Borelli](https://centreborelli.ens-paris-saclay.fr/en), ENS Paris-Saclay, advised by [Rafael Grompone](https://www.rafaelgrompone.org/) and [Thibaud Ehret](https://tehret.github.io/).
- **February 2022**: I am joining the Centre Borelli as a research intern, advised by [Jean-Michel Morel](https://sites.google.com/site/jeanmichelmorelcmlaenscachan/) and [Gabriele Facciolo](https://dev.ipol.im/~facciolo/).

Research
======
<div class="research-section">
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
                {% assign links = "" %}
                {% if post.paper %}{% assign links = links | append: '<a href="' | append: post.paper | append: '">paper</a>' %}{% endif %}
                {% if post.video %}{% if links != "" %}{% assign links = links | append: ' / ' %}{% endif %}{% assign links = links | append: '<a href="' | append: post.video | append: '">video</a>' %}{% endif %}
                {% if post.code %}{% if links != "" %}{% assign links = links | append: ' / ' %}{% endif %}{% assign links = links | append: '<a href="' | append: post.code | append: '">code</a>' %}{% endif %}
                {% if post.poster %}{% if links != "" %}{% assign links = links | append: ' / ' %}{% endif %}{% assign links = links | append: '<a href="' | append: post.poster | append: '">poster</a>' %}{% endif %}
                {% if post.slides %}{% if links != "" %}{% assign links = links | append: ' / ' %}{% endif %}{% assign links = links | append: '<a href="' | append: post.slides | append: '">slides</a>' %}{% endif %}
                {{ links | strip_newlines }}
              </p>
              <p style="margin: 5px 0;">{{ post.excerpt }}</p>
            </td>
          </tr>
        {% endif %}
      {% endfor %}
    {% endfor %}
  </table>
</div>