---
layout: page
title: メンバー
permalink: /members/
---

{% assign section_order = "教職員/スタッフ|共同研究者|学生" | split: "|" %}
{% for section_name in section_order %}
{% assign section_members = site.data.members | where: "section", section_name %}
{% if section_members.size > 0 %}
<section>
  <h2>{{ section_name }}</h2>
  <ul>
    {% for member in section_members %}
    <li>
      <article>
        {% if member.photo %}
        <figure>
          <img src="{{ '/assets/images/members/' | append: member.photo | relative_url }}" alt="{{ member.name }}">
        </figure>
        {% endif %}
        <div>
          <h3>{{ member.name }}</h3>
          {% if member.name_en %}
          <p>{{ member.name_en }}</p>
          {% endif %}
          <p>{{ member.role }}</p>
          {% if member.affiliation %}
          <p>{{ member.affiliation }}</p>
          {% endif %}
          {% if member.url %}
          <p><a href="{{ member.url }}">{{ member.url }}</a></p>
          {% endif %}
          {% if member.tel %}
          <p>{{ member.tel }}</p>
          {% endif %}
          {% if member.email %}
          <p>{{ member.email }}</p>
          {% endif %}
        </div>
      </article>
    </li>
    {% endfor %}
  </ul>
</section>
{% endif %}
{% endfor %}
