---
layout: default
title: Home
---
<section class="hero">
	<h1>Hello, my name is Rudy. I am a Designer / Front End Developer living in Indonesia. </h1>
</section>

<h3 class="page-title"><a href="/blog/">Latest Blog</a></h3>
<ol class="blog-list posts">
	{% assign blogfiltered = site.blog | reverse | top:2 %}
	{% for post in blogfiltered limit:2 %}
	    <!-- <li class="post post-{{ post.column }}-column"> -->
	    <li class="post {% cycle 'post-2-column', 'post-1-column is-in-last-column'  %}">
	    
	      <div class="post">
	        <h1 class="post-title">
	          <a href="{{ site.url }}{{ post.url }}">
	            {{ post.title }}
	          </a>
	        </h1>

	        <span class="post-date">
	        	{{ post.date | date_to_string }}
	        	{% if post.author %}
		        	by {{ post.author.name }}
		        {% endif %}
	        </span>

			{% if post.description.size > 140 %}{{ post.description | markdownify | remove: '<p>' | remove: '</p>' }}{% else %}{{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}{% endif %} <a href="{{ site.url }}{{ post.url }}" title="Read more"><strong>Read more...</strong></a>
	      </div>
	    </li>

	{% endfor %}
</ol>

<h3 class="page-title"><a href="/project/">Latest Project</a></h3>
<ol class="blog-list posts">
	{% assign projectfiltered = site.project | reverse | top:2 %}
	{% for post in projectfiltered limit:2 %}
	    <!-- <li class="post post-{{ post.column }}-column"> -->
	    <li class="post {% cycle 'post-2-column', 'post-1-column is-in-last-column'  %}">
	    
	      <div class="post">
	        <h1 class="post-title">
	          <a href="{{ site.url }}{{ post.url }}">
	            {{ post.title }}
	          </a>
	        </h1>

	        <span class="post-date">{{ post.date | date_to_string }}</span>

	         {% if post.description.size > 140 %}{{ post.description | markdownify | remove: '<p>' | remove: '</p>' }}{% else %}{{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}{% endif %} <a href="{{ site.url }}{{ post.url }}" title="Read more"><strong>Read more...</strong></a>
	      </div>
	    </li>
	{% endfor %}
</ol>
