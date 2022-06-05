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


## Supervisory Experience

Since September 2019, I have consistently hired and supervised co-op students on behalf of WATonomous, achieving an employer rating of 8.3 / 10. To date, we have supported 14 full-time co-ops, who have worked on projects ranging from guided soft target fabrication to action classification in video streams. 

### Summer 2022 Cohort

*Alexander and Eddy*: Action Classification

*Bao*: Mapping and Localization

*Julian*: Guided Soft Target Fabrication

### Winter 2021 Cohort

*Andrew*: Mapping and Localization

*Tae*: Simulation Map Creation

### Winter 2020 Cohort

*Frank*: Power Systems and Radar Driver

### Spring 2019 Cohort

*Tony*: Path Planning

*Wen*: Sensor Calibration

*Mitchell*: Power Systems

### Fall 2019 Cohort

*Rowan*: Project Management

*Chad*: Sensor Mounting

*Vinayak*: Dynamic Reconfigure