---
layout: default
title: Frequenty Asked Questions
permalink: /faq/
categories:
- name: About us
  questions:
  - question: Who are you?
    answer: We are a group of 70+ women from Canberra who work or study in areas such as IT, cybersecuity, software engineering, computer science, research and mathematics. We come from a wide range of organisations like the Australian Signals Directorate, CSIRO, Telstra, Australian Government, ANU and high schools. We contribute our time larely or (more usually) entirely voluntarily.
  - question: Why are you doing this?
    answer: We are passionate about coding and seeing more women enter careers in coding! We've all experienced the barriers to entry into our field for women and we want to break those down for the next generation.
  - question: Who supports you?
    answer: The majority of our financial support comes from the Australian Signals Directorate, with some contributions from other employers in the form of time off in lieu.
  - question: How did you start?
    answer: Canberra Girls' Programming Network is a chapter of Girls' Programming Network (GPN) Australia. GPN started in Sydney through the University of Sydney and the National Computer Science School. In 2016 GPN expanded to Canberra and we became the first interstate chapter. Since then, chapters have started in Perth and Cairns.
- name: About the workshops
  questions:
  - question: sdf
    answer: sdf
- name: About tutoring
  questions:
  - question: sdf
    answer: sdf
---

<div id="faq" role="tablist">
{% for category in page.categories %}
  <div class="bottom-padded">
    <h3>{{ category.name }}</h3>
    {% for question in category.questions %}
    <div class="card shadow">
      <div class="card-header" role="tab" id="heading{{ category.name | slugify }}{{ forloop.index }}">
        <h5 class="mb-0">
          <a class="collapsed" data-toggle="collapse" href="#collapse{{ category.name | slugify }}{{ forloop.index }}" aria-expanded="false" aria-controls="collapse{{ category.name | slugify }}{{ forloop.index }}">
            {{ question.question }}
          </a>
        </h5>
      </div>
      <div id="collapse{{ category.name | slugify }}{{ forloop.index }}" class="collapse" role="tabpanel" aria-labelledby="heading{{ category.name | slugify }}{{ forloop.index }}" data-parent="#faq">
        <div class="card-block">
          {{ question.answer }}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
{% endfor %}
</div>
