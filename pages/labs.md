---
layout: labs
title: Labs
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
      {% for lab in site.data.labs %}
	    <div class="shinyapp" style="width:65rem">
          <a class="applink" href="{{ lab.url }}" target="_blank">
            <img class="appimg" src="{{ site.url }}/assets/img/lab-screenshots/{{ lab.img }}" style="width: 10%" alt="" />
            <div class="apptitle">{{ lab.title }}</div>
            <div class="appdesc">{{ lab.description }}</div>
            <div class="appdesc">{{ lab.details }}</div>
            <div class="appdesc">{{ lab.contact }}</div>
          </a>
        </div>
	  {% endfor %}
    </div>
  </div>
</div>
