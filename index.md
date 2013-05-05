---
layout: page
title: 空心菜
tagline: --起点
---
{% include JB/setup %}

<div>
  {% for post in site.posts %}
    <div>
    	<h3><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
    	<div>
    		{{post.content | split:'<!-- more -->' |first }}
    	</div>
    	<div>
    		<a href="{{ BASE_PATH }}{{ post.url }}">阅读全文...</a>
    	</div>
    	<div>
          <cite>{{ post.date | date: "%Y-%m-%d" }}</cite> 
          <i class="icon-tag"></i>  
          {% for tag in post.tags %}
          	<a href="{{ BASE_PATH }}{{ site.JB.tags_path }}#{{ tag }}-ref">{{ tag }}</a>
          	{% if forloop.last %}{% else %}, {% endif %}
          {% endfor %}
       </div> 
    	<hr />
    </div>
  {% endfor %}
</div>



