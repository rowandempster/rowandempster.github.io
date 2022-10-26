---
permalink: /about
title: "About Me"
toc: true
# toc_sticky: true
toc_label: "About Me"
layout: single
classes: wide
---

## Summary

- In June 2020 I graduated from UWaterloo's CS Co-op program, with an academic and extracurricular focus on robotics and automation. 
- I am graduating from my MASc from UWaterloo in Fall 2022, under the supervision of Derek Rayside.
- My research is focussed on motion planning software with an application to automated driving. Research topics include mapping & environment modeling, action classification from video steams, and trajectory planning & control. See my [Google Scholar profile](https://scholar.google.com/citations?user=hKf7WaAAAAAJ) for details.

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

## Publications

{% for pub in site.data.publications %}
<!-- <a href="{{ pub.url }}" rel="pub access" style="width:50px;height:60px;">![pub-image]({{ pub.image }}){: .align-right} -->
<!-- <figure style="width: 200px" class="align-right">
  <!-- <img src="{{ pub.image }}" alt=""> -->
  <!-- <a href="{{ pub.image }}"><img src="{{ pub.image }}"></a> -->
<!-- </figure>  --> 
### [{{ pub.name }}]({{ pub.url }})

- Status: {{ pub.status }}
- Co-authors: {{ pub.co }}

{% endfor %}

## Industry Experience

{% for employer in site.data.employers %}
<a href="{{ employer.url }}" rel="employer website">![employer-image]({{ employer.image }}){: .align-right}
### {{ employer.name }}

{{ employer.position }} - {{ employer.dates }}

{{ employer.description }}
{% endfor %}


## Supervisory Experience

### Teaching Assistantships

In Winter 2021 I was the TA for ECE406 (Algorithm Design and Analysis). I was responsible for tutoring and marking the assignments of 150 ECE undergrad students.

### UWaterloo Co-op Management

Since September 2019, I have consistently hired and managed co-op students on behalf of WATonomous, achieving an employer rating of 8.3 / 10. To date, we have supported 14 full-time co-ops, who have worked on projects ranging from guided soft target fabrication to action classification in video streams. 

**Summer 2022 Cohort**

*Alexander and Eddy*: Action Classification

*Bao*: Mapping and Localization

*Julian*: Guided Soft Target Fabrication

**Winter 2021 Cohort**

*Andrew*: Mapping and Localization

*Tae*: Simulation Map Creation

**Winter 2020 Cohort**

*Frank*: Power Systems and Radar Driver

**Spring 2019 Cohort**

*Tony*: Path Planning

*Wen*: Sensor Calibration

*Mitchell*: Power Systems

**Fall 2019 Cohort**

*Rowan*: Project Management

*Chad*: Sensor Mounting

*Vinayak*: Dynamic Reconfigure