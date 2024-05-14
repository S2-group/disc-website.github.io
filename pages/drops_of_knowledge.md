---
layout: projects
title: Drops of knowledge
subtitle: Short videos on Sustainability and beyond
css:
- /assets/css/index.css
ext-css:
- //fonts.googleapis.com/css?family=Roboto:400,700
ext-js:
- //cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
---

  <div id="drops">
      {% for videoid in site.data.videos.videos %}
            <div class="video-tile">
                <iframe src="https://www.youtube.com/embed/{{ videoid }}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
  	  {% endfor %}
    </div>
  <style>
        #drops {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .video-tile {
            width: calc(33.33% - 10px);
            margin-bottom: 20px;
            margin-left: 10px;
            margin-right: 10px;
            box-sizing: border-box;
        }
        .video-tile iframe {
            width: 100%;
            height: 280px; 
            border: 1px solid #ccc; 
        }
    </style>