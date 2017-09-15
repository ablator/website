---
layout: page
title: Docs
permalink: /docs/
---

<img class="img-fluid" src="../img/ablator_logo.png" width="400px" style="float: right;" class="ml-4"
         alt="The ablator logo, a space capsule screaming through the atmosphere"/>

Welcome to the ablator docs, which contain information about how ablator works in depth, tips on how
to access ablator from various app types, and tutorials on how to achieve certain goals using
ablator.

These pages are hosted on [github](https://github.com/ablator/website/). If you have improvements,
corrections, or even new additions, we'd be very happy to accept your pull request.

<h2>{{ site.data.docs_list.docs_list_title }}</h2>
<ul>
   {% for item in site.data.docs_list.docs %}
      <li><a href="{{ item.url }}" alt="{{ item.title }}">{{ item.title }}</a></li>
   {% endfor %}
</ul>