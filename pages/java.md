---
layout: page
title: Java 基础 
titlebar: java
subtitle: jdk8 &nbsp;&nbsp; 集合 &nbsp;&nbsp; 泛型 &nbsp;&nbsp; 反射  &nbsp;&nbsp; IO/NIO &nbsp;&nbsp; 网络编程 &nbsp;&nbsp; 异常  &nbsp;&nbsp; 调试
menu: java
css: ['blog-page.css']
permalink: /java
---

<div class="row">

    <div class="col-md-12">

        <ul id="posts-list">
            {% for post in site.posts %}
                {% if post.category=='java' or post.keywords contains 'java' %}
                <li class="posts-list-item">
                    <div class="posts-content">
                        <span class="posts-list-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
                        <a class="posts-list-name bubble-float-left" href="{{ post.url }}">{{ post.title }}</a>
                        <span class='circle'></span>
                    </div>
                </li>
                {% endif %}
            {% endfor %}
        </ul> 

        <!-- Pagination -->
        {% include pagination.html %}

        <!-- Comments -->
       <div class="comment">
         {% include comments.html %}
       </div>
    </div>

</div>
<script>
    $(document).ready(function(){

        // Enable bootstrap tooltip
        $("body").tooltip({ selector: '[data-toggle=tooltip]' });

    });
</script>