---
title: "Home"
layout: homelay
excerpt: "MASS Lab official website"
sitemap: false
permalink: /
---

<h1> Welcome to the Mass Lab </h1>

<!--todo: Please edit contents-->

**MA**ssachusetts' **S**oftware **S**ystem Research Lab

<div markdown="0"  class="bs-example" data-example-id="simple-carousel">
    <div id="carousel-example-generic" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators">
            {% for article in site.data.news %}
            {% if article.showonhomepage == 1 %}
                <li data-target="#carousel-example-generic" data-slide-to="{{forloop.index|minus:1}}" {% if forloop.index == 1 %}class="active" {%else%}class="" {%endif%}></li>
            {% endif %}
            {% endfor %}
        </ol>
    <div class="carousel-inner" role="listbox">
    
    {% for article in site.data.news %}
    {% if article.showonhomepage == 1 %}
        <div {% if forloop.index == 1 %}class="item active" {%else%}class="item" {%endif%}>
            <img style="width:100%;height:300px;" src="{{ site.url }}{{ site.baseurl }}/images/newspic/{{article.picture}}" data-holder-rendered="true">
            <div class="carousel-caption">
                <h3 class="bg-newsheading">{{article.headline}}</h3>
            </div>
        </div>
    {% endif %}
    {% endfor %}
    
    </div>
      <a class="left carousel-control" href="#carousel-example-generic" role="button" data-slide="prev">
        <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
        <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
</div>




Group description here (PLEASE CHANGE)





Note: The followings are logo zone

<figure class="fourth">
  <img src="{{ site.url }}{{ site.baseurl }}/images/logopic/Logo_UMASS.png" style="width: 100px">
</figure>
