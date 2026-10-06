---
layout: prism
permalink: /
title: "About"
profile: true
redirect_from:
  - /about/
  - /about.html
---

<section class="section bio" markdown="1">

## About Me

I am a third-year Ph.D. student in Computer Science at [Arizona State University](https://scai.engineering.asu.edu/), advised by [Prof. Hua Wei](https://www.public.asu.edu/~hwei27/index.html). Before ASU, I received my M.Sc. in Computer Science from the [University of British Columbia](https://ok.ubc.ca/) under the guidance of [Prof. Yong Gao](https://cmps-people.ok.ubc.ca/yongg/), and my B.Eng. in Computer Science from Beijing Jiaotong University.

My research aims to make large language models and LLM agents **reliable enough for the real world**:

- **Uncertainty quantification in LLMs**: estimating how confident a model should be in its outputs and reasoning steps, and using these estimates to improve reasoning performance and reliability.
- **Learning and adaptation in LLM agents**: building agents that keep learning from interaction, acquire and refine reusable skills, and coordinate well in multi-agent systems.

<p class="callout">I am available for research internships in <strong>Winter 2027</strong> and <strong>Summer 2027</strong>. Feel free to reach out!</p>

</section>

<section class="section">
  <h2>News</h2>
  {% include prism/news.html %}
</section>

<section class="section">
  <div class="section-head">
    <h2>Selected Publications</h2>
    <a href="{{ site.baseurl }}/publications/">View all →</a>
  </div>
  <div class="pub-list">
    {% for pub in site.data.publications %}{% if pub.selected %}
      {% include prism/pub-card.html pub=pub hide_venue_full=true %}
    {% endif %}{% endfor %}
  </div>
</section>
