---
layout: page
permalink: /research/
title: Research
pubs:
    - title:   "Outguard: Detecting In-Browser Covert Cryptocurrency Mining in the Wild"
      author:  "Amin Kharraz, **Zane Ma**, Paul Murley, Charles Lever, Joshua Mason, Andrew Miller, Manos Antonakakis, Michael Bailey"
      conference: "The Web Conference (WWW)"
      year:    "2019"
      url:     "/papers/www19_cryptojacking.pdf"
      media:
        - name: "bib"
          url:  "/papers/www19_cryptojacking.bib"
      note: "Best paper award"

    - title:   "Measuring Ethereum's Peer-to-Peer Network"
      author:  "Seoung Kim, **Zane Ma**, Siddharth Murali, Joshua Mason, Andrew Miller, Michael Bailey"
      conference: "Internet Measurement Conference (IMC)"
      year:    "2018"
      url:     "/papers/imc18_ethpeers.pdf"
      media:
        - name: "bib"
          url:  "/papers/imc18_ethpeers.bib"

    - title:   "Understanding the Mirai Botnet"
      author:  "Manos Antonakakis, Tim April, Michael Bailey, Matt Bernhard, Elie Bursztein, Jaime Cochran, Zakir Durumeric, J. Alex Halderman, Luca Invernizzi, Michalis Kallitsis, Deepak Kumar, Chaz Lever, <b> Zane Ma* </b>, Joshua Mason, Damian Menscher, Chad Seaman, Nick Sullivan, Kurt Thomas, Yi Zhou"
      conference: "USENIX Security"
      year:    "2017"
      url:     "/papers/usenix17_mirai.pdf"
      media:
        - name: "bib"
          url:  "/papers/usenix17_mirai.bib"
        - name: "slides"
          url:  "/slides/mirai.pdf"
        - name: "talk"
          url:  "https://www.youtube.com/watch?v=1pywzRTJDaY"

    - title:   "The Security Impact of HTTPS Interception"
      author:  "Zakir Durumeric, **Zane Ma**, Drew Springall, Richard Barnes, Nick Sullivan, Elie Bursztein, Michael Bailey, J. Alex Halderman, Vern Paxson"
      conference: "Network and Distributed System Security Symposium (NDSS)"
      year:    "2017"
      url:     "/papers/ndss17_interception.pdf"
      media:
        - name: "bib"
          url:  "/papers/ndss17_interception.bib"

    - title:   "Security Challenges in an Increasingly Tangled Web"
      author:  "Deepak Kumar, **Zane Ma**, Zakir Durumeric, Ariana Mirian, Joshua Mason, Michael Bailey, J. Alex Halderman"
      conference: "World Wide Web (WWW)"
      year:    "2017"
      url:     "/papers/www17_tangled.pdf"
      media:
        - name: "bib"
          url:  "/papers/www17_tangled.bib"

    - title:   "An Internet-wide View of ICS devices"
      author:  "Ariana Mirian, **Zane Ma**, David Adrian, Matthew Tischer, Thasphon Chuenchujit, Tim Yardley, Robin Berthier, Josh Mason, Zakir Durumeric, J. Alex Halderman, Michael Bailey"
      conference: "Privacy, Security and Trust (PST)"
      year:    "2016"
      url:     "/papers/pst16_ics.pdf"
      media:
        - name: "bib"
          url:  "/papers/pst16_ics.bib"
        - name: "slides"
          url:  "/slides/pst16_ics_slides.pdf"

talks:
    - title: "Mirai and the Future of IoT Botnets"
      url: ""
      conference: "Messaging, Malware and Mobile Anti-Abuse Working Group (M3AAWG): 42nd General Meeting"
      location: "San Francisco, CA"
      date: "2018-02-20"
      media: 
        - name: "slides"
          url:  "/slides/m3aawg_mirai.pdf"

    - title: "Understanding the Mirai Botnet"
      date: "2017-11-08"
      conference: "Security Seminar"
      location: "University of Chicago, IL"
      media:
        - name: "slides"
          url:  "/slides/uchicago_mirai.pdf"
    
---

### Publications

[Google Scholar](https://scholar.google.com/citations?user=Qoy6za0AAAAJ&hl=en){:target="_blank"}

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
*{{pub.conference}}* *{{pub.year}}*
{% if pub.media %}&nbsp;{% for article in pub.media %}[[{{article.name}}]({{article.url}}){:target="_blank"}]{% endfor %}{% endif %}<br />
{{pub.author}}<br />
{% if pub.note %} __{{pub.note}}__
{% endif %}
{% endfor %}

<i>* denotes primary/first author</i>


### Invited Talks

{% for talk in page.talks %}
**{{talk.date}}**&nbsp;&nbsp;&nbsp;"{{talk.title}}." *{{talk.conference}}*. {{talk.location}}.
{% if talk.media %}&nbsp;{% for article in talk.media %}[[{{article.name}}]({{article.url}}){:target="_blank"}]{% endfor %}{% endif %}
{% endfor %}
