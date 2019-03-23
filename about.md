---
layout: default
title: About John
---
<hr>
<p align="justify">John. But some of his friends call him Ice. John is an undergrad who's set to graduate with a BS in Computer Science this year (2018), in May. Other than being busy in all things computer science, John likes to spend his time playing the piano, guitar, reading non-fiction books, and eating lasagnas.</p>
<center>
  <p><img src="https://avatars1.githubusercontent.com/u/12871105"/></p>
</center>
  
<div class="pagination">
  {% if site.owner.linkedin %}
    <a href="{{ site.owner.linkedin }}" class="social-media-icons"><i class="fa fa-2x fa-linkedin" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.email %}
    <a href="mailto:{{ site.owner.email }}" class="social-media-icons"><i class="fa fa-2x fa-envelope" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.twitter %}
    <a href="{{ site.owner.twitter }}" class="social-media-icons"><i class="fa fa-2x fa-twitter" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.github %}
    <a href="{{ site.owner.github }}" class="social-media-icons"><i class="fa fa-2x fa-github" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.stackexchange %}
    <a href="{{ site.owner.stackexchange }}" class="social-media-icons"><i class="fa fa-2x fa-stack-overflow" aria-hidden="true"></i></a>
  {% endif %}
</div>
