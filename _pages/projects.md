---
layout: page
title: projects
permalink: /projects/
description: Some of the project I have been involved with.
nav: true
---

I'm actively involved in R&D in the area of Software Engineering and its interplay with Information Security, focusing on the following topics Self-adaptive Software Systems, Service-orientation and Business Process, Secure by design, Digital Identity Management and Access Control.

I have been involved in different projects applying the above mentioned topics in the context of Smart City applications (e.g., smart building management, fine-grained access control), development and deployment of infrastructure and applications for Cloud Computing and IoT, techniques for multi-factor authentication and detection/response of insider threats.

I was one of the leaders of the cloud computing for science (CNC) work group of the Brazilian National Research and Education Network (RNP), which deployed a large scale cloud storage platform throughout Brazil and resulted in a spin-off company. This project resulted in the EduDrive service by RNP. More information can be found [here](201109_project).

<div class="projects grid">

  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ project.title }}</h2>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if project.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ project.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
