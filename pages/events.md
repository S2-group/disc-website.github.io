---
layout: events
title: Events
---

<style>

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative; /* Relative positioning for scroll buttons */
        }
        .post-list {
            display: flex;
            flex-wrap: nowrap; /* Prevent items from wrapping */
            overflow-x: auto; /* Enable horizontal scrolling */
            list-style: none;
              gap: 1px; /* Add space between items */
            scroll-behavior: smooth; /* Smooth scrolling */
            padding-left: 15px; /* Space for the scroll buttons */
            padding-right: 15px; /* Space for the scroll buttons */

        }
        .post {
            position: relative; /* Allow absolute positioning of title */
            border: 1px solid #ccc;
            /* border-radius: 5px; */
            min-width: 250px; /* Minimum width for each post */
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            overflow: hidden; /* Prevent overflow */
            transition: transform 0.3s;
            height: 200px; /* Fixed height for square */
        }
        .post:hover {
            transform: translateY(-2px);
        }
        .post img {
            width: 100%;
            height: 100%; /* Set height to 100% to fill the container */
            object-fit: cover; /* Ensure the image covers the space */
        }
        .post-title {
            width: 100%;
            height: 100%; /* Set height to 100% to fill the container */
            position: absolute; /* Position title over the image */
            bottom: 0px; /* Position title closer to the bottom */
            color: white;
            text-align: top;
            text-decoration: none; 
            font-size: x-large;
            padding: 5px 10px;
        }
        .cocktail-post-title{
            background-color: rgba(0, 29, 69, 0.4); /* Semi-transparent background for readability */
        }
        .lecture-post-title{
            background-color: rgba(30, 0, 59, 0.407); /* Semi-transparent background for readability */
        }
        .other-post-title{
            background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent background for readability */
        }
        .post-date {
            width: 100%;
            height: 20%; /* Set height to 100% to fill the container */
            position: absolute; /* Position title over the image */
            bottom: 0px; /* Position title closer to the bottom */
            color: white;
            background-color: rgba(1, 27, 43, 0.5); /* Semi-transparent background for readability */
            text-align: bottom;
            text-decoration: none; 
            font-size: large;
            padding: 5px 0 0 10px;
        }
        .scroll-button {
            position: absolute;
            top: 50%; /* Center vertically */
            /* background-color: rgba(0, 110, 185, 0.5); */
            background-color: rgba(255, 255, 255, 0);
            color: black;
            border: none;
            padding: 10px;
            cursor: pointer;
            /* border-radius: 5px; */
            z-index: 1; /* Ensure buttons are above other elements */
        }
        .scroll-left {
            left: 0;
        }
        .scroll-right {
            right: 0;
        }
    </style>
<div>

{% assign date_format = site.date_format | default: "%B %-d, %Y" %}

<div class="container-md">
        <div class="container">
            <h1>Distinguished Lectures</h1><br>
            <button class="scroll-button scroll-left" onclick="scrollLefty('distinguished-lecture')">&#10094;</button>
            <ul class="post-list" id="distinguished-lecture">
                {% assign sorted_posts = site.posts | sort: "event-date" | reverse%}
                {% for post in sorted_posts %}
                    {% if post.event-type == "distinguished-lecture" %}
                        <li class="post">
                            <a href="{{ post.url }}">
                            <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}">
                            <div>
                                <div class="post-title lecture-post-title">
                                    {{ post.title | truncate: 50, "..." }}<br>
                                </div>
                                <div class="post-date">
                                    {{post.event-date  | date: date_format}}
                                </div>
                            </div>
                            </a>
                        </li>
                    {% endif %}
                {% endfor %}
            </ul>
            <button class="scroll-button scroll-right" onclick="scrollRight('distinguished-lecture')">&#10095;</button>
        </div>

<div class="container-md">
    <div class="container">
        <h1>Research Cocktails</h1><br>
        <button class="scroll-button scroll-left" onclick="scrollLefty('cocktails')">&#10094;</button>
        <ul class="post-list" id="cocktails">
            {% assign sorted_posts = site.posts | sort: "event-date" | reverse%}
            {% for post in sorted_posts %}
                {% if post.event-type == "cocktail" %}
                    <li class="post">
                        <a href="{{ post.url }}">
                        <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}">
                        <div>
                            <div class="post-title cocktail-post-title">
                                {{ post.title | truncate: 50, "..." }}<br>
                            </div>
                            <div class="post-date">
                                {{post.event-date  | date: date_format}}
                            </div>
                        </div>
                        </a>
                    </li>
                {% endif %}
            {% endfor %}
        </ul>
        <button class="scroll-button scroll-right" onclick="scrollRight('cocktails')">&#10095;</button>
    </div>

   

<div class="container">
        <h1>Other Events</h1><br>
        <button class="scroll-button scroll-left" onclick="scrollLefty('discevents')">&#10094;</button>
        <ul class="post-list" id="discevents">
            {% assign sorted_posts = site.posts | sort: "event-date" | reverse%}
            {% for post in sorted_posts %}
                {% if post.event-type == "other" %}
                    <li class="post">
                        <a href="{{ post.url }}">
                        <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}">
                        <div>
                            <div class="post-title other-post-title">
                                {{ post.title | truncate: 50, "..." }}<br>
                            </div>
                            <div class="post-date">
                                {{post.event-date  | date: date_format}}
                            </div>
                        </div>
                        </a>
                    </li>
                {% endif %}
            {% endfor %}
        </ul>
        <button class="scroll-button scroll-right" onclick="scrollRight('discevents')">&#10095;</button>
    </div>

</div>
</div>
<script>
    function scrollLefty(id) {
        const postList = document.getElementById(id);
        postList.scrollBy({
            top: 0,
            left: -200, // Scroll left by 200px
            behavior: 'smooth'
        });
    }

    function scrollRight(id) {
        const postList = document.getElementById(id);
        postList.scrollBy({
            top: 0,
            left: 200, // Scroll right by 200px
            behavior: 'smooth'
        });
    }
</script>
