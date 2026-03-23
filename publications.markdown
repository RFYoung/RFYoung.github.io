---
layout: page
title: Publications
display_title: "Publications <span class='title-accent'>&amp;</span> Research"
permalink: /publications/
kicker: Research Archive
lead: Exploring the intersections of reinforcement learning, multi-agent systems, and intelligent decision making.
page_style: publications
---
{%- assign current_year = "" -%}
<div class="publication-archive">
  {%- for pub in site.publications -%}
    {%- assign pub_year = pub.venue | split: ", " | last | strip -%}
    {%- if pub_year != current_year -%}
      {%- unless forloop.first -%}
        </div>
      </section>
      {%- endunless -%}
      {%- assign current_year = pub_year -%}
      <section class="publication-year-group">
        <div class="publication-year-rail">
          <h2 class="publication-year">{{ pub_year }}</h2>
        </div>
        <div class="publication-year-list">
    {%- endif -%}
          <article class="publication-entry anim-slide-in" style="--delay: {{ forloop.index | times: 0.08 }}s">
            <div class="publication-entry-header">
              <span class="publication-badge">{{ pub.venue | split: "," | first | strip }}</span>
            </div>
            <h3 class="publication-entry-title">{{ pub.title }}</h3>
            <p class="publication-entry-authors">{{ pub.authors }}</p>
            <p class="publication-entry-venue">{{ pub.venue }}</p>
            <div class="publication-entry-links">
              {%- include pub-links.html pub=pub -%}
            </div>
          </article>
    {%- if forloop.last -%}
        </div>
      </section>
    {%- endif -%}
  {%- endfor -%}
</div>
