---
layout: single
title: "Posts as Blog"
permalink: /blog-list/
author_profile: true
---



<div class="posts">

  {% for post in site.posts  %}

  <div class="post">

    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <span class="post-date">- {{ post.date | date_to_string }}</span>

{% for t in post.tags %}
  <a class="button" href="{{ site.baseurl }}/tag/#{{t | downcase | replace:" ","-" }}">{{ t | downcase }}</a>
{% endfor %}
  
    {{ post.content }}
  
  </div>
  {% endfor %}
</div>
