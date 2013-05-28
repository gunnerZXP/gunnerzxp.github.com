---
layout: page
title: Vector
tagline:
---
{% include JB/setup %}


<ul class="posts">
  {% for post in site.posts limit:12 %}
    <li>
      <span>
        {{ post.date | date_to_string }}
      </span> 
        &raquo; 
      <a href="{{ BASE_PATH }}{{ post.url }}">
        {{ post.title }}
      </a>
    </li>
  {% endfor %}
</ul>


<h5><a href="/archive.html"> >>Read more.</a></h5>


