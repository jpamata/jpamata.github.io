---
layout: default
title: Archives
---

<div class="listing">

<ul class="tags-box">

{% if site.posts != empty %}

{% for post in site.posts %}
{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% unless year == this_year %}
{% assign year = this_year %}
{% unless post == site.posts.first %}
{% endunless %}
<p><strong>{{ year }}</strong></p>
{% endunless %}
<time datetime="{{ post.date | date:"%Y-%m-%d" }}">
{{ post.date | date:"%Y-%m-%d" }}
</time>
&raquo; <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title | capitalize }}</a><br />
{% endfor %}

{% else %}

<span>No posts</span>

{% endif %}

</ul>
</div>
<hr/>
<p align="center">&nbsp;&nbsp;Yours truly,</p>
<div style="display: flex; justify-content: center;">
  <img src="http://johnamata.com/assets/transparent-sign.png"> 
</div>
