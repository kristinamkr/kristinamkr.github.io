---
layout: default
title: archive
permalink: /archive
---

<div class="archive">
<nav>
    <ul>
    {% for post in site.posts %}
    <h3>
       <li id="archive-links"><a href="{{ post.url }}">{{ post.title }} - {{ post.date | date: "%d %b %Y" | downcase}}</a></li>
    </h3>
    {% endfor %}
   </ul>
</nav>
</div>
