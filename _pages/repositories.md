---
layout: page
permalink: /repositories/
title: repositories
description: Selected project repositories.
nav: true
nav_order: 4
---

<div class="repositories">
  <div class="row row-cols-1 row-cols-md-3">
    {% for repo in site.data.repositories.repos %}
      <div class="col">
        <a href="{{ repo.url }}" target="_blank" rel="noopener noreferrer">
          <div class="card h-100 hoverable">
            <div class="card-body">
              <h2 class="card-title">{{ repo.name }}</h2>
              <p class="card-text">{{ repo.description }}</p>
              <div class="row ml-1 mr-1 p-0 align-items-center justify-content-between">
                {% if repo.language %}
                  <span class="language-badge">{{ repo.language }}</span>
                {% endif %}
                <i class="fa-brands fa-github gh-icon"></i>
              </div>
            </div>
          </div>
        </a>
      </div>
    {% endfor %}
  </div>
</div>
