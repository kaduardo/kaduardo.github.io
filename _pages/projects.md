---
layout: page
title: projects
permalink: /projects/
description: Some of the project I have been involved with.
---

I'm actively involved in R&D in the area of Software Engineering and its interplay with Information Security, focusing on the following topics Self-adaptive Software Systems, Service-orientation and Business Process, Secure by design, Digital Identity Management and Access Control.

I have been involved in different projects applying the above mentioned topics in the context of Smart City applications (e.g., smart building management, fine-grained access control), development and deployment of infrastructure and applications for Cloud Computing and IoT, techniques for multi-factor authentication and detection/response of insider threats.

I was one of the leaders of the cloud computing for science (CNC) work group of the Brazilian National Research and Education Network (RNP), which deployed a large scale cloud storage platform throughout Brazil and resulted in a spin-off company. This project resulted in the EduDrive service by RNP. More information can be found [here](201109_project).


{% assign sorted = site.projects | reverse %}
{% for project in sorted  %}
{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
