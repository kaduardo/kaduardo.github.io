---
layout: page
title: projects
permalink: /projects/
description: Some of the project I have been involved with.
---

I'm actively involved in R&D in the area of Software Engineering and its interplay with Information Security, exploring topics like Self-adaptive Software Systems, Service-orientation and Business Process, Secure by design, Digital Identity Management and Access Control.

I have been involved in different projects applying the above mentioned topics in the context of Smart City applications (e.g., smart building management, fine-grained access control), development and deployment of infrastructure and applications for IoT, techniques for multi-factor authentication and detection/response of insider threats.

I was the leader of the Infrastructure Work Package of the [Smart Metropolis](https://smartmetropolis.imd.ufrn.br/?page_id=361) project, a 5-years project aimed at the development of information and communication technology for human and smart cities.
I was responsible for overseeing cloud infrastructure deployment and operation, information security and access control, and ensuring the project adopted a ‘security by design’ approach to its systems from the outset.
A video of me talking about the Smart Metropolis project at the Smart Sheffield meetup can be found [here](https://www.smartsheffield.city/smartsheffield/notes-from-meetup-15-locking-down-the-smart-city).

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
