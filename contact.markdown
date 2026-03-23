---
layout: page
title: Contact
display_title: "Collaborative <span class='title-accent title-italic'>Inquiry</span>."
permalink: /contact/
kicker: Collaboration
lead: Seeking synergy at the intersection of multi-agent systems and reinforcement learning. Reach out for academic exchange, technical consultation, or research partnerships.
page_style: contact
---
<section class="contact-grid">
  <div class="contact-stack">
    <article class="contact-card contact-card-feature">
      <p class="contact-card-kicker">Current Base</p>
      <h2>{{ site.contact_location }}</h2>
      <p>{{ site.bio_affiliation }}</p>
      <div class="contact-mini-grid">
        <div>
          <span class="contact-mini-label">Hours</span>
          <strong>{{ site.contact_hours }}</strong>
        </div>
        <div>
          <span class="contact-mini-label">Timezone</span>
          <strong>{{ site.contact_region }}</strong>
        </div>
      </div>
    </article>

    <article class="contact-card">
      <p class="contact-card-kicker">Best Channel</p>
      <a class="contact-primary-link" href="mailto:{{ site.email }}">{{ site.email }}</a>
      <p>{{ site.contact_note }}</p>
    </article>

    <div class="contact-links-row">
      {%- if site.github_username -%}
      <a class="contact-pill" href="https://github.com/{{ site.github_username }}" target="_blank" rel="noopener">GitHub</a>
      {%- endif -%}
      {%- if site.linkedin_username -%}
      <a class="contact-pill" href="https://www.linkedin.com/in/{{ site.linkedin_username }}" target="_blank" rel="noopener">LinkedIn</a>
      {%- endif -%}
      {%- if site.leetcode_username -%}
      <a class="contact-pill" href="https://leetcode.com/{{ site.leetcode_username }}" target="_blank" rel="noopener">LeetCode</a>
      {%- endif -%}
      <a class="contact-pill" href="{{ '/feed.xml' | relative_url }}">RSS</a>
    </div>
  </div>

  <aside class="contact-aside">
    <article class="contact-card contact-card-outline">
      <p class="contact-card-kicker">Inquiry Types</p>
      <ul class="contact-topic-list">
        <li>Research collaboration and paper discussion</li>
        <li>Applied AI and engineering consulting</li>
        <li>Speaking, mentoring, and technical exchange</li>
      </ul>
    </article>

    <article class="contact-card contact-card-outline">
      <p class="contact-card-kicker">Response Style</p>
      <p>Concise messages with context, scope, and relevant links get the fastest response.</p>
      <a class="btn-primary btn-glow" href="mailto:{{ site.email }}">Start via Email</a>
    </article>
  </aside>
</section>
