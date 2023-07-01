---
layout: projects
title: Projects
subtitle: Our research at a glance
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
      {% for project in site.data.projects %}
	    <div class="shinyapp">
          <a class="applink" href="{{ project.url }}" target="_blank">
            <img class="appimg" src="{{ site.url }}/assets/img/project-screenshots/{{ project.img }}" alt="" />
            <div class="apptitle">{{ project.title }}</div>
            <div class="appdesc">{{ project.description }}</div>
          </a>
        </div>
	  {% endfor %}
    </div>
  </div>
</div>
