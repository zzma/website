---
layout: page
permalink: /
---



<h4></h4>
<b>  I am recruiting new Ph.D. students! I have a few funded positions available. Please [drop me an email](mailto:zane.ma@oregonstate.edu) with your CV if you're interested in working with me. </b>
<hr>
I'm Zane, and I study <span class="underline"><b>network security and privacy</b></span>. My [research](/research/) seeks to understand and build systems for <b>authentication and trust</b> on the internet. Recent areas of focus include DNS, HTTPS/TLS server authentication, client authentication, and data authenticity. I also analyze the security threats related to emerging network technologies: 5G networks, IoT botnets, cryptocurrency/blockchain abuse, etc.


#### Select publications 

{% assign selected = site.data.research.pubs | where: "selected", true %}
{% for pub in selected %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.conference}}* *{{pub.year}}*
<br>
{% if pub.media %}&nbsp;{% for article in pub.media %}[[{{article.name}}]({{article.url}}){:target="_blank" .sublinks}]{% endfor %}<br>{% endif %}
{% if pub.note %} {{pub.note}}
{% endif %}
{% endfor %}



