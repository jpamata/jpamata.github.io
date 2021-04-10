---
layout: default
title: About John
---

<p align="justify">
<big><strong>Hello!</strong></big> I'm John, but some of my friends call me either Ice or JP.
</p>

<p>Feel free to send emails at &lt;<code>j+p@johnamata.com</code>&gt;</p> 

<p>see some <a href="#">projects</a>; you can find me <a href="{{ "/elsewhere" | prepend: site.url }}">elsewhere</a></p>

<p><img src="/photos/johnamata2.png"></p>
  
<p>you can find me <a href="{{ "/elsewhere" | prepend: site.url }}">elsewhere</a></p>
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
