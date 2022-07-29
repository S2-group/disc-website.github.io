---
layout: projects
title: Projects
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
      {% for app in site.data.projects %}
	    <div class="shinyapp">
          <a class="applink" href="{{ app.url }}" target="_blank">
            <img class="appimg" src="/assets/img/project-screenshots/{{ app.img }}" />
            <div class="apptitle">{{ app.title }}</div>
            <div class="appdesc">{{ app.description }}</div>
          </a>
        </div>
	  {% endfor %}
    </div>
  </div>
</div>
