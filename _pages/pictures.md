---
title: "Pictures"
layout: piclay
excerpt: "Pictures"
permalink: /pictures/
---

# Pictures

#### Gallery
(Click to see a larger image)

{% assign number_printed = 0 %}
{% for pic in site.data.gallery %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix">


{% assign cacheArr = pic.image | split:"." %}
{% assign fileExt = "."| append: cacheArr[-1]%}
{% assign fileName = pic.image | replace: fileExt,"" %}
{% capture img %}/images/picpic/Gallery/{{ fileName}}{{fileExt}}{% endcapture %}
{% capture scaledImg %}/images/picpic/Gallery/{{ fileName}}_scaled{{fileExt}}{% endcapture %}
{% assign haveScaledImg = true %}


{% if haveScaledImg %}

<a href="{{img}}" target="_blank">
    <img src="{{ scaledImg }}" class="img-responsive" width="95%" style="float: left" />
</a>
{%else%}
<a href="{{img}}" target="_blank">
    <img src="{{ img }}" class="img-responsive" width="95%" style="float: left" />
</a>
{% endif %}
</div>


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

<p> &nbsp; </p>
