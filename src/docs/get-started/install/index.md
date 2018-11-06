---
title: Install
next:
  title: Set up an editor
  path: /get-started/editor
toc: false
---

Flutter를 개발하려는 운영체제를 선택하세요.

<div class="card-deck mb-8">
{% for os in site.os-list %}
  <a class="card" href="/get-started/install/{{os | downcase}}">
    <div class="card-body">
      <header class="card-title text-center m-0">
        {{os}}
        <i class="fab fa-{{os | downcase}}"></i>
      </header>
    </div>
  </a>
{% endfor %}
</div>

