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

<div class="container-md" style="margin-bottom:40px; ">
    <div id="shinyapps-big">
        {% for videoid in site.data.videos.videos %}
            <div class="video-tile" style="width=24rem;margin-bottom:10px">
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/{{ videoid }}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                </div>
            </div>
        {% endfor %}
    </div>
</div>

<style>
    #shinyapps-big {
        display: flex;
        flex-wrap: wrap;
    }

    .video-tile {
        width: calc(33.33% - 20px);
        margin: 10px;
        box-sizing: border-box;
    }

    .video-container {
        position: relative;
        width: 100%;
        padding-bottom: 56.25%; /* Aspect ratio 16:9 (9 / 16 = 0.5625) */
        overflow: hidden;
    }

    .video-container iframe {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border: 1px solid #ccc;
    }
</style>
