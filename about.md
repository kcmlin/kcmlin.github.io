---
layout: page
permalink: /about/index.html
title: About
tags: 
imagefeature: 
chart: true
---

Katherine is an avid runner, a seasonal cyclist, a traveler and a self-proclaimed photography enthusiast. She has completed 6 half marathons and 3 marathons. Katherine is currently training for her first ultramarathon. Her ultimate goals are to travel around the world, embrace every moment in life and never stop exploring.

#### Places I have run at
    
| Africa | N/S America | Antarctica | Asia | Europe | Oceania |  
|:--:|:---:|:--:|:---:|:--:|:---:|
| Ethiopia | USA | | Taiwan | | | 
| | | | China |  | |

#### Past Running Events at a Glance: 

* **Ultra Marathons**:

| No.  | Race | Distance | Year | Month | City | State | Country | Chip Time | Type  | Note |
|:----:|:---- |:----:|:----:|:----: |:---- |:----  | :----   | :----:    |:----:|:----:|
| 1    |      |      |       |      |       |         |           |      |      |      |

* **Full Marathons**:

| No.  | Race | Year | Month | City | State | Country | Chip Time | Type  | Note |
|:----:|:---- |:----:|:----: |:---- |:----  | :----   | :----:    |:----:|:------:| 
| 1    | Baltimore Running Festival | 2015 | 10 | Baltimore | MD | USA | 6:51:27 | Road |  |
| 2    | Anthem Richmond Marathon | 2015 | 11 | Richmond | VA  | USA | 5:53:36  | Road | VA Capital |
| 3    | Salmon Marathon | 2016 | 09 | Salmon  | ID | USA | 6:13:54 | Mixed | 1st Race at Altitude  |

* **Mid Distances**:

| No.  | Race | Distance | Year | Month | City | State | Country | Chip Time | Type | Note|
|:----:|:---- |:----:|:----:|:----: |:---- |:----  | :----   | :----:    |:----:|:----:|
| 1    | PHUNT | 25K | 2016 |  01 | Elkton | MD  | USA | 3:59:59 (Watch) | Trail | D+ 2,207 ft |
| 2    | Gunpowder Keg Ultra | 25K | 2016 | 04 | Hereford | MD | USA | 3:53:28 (Watch) | Trail | D+ 1,733 ft |

* **Half Marathons**:

| No.  | Race | Year | Month | City | State | Country | Chip Time | Type | Note | 
|:----:|:---- |:----:|:----: |:---- |:----  | :----   | :----:    |:----:|:----:|
| 1    | Baltimore Running Festival     | 2009 | 10 | Baltimore  | MD | USA | 3:11:42 | Road |  | 
| 2    | Rock 'n' Roll USA Marathon     | 2014 | 03 | Washington | DC | USA | 3:07:56 | Road | US Capital |
| 3    | Rock 'n' Roll Raleigh Marathon | 2014 | 04 | Raleigh    | NC | USA | 2:57:22 | Road | NC Capital |
| 4    | Pittsburgh Marathon            | 2014 | 05 | Pittsburgh | PA | USA | 2:49:04 | Road | |
| 5    | TCS Annapolis Running Classic  | 2014 | 11 | Annapolis  | MD | USA | 2:35:57 | Road | MD Capital |
| 6    | Frederick Running Festival     | 2015 | 05 | Frederick  | MD | USA | 2:28:45 | Road |  |

* **Other Short Distances**:

| No.  | Race                    | Distance | Year | City | State | Country | Note | 
|:----:|:----                       |:----: |:----: |:---- |:----  | :----   | :----    |
| 1    | Baltimore Running Festival | 5K    | 2010 | Baltimore  | MD | USA | |
| 2    | Baltimore Running Festival | 5K    | 2012 | Baltimore  | MD | USA | With P |
| 3    | Baltimore Running Festival | 5K    | 2013 | Baltimore  | MD | USA | First trained race. C25K |
| 4    | Philadelphia Marathon      | 8K    | 2013 | Philadelphia  | PA | USA | First out of state race |
| 5    | Baltimore 10-Miler         | 10M   | 2015 | Baltimore  | MD | USA | King Crab Challenge |
| 6    | Color Vibe 5K              | 5K    | 2016 | Hanover    | MD | USA | First color run. With 2 nephews (5yo, 8yo) | 
| 7    | UN Women's first 5K        | 5K    | 2017 | Addis Ababa | | Ethiopia | First overseas race | 


---

{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}
{% assign statuscount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign readtime = post_words | append: '.0' | divided_by:200 %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}


#### Project Ultra: Current Stats

* **<span style="color:orange">Number of Posts</span>**: {{ site.posts | size }} posts {% if featuredcount != 0 %} (including <a href="{{ site.url }}/featured">{{ featuredcount }} featured posts</a>){% endif %}
* **<span style="color:orange">Number of Categories</span>**: {{ site.categories | size }} categories
* **<span style="color:orange">Number of Words</span>**: {{ total_words }} words
* **<span style="color:orange">Average Time to Read All Posts</span>**: approximately <span class="time">{{ total_readtime }}</span> minutes

#### Project Ultra: Most Recent Post

* **<span style="color:orange">Title</span>**: {% for post in site.posts limit:1 %}{% if post.description %}<a href="{{ site.url }}{{ post.url }}" title="{{ post.description }}">"{{ post.title }}"</a>{% else %}<a href="{{ site.url }}{{ post.url }}" title="{{ post.description }}" title="Read more about {{ post.title }}">"{{ post.title }}"</a>{% endif %}{% endfor %} 
* **<span style="color:orange">Published Date</span>**: {% for post in site.posts limit:1 %}{% assign modifiedtime = post.modified | date: "%Y%m%d" %}{% assign posttime = post.date | date: "%Y%m%d" %}<time datetime="{{ post.date | date_to_xmlschema }}" class="post-time">{{ post.date | date: "%d %b %Y" }}</time>{% if post.modified %}{% if modifiedtime != posttime %} and last modified on <time datetime="{{ post.modified | date: "%Y-%m-%d" }}" itemprop="dateModified">{{ post.modified | date: "%d %b %Y" }}</time>{% endif %}{% endif %}{% endfor %}.

#### Project Ultra: Most Recent Commit

* **<span style="color:orange">Most Recent Site Update</span>**: {{ site.time | date: "%A, %d %b %Y" }} at {{ site.time | date: "%I:%M %p" }} [UTC](http://en.wikipedia.org/wiki/Coordinated_Universal_Time "Temps Universel Coordonné").
