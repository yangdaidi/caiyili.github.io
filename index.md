---
layout: page
title: 空心菜
tagline: --起点
---
{% include JB/setup %}


<ul class="posts">
  {% for post in site.posts %}
    <li>
    	<h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
    	<div>
    		{{post.content | split:'<!-- more -->' |first }}
    	</div>
    	<hr />
    </li>
  {% endfor %}
</ul>

## To-Do

This theme is still unfinished. If you'd like to be added as a contributor, [please fork](http://github.com/plusjade/jekyll-bootstrap)!
We need to clean up the themes, make theme usage guides with theme-specific markup examples.


