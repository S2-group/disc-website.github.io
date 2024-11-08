---
layout: labs
title: Labs
subtitle: Our long-term collaborations
description: Labs are funded by external companies. They provide structure for their strategic collaboration with DiSC researchers and young talents, for PhD research and Master-level research.
css:
- /assets/css/index.css
ext-css:
- //fonts.googleapis.com/css?family=Roboto:400,700
ext-js:
- //cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
---

<div id="portfolio-out">
  <div id="portfolio">
    <div id="shinyapps-big"> 
      {% for lab in site.data.labs %}
	    <div class="shinyapp" style="background-color:#e6ffe7; ">
          <a class="applink" href="{{ lab.url }}" target="_blank">
            <img class="appimg" src="{{ site.url }}/assets/img/lab-screenshots/{{ lab.img }}" style="width: {{ lab.img-width }};" alt="" />
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
