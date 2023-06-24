---
layout: projects
title: Drops of knowledge
subtitle: Short videos on Sustainability and beyond
css:
- /assets/css/index.css
ext-css:
- //fonts.googleapis.com/css?family=Roboto:400,700
js:
- /assets/js/index.js
ext-js:
- //cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
---

<div id="portfolio-out" class="page-section grey-section">
  <div id="portfolio">
    <div id="shinyapps-big">
      {% for video in site.data.videos %}
	    <div class="shinyapp">
            <img class="appimg" src="{{ site.url }}/assets/img/video-screenshots/{{ video.img }}" alt="" />
            <div class="apptitle">{{ video.title }}</div>
            <div class="appdesc">{{ video.description }}</div>
        </div>
	  {% endfor %}
    </div>
  </div>
</div>
