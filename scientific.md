---
layout: post
title: Scientific commentary
---

<ul class="post-list">
{% for post in site.posts %}
    {% if post.category == "SC" %}
        <li>
            <a href="{{ post.url | absolute_url }}" class="post-link">
                <div class="post-link__heading">
                    <h1 class="post-link__title">      
                        {{ post.title }}
                    </h1>
                </div>
                <span class="post-date">
                {{ post.date | date: "%b %-d, '%y" }}
                </span>
            </a>
            <a href="{{ post.url | absolute_url }}" class="post-link2">
                <div class="post-link__heading">
                {% unless post.author == "" %}
                    <h2 class="post-link__title">      
                        {{ post.author }}
                    </h2>
                {% else %}
                {% endunless %}
                </div>
            </a>
        </li>
    {% endif %}
{% endfor %}
</ul>