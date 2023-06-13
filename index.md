---
layout: page
permalink: /

pubs:     
    - title:   "Tracing Your Roots: Exploring the TLS Trust Anchor Ecosystem"
      author:  '<span style="text-decoration: underline">Zane Ma</span>, James Austgen, Joshua Mason, Zakir Durumeric, Michael Bailey'
      conference: "ACM Internet Measurement Conference (IMC)"
      url:     "/papers/imc21_roots.pdf"
      year:    "2021"
      media:
        - name: "bib"
          url:  "/papers/imc21_roots.bib"
        - name: "slides"
          url: "/slides/imc21_roots.pdf"
        - name: "talk"
          url: "/videos/imc21-roots.mp4"

    - title:   "What's in a Name? Exploring CA Certificate Control"
      author:  '<span style="text-decoration: underline">Zane Ma</span>, Joshua Mason, Manos Antonakakis, Zakir Durumeric, Michael Bailey'
      conference: "USENIX Security"
      year:    "2021"
      url:     "/papers/usenix21_ca_operators.pdf"
      media:
        - name: "bib"
          url:  "/papers/usenix21_ca_operators.bib"
        - name: "slides"
          url: "/slides/sec21_ca_operators.pdf"
        - name: "talk"
          url: "https://www.youtube.com/watch?v=Aq1o8prmoyE"

    - title:   "Measuring Identity Confusion with Uniform Resource Locators"
      author:  'Joshua Reynolds, Deepak Kumar, <span style="text-decoration: underline">Zane Ma</span>, Rohan Subramanian, Meishan Wu, Martin Shelton, Joshua Mason, Emily Stark, Michael Bailey'
      conference: "ACM Conference on Human Factors in Computing Systems (CHI)"
      year:    "2020"
      url:     "/papers/chi20_urlconfusion.pdf"
      media:
        - name: "bib"
          url:  "/papers/chi20_urlconfusion.bib"

    - title:   "The Impact of Secure Transport Protocols on Phishing Efficacy"
      author:  '<span style="text-decoration: underline">Zane Ma</span>, Joshua Reynolds, Joseph Dickinson, Kaishen Wang, Taylor Judd, Joseph D. Barnes, Joshua Mason, Michael Bailey'
      conference: "USENIX Workshop on Cyber Security Experimentation and Test (CSET)"
      year:    "2019"
      url:     "/papers/cset19_httpsphishing.pdf"
      media:
        - name: "bib"
          url:  "/papers/cset19_httpsphishing.bib"
        - name: "slides"
          url:  "/slides/cset-https-phishing-2019.pdf"

    - title:   "The Security Impact of HTTPS Interception"
      author:  'Zakir Durumeric, <span style="text-decoration: underline">Zane Ma</span>, Drew Springall, Richard Barnes, Nick Sullivan, Elie Bursztein, Michael Bailey, J. Alex Halderman, Vern Paxson'
      conference: "Network and Distributed System Security Symposium (NDSS)"
      year:    "2017"
      url:     "/papers/ndss17_interception.pdf"
      media:
        - name: "bib"
          url:  "/papers/ndss17_interception.bib"

    - title:   "Understanding the Mirai Botnet"
      author:  '<span style="text-decoration: underline">Zane Ma</span>, Manos Antonakakis, Tim April, Michael Bailey, Matt Bernhard, Elie Bursztein, Jaime Cochran, Zakir Durumeric, J. Alex Halderman, Luca Invernizzi, Michalis Kallitsis, Deepak Kumar, Chaz Lever, Joshua Mason, Damian Menscher, Chad Seaman, Nick Sullivan, Kurt Thomas, Yi Zhou'
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
---

{% include image.html url="images/zane-headshot.jpg" caption="" width="250px" align="right" %}

#### Beginning in September 2023, I will be joining Oregon State University's EECS department as an Assistant Professor. Please reach out if you are interested in working together!
<br />
I'm Zane, and I [research](/research/) computer and network security. I take a data-driven, systems approach to authentication and trust on today's internet. I strive to understand + build systems that allow computers and users to *reliably and securely authenticate information*. Applications of particular interest include HTTPS/TLS server authentication, client authentication, and data authenticity. My secondary research interest characterizes the security of new, rapidly evolving internet technologies: IoT botnets, cryptocurrency miners/abuse, ICS devices, and realtime web protocols.

I'm currently a research scientist at the Georgia Institute of Technology. I work with some great folks in the [Astrolavos Lab](https://astrolavos.gatech.edu/){:target="_blank"} and 
[Center for Cyber Operations Enquiry and Unconventional Sensing (COEUS)](https://coeus.center/){:target="_blank"}. 

I received my Ph.D. in Computer Science at the University of Illinois at Urbana-Champaign, advised by [Michael Bailey](http://mdbailey.ece.illinois.edu/){:target="_blank"}. My [dissertation](/papers/zane-dissertation.pdf) identified the trust relationships of the web PKI. 


## Contact

Klaus Advanced Computing Building <br />
266 Ferst Drive<br />
Atlanta, GA 30313 <br />
Email: [zanema@gatech.edu]

[zanema@gatech.edu]: mailto:zanema@gatech.edu


## Select publications 

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
*{{pub.conference}}* *{{pub.year}}*
{% if pub.media %}&nbsp;{% for article in pub.media %}[[{{article.name}}]({{article.url}}){:target="_blank"}]{% endfor %}{% endif %}<br />
{{pub.author}}<br />
{% if pub.note %} {{pub.note}}
{% endif %}
{% endfor %}



