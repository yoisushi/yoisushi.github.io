---
layout: default
title: Tags
---

<div class="post">

{% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign tag_words = site_tags | split:',' | sort %}

<!-- <h3 style="margin-left: -5px;">All Tags</h3> -->
<h2>All Tags</h2>

<p>
<ul>
{% for item in (0..site.tags.size) %}{% unless forloop.last %}
{% capture this_word %}{{ tag_words[item] | strip_newlines }}{% endcapture %}
<li>
<a href="#{{ this_word | replace:' ','-' }}-ref" data-toggle="tab">
{{ this_word }} ({{ site.tags[this_word].size }})
</a>
</li>
{% endunless %}{% endfor %}
</ul>
</p>

<!-- Tab panes -->
{% assign last_item = site.tags.size | minus: 1 %}
{% for item in (0..site.tags.size) %}{% unless forloop.last %}
{% capture this_word %}{{ tag_words[item] | strip_newlines }}{% endcapture %}
<div id="{{ this_word | replace:' ','-' }}-ref">
<h3><i class="fa fa-tag" style="margin-right: 3px; margin-left: -5px;" aria-hidden="true"></i>{{ this_word }}</h3>

<p>

{% for post in site.tags[this_word] %}{% if post.title != null %}

<ul>
<li style="line-height: 30px;"><a href="{{ site.BASE_PATH }}{{post.url}}">{{post.title}}</a> - {{ post.date | date: "%d %B, %Y" }}</li>
{% endif %}{% endfor %}
{% unless item == last_item %}
{% endunless %}
</ul>

</p>

</div>
{% endunless %}{% endfor %}


</div>
