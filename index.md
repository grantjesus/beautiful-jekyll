---
layout: page
title: 
subtitle: May Grant be with you
use-site-title: true
bigimg: "img/lastsupper.jpg"
---

<h1 class="text-center">Personal Projects</h1>
<div class="spacer"></div>

<p></p>

<div class="row text-center">
  <div class="col-md-4 col-md-offset-0 col-sm-4 col-sm-offset-0 col-xs-12 col-xs-offset-0 text-center">
    <div class="project-card">
      <a target="_blank" href="https://github.com/tommy1019/Totality" class="project-link">
        <span class="fa-stack fa-3x">
          <i class="fa fa-circle fa-stack-2x stack-color"></i>
          <i class="fa fa-gamepad fa-stack-1x fa-inverse"></i>
        </span>
        <h4>Totality</h4>
        <hr class="seperator">
        <p class="text-muted">
        Universal game controller framework
	</p>
	<p class="text-muted">      
	TAMUHack 2016 Top 10 Project 
        </p>
      </a>
    </div>
  </div>

	
<div class="row text-center">
  <div class="col-md-4 col-md-offset-0 col-sm-4 col-sm-offset-0 col-xs-12 col-xs-offset-0 text-center">
    <div class="project-card">
      <a target="_blank" href="https://github.com/tommy1019/murmur" class="project-link">
        <span class="fa-stack fa-3x">
          <i class="fa fa-circle fa-stack-2x stack-color"></i>
          <i class="fa fa-commenting fa-stack-1x fa-inverse"></i>
        </span>
        <h4>Murmur</h4>
        <hr class="seperator">
        <p class="text-muted">
        End-to-end encrypted chat client
	</p>
	<p class="text-muted">
	HackUTD 2016 "Best Developer Tool" winner
        </p>
      </a>
    </div>
  </div>

	
<div class="row text-center">
  <div class="col-md-4 col-md-offset-0 col-sm-4 col-sm-offset-0 col-xs-12 col-xs-offset-0 text-center">
    <div class="project-card">
      <a target="_blank" href="https://github.com/gcmvy3/GeoDrop" class="project-link">
        <span class="fa-stack fa-3x">
          <i class="fa fa-circle fa-stack-2x stack-color"></i>
          <i class="fa fa-map-marker fa-stack-1x fa-inverse"></i>
        </span>
        <h4>Geodrop</h4>
        <hr class="seperator">
        <p class="text-muted">
        Location-based anonymous messaging app
        </p>
	<p class="text-muted">
	HackDFW Participant
        </p>
      </a>
    </div>
  </div>
</div>

	<div class="posts-list">
  {% for post in paginator.posts %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	  <h2 class="post-title">{{ post.title }}</h2>

	  {% if post.subtitle %}
	  <h3 class="post-subtitle">
	    {{ post.subtitle }}
	  </h3>
	  {% endif %}
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: "%B %-d, %Y" }}
    </p>

    <div class="post-entry-container">
      {% if post.image %}
      <div class="post-image">
        <a href="{{ post.url | prepend: site.baseurl }}">
          <img src="{{ post.image }}">
        </a>
      </div>
      {% endif %}
      <div class="post-entry">
        {{ post.excerpt | strip_html | xml_escape | truncatewords: site.excerpt_length }}
        {% assign excerpt_word_count = post.excerpt | number_of_words %}
        {% if post.content != post.excerpt or excerpt_word_count > site.excerpt_length %}
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
        {% endif %}
      </div>
    </div>

    {% if post.tags.size > 0 %}
    <div class="blog-tags">
      Tags:
      {% if site.link-tags %}
      {% for tag in post.tags %}
      <a href="{{ site.baseurl }}/tag/{{ tag }}">{{ tag }}</a>
      {% endfor %}
      {% else %}
        {{ post.tags | join: ", " }}
      {% endif %}
    </div>
    {% endif %}

   </article>
  {% endfor %}
</div>
	

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}



<div class="spacer"></div>
