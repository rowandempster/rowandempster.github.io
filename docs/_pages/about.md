---
permalink: /about
title: "About Me"
toc: true
toc_sticky: true
toc_label: "About Me"
---

Hi, I'm Rowan. I am graduated from UWaterloo's CS Co-op program in June 2020 with an academic and extracurricular focus on robotics and automation. Now I'm back in school working on a MASc in ECE under the supervision of Derek Rayside. I'm research environment modeling and motion planning for AVs, using WATonomous as a platform, and having a great time!

Some things I enjoy are:
- Autonomous Vehicles and Robotics in general
- Building human systems that work efficiently
- Architecting software systems

Please look through this page to get an idea of what I've done, and where I'm heading!

## Education

{% for edu in site.data.education %}
<a href="{{ edu.url }}" rel="edu website">![edu-image]({{ edu.image }}){: .align-right}
### {{ edu.degree }}

{{ edu.name }} - {{ edu.dates }}

{% for highlight in edu.highlights %}
- {{ highlight }}
{% endfor %}

<details><summary>Selected Courses</summary>
<br>
{% for course in edu.courses %}
- {{ course }} <br>
{% endfor %}
</details>

{{ edu.description }}
{% endfor %}

## Industry Experience

{% for employer in site.data.employers %}
<a href="{{ employer.url }}" rel="employer website">![employer-image]({{ employer.image }}){: .align-right}
### {{ employer.name }}

{{ employer.position }} - {{ employer.dates }}

{{ employer.description }}
{% endfor %}
