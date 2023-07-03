---
layout: labs
title: Talent Hub
subtitle: Our talent labs
description: Talent Labs are geared around a common theme. They provide structure for internships and short-term projects between companies and students supervised by DiSC researchers. Talent Labs also organize cross-fertilization events for knowledge sharing.
css:
- /assets/css/index.css
ext-css:
- //fonts.googleapis.com/css?family=Roboto:400,700
ext-js:
- //cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
---

<div id="portfolio-out" class="page-section grey-section">
  <div id="portfolio">
    <div id="shinyapps-big"> 
      {% for lab in site.data.talent_labs %}
	    <div class="shinyapp" style="cursor: pointer; width:65rem; background-color:#e6faff;" onclick="window.location='{{ lab.url }}'">
            <img class="appimg" src="{{ site.url }}/assets/img/lab-screenshots/{{ lab.img }}" style="width: {{ lab.img-width }}; color:#e6faff; filter: opacity(0.7) ;" alt="" />
            <div class="apptitle">{{ lab.title }}</div>
            <div class="appdesc">{{ lab.description }}</div>
            <div class="appdesc">{{ lab.details }}</div>
            <div class="appdesc">{{ lab.contact }}</div>
        </div>
	  {% endfor %}
    </div>
  </div>
</div>
