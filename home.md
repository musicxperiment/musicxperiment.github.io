---
layout: default
title: Home
---
<!-- <ol class="blog-list posts">
	{% for post in paginator.posts %}
		<li class="post {% cycle 'post-2-column', 'post-1-column is-in-last-column', 'post-1-column', 'post-1-column', 'post-1-column is-in-last-column', 'post-1-column', 'post-1-column', 'post-1-column is-in-last-column' %}">
		
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
</ol> -->

<section class="hero">
	<h1>Hello, my name is Rudy. I am a Designer / Front End Developer living in Indonesia. </h1>
</section>

<h1 class="page-title">Blog</h1>
<ol class="blog-list posts">
  {% for post in site.blog reversed limit:2 %}
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

<h1 class="page-title">Project</h1>
<ol class="blog-list posts">
  {% for post in site.project reversed limit:2 %}
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
