---
layout: page
title: All in Automation
tagline: Supporting tagline
---
{% include JB/setup %}


<div class="row">
  <div class="span12">
    <div class="row">
      <div class="span9">

        {% for post in site.posts limit:5 %}
        <div class="row">
          <div class="span2">
            <h5 class="post-date" align="right">
              {{ post.date | date: "%e%B %Y" }}</h5>
          </div>
          <div class="span7">
            <h2><a class="post-title" href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
            {{ post.content }}
            <a href="{{ BASE_PATH }}{{ post.url }}/#share-comment">Share Comment</a>
            <hr>
            <br />
            <br />
          </div>
        </div>
        {% endfor %}

      </div>
      <div class="span3">
        {% include JB/sidebar %}
      </div>
    </div>
  </div>
</div>

<div class="row">
  <div class="span7 offset2">
    <h3><a href="{{ BASE_PATH }}{{ site.JB.archive_path }}">More posts</a></h3>
  </div>
</div>