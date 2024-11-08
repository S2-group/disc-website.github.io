---
layout: page
title: Sustainable IT Lab
subtitle: A collaboration between ABN AMRO and the Vrije Universiteit Amsterdam
---

![image](/assets/img/lab-screenshots/vu-abn.png)


Sustainable IT - Lab is a collaboration between ABN AMRO and the Vrije Universiteit Amsterdam. This collaboration allows ABN AMRO software architects and decision makers to work closer with software sustainability researchers in academia, contribute to education and science, and collaborate in PhD- and Master-level research. Academics in turn gain a better understanding of how real-world software can be measured and re-designed to achieve sustainability goals.

**Contact:**
Prof. Dr. Patricia Lago p.lago@vu.nl (VU | S2 Research Group), Wiebren van der Zee (ABN AMRO | CIO – Sustainable IT)

_____

 <div class="container">
<h3>Theses</h3><br>
        <button class="scroll-button scroll-left" onclick="scrollLefty('thesis')">&#10094;</button>
        <ul class="post-list" id="thesis">
            {% assign sorted_posts = site.data.theses | sort: "year" | reverse%}
            {% for post in sorted_posts %}
            <li class="post">
                <!-- <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}"> -->
                    <div class= "thesis tile">
                        <h6>{{ post.title }}</h6>
                        <p>{{ post.author }} ({{ post.year }})</p>
                    </div>
            </li>
            {% endfor %}
        </ul>
        <button class="scroll-button scroll-right" onclick="scrollRight('thesis')">&#10095;</button>
    </div>
<div class="container">
<h3>Research Projects</h3><br>
        <button class="scroll-button scroll-left" onclick="scrollLefty('rps')">&#10094;</button>
        <ul class="post-list" id="rps">
            {% assign sorted_posts = site.data.research_projects | sort: "year" | reverse%}
            {% for post in sorted_posts %}
            <li class="post">
                <!-- <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}"> -->
                    <div class= "rp tile">
                        <h6>{{ post.title }}</h6>
                        <p>{{ post.author }} ({{ post.year }}) </p>
                    </div>
            </li>
            {% endfor %}
        </ul>
        <button class="scroll-button scroll-right" onclick="scrollRight('rps')">&#10095;</button>
    </div>

 <div class="container">
        <h3>Publications</h3><br>
        <button class="scroll-button scroll-left" onclick="scrollLefty('pubs')">&#10094;</button>
        <ul class="post-list" id="pubs">
            {% assign sorted_posts = site.data.publications | sort: "year" | reverse%}
            {% for post in sorted_posts %}
            <li class="post">
                <a href="{{ post.url }}">
                <!-- <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}"> -->
                    <div class= "pubs tile">
                        <h6>{{ post.title }} <img src="/assets/img/file.png" alt="Publication" style="width:auto; height:16px;"></h6>
                        <p>{{ post.authors }} ({{ post.year }}) </p>
                    </div>
                </a>
            </li>
            {% endfor %}
        </ul>
        <button class="scroll-button scroll-right" onclick="scrollRight('pubs')">&#10095;</button>
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
            list-style: none;
              gap: 1px; /* Add space between items */
            scroll-behavior: smooth; /* Smooth scrolling */
            padding-left: 20px; /* Space for the scroll buttons */
            padding-right: 15px; /* Space for the scroll buttons */
            overflow-x: auto;
            /* Hide scrollbar on WebKit browsers (Chrome, Safari) */
            -webkit-overflow-scrolling: touch;
            scrollbar-width: none; /* Firefox */

        }
        .post {
            margin-right: 10px
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
            background-color: rgba(0, 71, 65, 0.7); /* Semi-transparent background for readability */
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
            top: 30%; /* Center vertically */
            height: 170px;
            /* background-color: rgba(0, 110, 185, 0.5); */
            background-color: rgba(255, 255, 255, 1);
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

        .tile-container {
            display: flex;                /* Use flexbox for horizontal layout */
            gap: 20px;                   /* Space between tiles */
            overflow-x: none;            /* Enable horizontal scrolling */
            max-width: 100%;             /* Ensure container fits within screen width */
            padding-bottom: 10px;        /* Space for scrollbar */
            margin-bottom: 30px;         /* Space below the container */
        }

        .tile {
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 300px;                /* Fixed width for tiles */
            height: 150px;               /* Fixed height for tiles */
            padding: 10px;               /* Inner padding */
            text-align: left;            /* Text alignment */
            display: flex;               /* Flexbox for inner content */
            flex-direction: column;      /* Arrange content vertically */
            flex-shrink: 0;              /* Prevent shrinking */
        }

        .thesis {
            background-color: rgba(22, 140, 119, .2);  /* Color for thesis tiles */
        }

        .rp {
            background-color: rgba(242, 187, 22, .2);   /* Color for research project tiles */
        }
        .pubs {
            background-color: rgba(4, 157, 217, .2)
        }
        /* .pubs h6{
            text-decoration: underline;
        } */
        .tile h3 {
            font-size: 1.1em;            /* Title font size */
            color: #333;                 /* Title color */
            margin: 0;                   /* Remove default margin */
        }

        .tile p {
            font-size: 0.9em;            /* Author and year font size */
            color: #666;                 /* Author and year color */
            margin-top: auto;            /* Push to bottom of tile */
        }
       
       .post a{
        color: #000;
       }
       
        
        
    </style>