---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D in Version Control Theory, GitHub University, 2018 (expected)
* M.S. in Jekyll, GitHub University, 2014
* B.S. in GitHub, GitHub University, 2012

Work experience
======
* Spring 2024: Academic Pages Collaborator
  * GitHub University
  * Duties includes: Updates and improvements to template
  * Supervisor: The Users

* Fall 2015: Research Assistant
  * GitHub University
  * Duties included: Merging pull requests
  * Supervisor: Professor Hub

* Summer 2015: Research Assistant
  * GitHub University
  * Duties included: Tagging issues
  * Supervisor: Professor Git
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======

<div style="max-width: 850px; line-height: 1.8; font-size: 16px;">

  <div style="text-align: center; margin-bottom: 30px;">
    <img src="{{ site.baseurl }}/images/profile_photo_wei.png"
         alt="Wei Xiangqing profile photo"
         style="width: 240px; height: 240px; object-fit: cover; border-radius: 50%; box-shadow: 0 4px 12px rgba(0,0,0,0.18);">
  </div>

  <h1>Wei Xiangqing</h1>

  <p>
    I am currently a research assistant at Chiba University, Japan. My research focuses on AI accelerator architecture,
    reinforcement-learning-driven scheduling, and hardware-software co-design for neural network accelerators.
  </p>

  <p>
    <strong>Master’s Degree in Integrated Circuit Engineering</strong><br>
    Guizhou University, China<br>
    Research area: RISC-V processor design, integer execution units, Booth multiplication, SRT division, and digital circuit design.
  </p>

  <h2>Research Interests</h2>

  <ul>
    <li>AI hardware architecture</li>
    <li>NPU and FPGA-based DNN acceleration</li>
    <li>Reinforcement learning </li>
    <li>Hardware-software co-design</li>
  </ul>
