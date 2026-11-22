---
layout: default
title: Home
---

<section class="intro">
  <div class="intro-copy">
    <h1>Giuseppe Curci</h1>
    <p>
      I am an AI Researcher at <strong style="color: #d9378b;">Villanova AI</strong>, working on the development
      of the fully open Villanova LLMs family (among the best in Europe), where I am primarily responsible for post-training.
      <a href="https://huggingface.co/collections/VillanovaAI/villanova2"
         target="_blank" rel="noopener noreferrer"
         aria-label="Villanova AI Hugging Face collection">
        <i class="fa-solid fa-face-smile"></i>
      </a>
      Before that, I got my MS from the <strong>University of Trento</strong> 🇮🇹
      and conducted research under the supervision of Elisa Ricci.
    </p>
    <div class="intro-links">
      <a class="github-profile-link" href="https://github.com/giuseppecurci"
        target="_blank" rel="noopener noreferrer" aria-label="GitHub profile">
        <svg class="github-profile-icon" viewBox="0 0 16 16" aria-hidden="true">
          <path d="M8 .8a7.2 7.2 0 0 0-2.28 14.03c.36.07.49-.16.49-.35v-1.25c-2 .44-2.43-.85-2.43-.85-.33-.83-.8-1.05-.8-1.05-.65-.45.05-.44.05-.44.72.05 1.1.74 1.1.74.64 1.1 1.68.78 2.09.6.06-.47.25-.78.45-.96-1.6-.18-3.28-.8-3.28-3.56 0-.79.28-1.43.74-1.93-.08-.18-.32-.92.07-1.91 0 0 .6-.19 1.98.74a6.9 6.9 0 0 1 3.6 0c1.38-.93 1.98-.74 1.98-.74.39.99.15 1.73.07 1.91.46.5.74 1.14.74 1.93 0 2.77-1.68 3.38-3.29 3.56.26.22.48.66.48 1.33v1.98c0 .19.13.42.49.35A7.2 7.2 0 0 0 8 .8z"/>
        </svg>
        <span>GitHub</span>
      </a>

      <a href="https://scholar.google.com/citations?user=6O0KBCAAAAAJ&hl=en"
        target="_blank" rel="noopener noreferrer" aria-label="Google Scholar profile">
        🎓 Scholar
      </a>

      <a href="mailto:giuseppecurci49@gmail.com" aria-label="Email Giuseppe Curci">
        ✉️ Email
      </a>

      <a href="https://www.linkedin.com/in/giu-curci/"
        style="margin-left: 12px;"
        target="_blank" rel="noopener noreferrer"
        aria-label="LinkedIn profile">
        <svg class="github-profile-icon" viewBox="0 0 16 16" aria-hidden="true">
          <path d="M3.5 5.5H1V15h2.5V5.5zM2.25 1a1.5 1.5 0 1 0 0 3 1.5 1.5 0 0 0 0-3zM15 9.5c0-2.6-1.4-3.8-3.3-3.8-1.5 0-2.2.8-2.6 1.4V5.5H6.6V15h2.5v-4.7c0-1.2.2-2.4 1.8-2.4s1.6 1.4 1.6 2.5V15H15V9.5z"/>
        </svg>
        <span>LinkedIn</span>
      </a>
    </div>
  </div>

  <figure class="profile-figure">
    <img
      src="{{ '/assets/images/profile.jpeg' | relative_url }}"
      alt="Profile photo for Giuseppe Curci">
  </figure>
</section>

<section class="research-section">
  <h2>Research interests</h2>
  <div class="research-box">
    <p>
      My research focuses on <strong>large language models (LLMs)</strong>, particularly
      post-training. I am currently investigating on-policy learning, with an emphasis
      on improving its stability and efficiency. Previously, I worked on designing
      efficient, uncertainty-aware <strong>Transformer</strong> architectures.
      More broadly, I am interested in representation learning and the fundamental
      challenges behind building capable and reliable machine learning models.
    </p>
  </div>
</section>

<section class="publications-section">
  <h2>Publications &amp; preprints</h2>

  {% for paper in site.data.publications %}
  <article class="publication">
    <figure
      class="publication-figure{% if paper.image_variant %} publication-figure--{{ paper.image_variant }}{% endif %}"
      style="--figure-width: {{ paper.image_width }}px;
             --figure-height: {{ paper.image_height }}px;">
      <img src="{{ paper.image | relative_url }}" alt="{{ paper.image_alt }}">
    </figure>

    <div class="publication-content">
      <div class="publication-heading">
        <a class="paper-title" href="{{ paper.paper_url }}">{{ paper.title }}</a>

        <div class="paper-authors">
          {% for author in paper.authors %}
            {% if author.self %}
              <strong>{{ author.name }}</strong>
            {% else %}
              <span>{{ author.name }}</span>
            {% endif %}{% unless forloop.last %}, {% endunless %}
          {% endfor %}
        </div>

        <div class="paper-venue">
          <span>{{ paper.venue }}</span><span>, {{ paper.month }} {{ paper.year }}</span>
        </div>

        <div class="paper-links" aria-label="Paper links">
          {% for link in paper.links %}
            {% unless forloop.first %}<span class="link-separator" aria-hidden="true">|</span>{% endunless %}
            <a href="{{ link.url }}" class="paper-link" target="_blank" rel="noopener noreferrer">
              {% if link.icon == "paper" %}
                <svg class="link-icon" viewBox="0 0 16 16" aria-hidden="true">
                  <path d="M4 1.75h5l3 3v9.5H4zM9 1.75v3h3M6 8h4M6 10.5h4" />
                </svg>
              {% elsif link.icon == "github" %}
                <svg class="link-icon icon-fill" viewBox="0 0 16 16" aria-hidden="true">
                  <path d="M8 .8a7.2 7.2 0 0 0-2.28 14.03c.36.07.49-.16.49-.35v-1.25c-2 .44-2.43-.85-2.43-.85-.33-.83-.8-1.05-.8-1.05-.65-.45.05-.44.05-.44.72.05 1.1.74 1.1.74.64 1.1 1.68.78 2.09.6.06-.47.25-.78.45-.96-1.6-.18-3.28-.8-3.28-3.56 0-.79.28-1.43.74-1.93-.08-.18-.32-.92.07-1.91 0 0 .6-.19 1.98.74a6.9 6.9 0 0 1 3.6 0c1.38-.93 1.98-.74 1.98-.74.39.99.15 1.73.07 1.91.46.5.74 1.14.74 1.93 0 2.77-1.68 3.38-3.29 3.56.26.22.48.66.48 1.33v1.98c0 .19.13.42.49.35A7.2 7.2 0 0 0 8 .8z"/>
                </svg>
              {% elsif link.icon == "arxiv" %}
                <svg class="link-icon" viewBox="0 0 16 16" aria-hidden="true">
                  <path d="M2 3.2h12M2 6.1h12M2 9h8M2 11.9h8" />
                  <path d="M11 10.5l2.5 2.5L11 15.5" />
                </svg>
              {% else %}
                <svg class="link-icon" viewBox="0 0 16 16" aria-hidden="true">
                  <path d="M6.5 9.5l3-3M5.2 11.8H4a2.8 2.8 0 0 1 0-5.6h3M10.8 4.2H12a2.8 2.8 0 0 1 0 5.6H9" />
                </svg>
              {% endif %}
              {{ link.label }}
            </a>
          {% endfor %}
        </div>
      </div>

      <p class="paper-summary"><strong>tl;dr.</strong> <em>{{ paper.summary }}</em></p>
    </div>
  </article>
  {% endfor %}
</section>
