---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

<p><font size="4.9"> <strong> Journal </strong> </font></p>

{% include base_path %}
{% capture written_type %}'None'{% endcapture %}
{% for post in site.publications reversed %}
  {% capture type %}{{ post.type | type: '%Y'}}{% endcapture %}
  {% if type == 'journal' %}
    {% capture written_type %}{{ type }}{% endcapture %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
<p><font size="4.9"> <strong> Conference </strong> </font><p>
{% capture written_type %}'None'{% endcapture %}
{% for post in site.publications reversed %}
  {% capture type %}{{ post.type | type: '%Y'}}{% endcapture %}
  {% if type == 'conference' %}
    {% capture written_type %}{{ type }}{% endcapture %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
