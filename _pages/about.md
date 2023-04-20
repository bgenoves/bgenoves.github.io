---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---


{% for member in site.data.pi %}
<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.info }}</i></h4>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}{% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a> {% endif %}{% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}{% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}{% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a> {% endif %}{% if member.linkedin %} <a href="{{ member.linkedin }}" target="_blank"><i class="fa fa-linkedin fa-3x"></i></a> {% endif %}

  
  <ul style="overflow: hidden">
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 3 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 4 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education4 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 5 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education4 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education5 | replace: "-","&#8211;"}} </li>
  {% endif %}
  {% if member.number_educ == 6 %}
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education4 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education5 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education6 | replace: "-","&#8211;"}} </li>
  {% endif %}
  </ul>
</div>
</div>
</div>
{% endfor %}

<div class="jumbotron">
I am a Marie Curie postdoctoral fellow in the Electrical and Computer Engineering Department at the <b>University of Virginia</b>, USA (2023-present).

I completed the PhD in the <b>University Carlos III of Madrid</b> in 2019 with the maximum grade and the cum laude recognition, under the supervision of Dr. Victor P. Gil Jimenez in the Communications Research group, led by Prof. Ana Garcia Armada. During the PhD studies I obtained two FPU mobility grants to work as a visiting scholar in <b>Southampton University</b> and <b>The University of Edinburgh</b> (each for 3 months), under the supervision of Prof. Lajos Hanzo and Prof. Harald Haas, respectively.

After my PhD studies, I joined in 2019 <b>IMDEA Networks Institute</b> as a postdoctoral researcher, in Dr. Domenico Giustiniano’s group, to work in VLC for low-power Internet of Things and battery-free scenarios, while co-supervising PhD and MSc students. I also performed as project manager for ENLIGHT’EM H2020-MSCA-ITN-2018 nº 814215. In 2020 I was awarded by Ministry of Science, Innovation and Universities (Spain) with a competitive grant whose aim is to support early-stage researchers until mid-2022 (Juan de la Cierva – Formación grant). 

From January 2023, I am a Marie Curie postdoctoral fellow. During the outgoing phase of the fellowship (Jan 23 – Dec 24) I will be working at the University of Virginia (USA), and the return phase (Jan 25 - Dec 25) of the MSCA fellowship will be at the UC3M (Spain). The objective of the project is to design RIS-based LiFi for enabling autonomous IoT devices, studying the boundaries on communication and energy harvesting. Find more details in [(RISA-VLC)](https://cordis.europa.eu/project/id/101061853). 

My research interests include visible light communication, Internet of Things, low-power wireless communications and mobile communications. For more detail on my work in some of these areas, head over to the Publications tab!
</div>

[comment]: <>   <h3>PhD Opportunities</h3>
  
[comment]: <>   I am currently accepting new PhD students.... 
  
[comment]: <>   <div class="jumbotron">
[comment]: <b>...</b>

[comment]: <> ...  
[comment]: </div>

{% if site.data.grants %}
<div class="jumbotron">
### Grants
<ul>
{% for grant in site.data.grants %}
 <li> {{ grant.name }} </li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="jumbotron">
### Awards
<ul>
{% for award in site.data.awards %}
 <li> {{ award.name | replace: "-","&#8211;"}} </li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.people %}
<div class="jumbotron">
### Students and mentoring
<ul>
{% for student in site.data.people %}
 <li> {{ student.name }}, {{student.location}} ({{student.degree}}, {{student.year}}) </li>
{% endfor %}
</ul>
</div>
{% endif %}


