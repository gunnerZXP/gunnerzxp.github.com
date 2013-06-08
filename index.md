---
layout: page
title: Vector
tagline:
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts limit:8 %}
  <section>
    <li>
      <span>
        {{ post.date | date_to_string }}
      </span> 
        &raquo; 
        {{ post.title }}
    </li>
         {{ post.content  | | split:'<!--break-->'|first }} 
      <a href="{{ BASE_PATH }}{{ post.url }}">全文阅读&raquo;</a>
  </section>
  {% endfor %}

</ul>



<a href="archive.html">Read more</a>