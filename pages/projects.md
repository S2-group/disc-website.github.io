---
layout: projects
title: Projects
subtitle: Research Projects that engage with different aspects of digital sustainability

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
        {% if project.status == "current"%}
        <div class="shinyapp">
            <a class="applink" href="{{ project.url }}" target="_blank">
              <img class="appimg" src="{{ site.url }}/assets/img/project-screenshots/{{ project.img }}" alt="" />
              <div class="apptitle">{{ project.title }}</div>
              <div class="appdesc">{{ project.description }}</div>
            </a>
          </div>
          {% endif %}
	  {% endfor %}
    </div>
    {% assign past_projects = site.data.projects | where: "status", "past" %}
    {% if past_projects.size > 0 %}
    <hr>
      <h3 style="text-align:left; margin:40px">Past Projects</h3>
        {% for project in past_projects %}
          {% if project.status == "past"%}
          <div class="shinyapp" style="text-align:left; margin-left:40px; margin-top:10px;">
                <a href="{{ project.url }}" target="_blank">
                  <div class="apptitle">{{ project.title }}</div>
                </a>
          </div>
          {% endif %}
        {% endfor %}
    {% endif %}
  </div>
</div>
