---
layout: page
permalink: /

pubs:     
    - title:   "Stale TLS Certificates: Investigating Precarious Third-Party Access to Valid TLS Keys"
      author:  '<span style="text-decoration: underline">Zane Ma</span>, Aaron Faulkenberry, Thomas Papastergiou, Zakir Durumeric, Michael D. Bailey, Angelos D. Keromytis, Fabian Monrose, Manos Antonakakis'
      conference: "ACM Internet Measurement Conference (IMC)"
      url:     "/papers/imc23_stale_certs.pdf"
      year:    "2023"
      media:
        - name: "bib"
          url:  "/papers/imc23_stale_certs.bib"

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

###  I am actively recruiting new graduate students! I have a few funded positions available. Please [drop me an email](mailto:zane.ma@oregonstate.edu) with your CV if you're interested in working with me. 



{% include image.html url="images/zane-headshot.jpg" caption="" width="224px" align="left" %}

I'm Zane, and I am an Assistant Professor teaching computer science at Oregon State University. My [research](/research/) takes a data-driven approach to authentication and trust on today's internet. I strive to understand + build systems that allow computers and users to *reliably and securely authenticate information*. Applications of particular interest include HTTPS/TLS server authentication, client authentication, and data authenticity. My secondary research interest analyzes the security of novel internet technologies: 5G networks, IoT botnets, cryptocurrency miners/abuse, etc.

I previously worked with wonderful folks at [Georgia Tech](https://astrolavos.gatech.edu/){:target="_blank"}, and I received my Ph.D. at the University of Illinois at Urbana-Champaign, advised by [Michael Bailey](https://faculty.cc.gatech.edu/~mbailey/){:target="_blank"}. My [dissertation](/papers/zane-dissertation.pdf) identified the trust relationships of the web PKI. 

## Contact

3079 Kelley Engineering Center <br />
Corvallis, OR 97331 <br />
Email: [zane.ma@oregonstate.edu]

[zane.ma@oregonstate.edu]: mailto:zane.ma@oregonstate.edu


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



