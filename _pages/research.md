---
layout: default
title: research
permalink: /research/
nav: true
nav_order: 2        # change this number to where you want it to appear in the menu
---

<!-- ===========================
     Research cards (2-column grid)
     - Paste this block into `_pages/research.md`
     - Each card links to a detailed project page
     - Replace image paths, titles, tags, and hrefs
     =========================== -->

<style>
  /* ---------- Layout: responsive 2-column grid ---------- */
  .grid2 {
    display: grid;                             /* turn on CSS grid */
    grid-template-columns: repeat(2, 1fr);     /* 2 equal columns on wide screens */
    gap: 1rem;                                 /* space between cards */
  }

  /* Collapse to single column on small screens */
  @media (max-width: 720px){
    .grid2 { grid-template-columns: 1fr; }
  }

  /* ---------- Card + link behavior ---------- */
  .cardlink {                                  /* make the whole card clickable */
    text-decoration: none;                     /* remove underline on the link wrapper */
    color: inherit;                            /* use surrounding text color */
    display: block;
  }

  .card {
    padding: .9rem 1rem;                       /* inner spacing */
    border: 1px solid rgba(0,0,0,.08);         /* subtle border in light mode */
    border-radius: 12px;                       /* rounded corners */
    transition: transform .15s ease,
                box-shadow .15s ease,
                border-color .15s ease;        /* smooth hover */
    box-shadow: 0 2px 10px rgba(0,0,0,.05);    /* soft elevation */
  }

  .card:hover {                                /* lift on hover */
    transform: translateY(-2px);
    box-shadow: 0 10px 24px rgba(0,0,0,.10);
  }

  /* ---------- Project image thumbnail ---------- */
  .thumb {
    width: 100%;
    aspect-ratio: 16/9;                        /* keeps a clean 16:9 box */
    object-fit: cover;                         /* crop to fill box without distortion */
    border-radius: 10px;
    display: block;
    margin: 0 0 .6rem 0;                       /* space below image */
  }

  /* ---------- Titles + tags ---------- */
  .card h3 {
    margin: .15rem 0 .5rem;
    font-size: 1.05rem;
    line-height: 1.25;
  }

  .tags {                                      /* inline “pill” list */
    display: flex;
    flex-wrap: wrap;
    gap: .45rem;
  }

  .tag {
    border: 1px solid rgba(0,0,0,.12);
    padding: .18rem .55rem;
    border-radius: 999px;                      /* fully rounded pill */
    font-size: .8rem;
    color: #555;
  }

  /* ---------- Dark mode tweaks ---------- */
  @media (prefers-color-scheme: dark){
    .card { border-color: rgba(255,255,255,.12);
            box-shadow: 0 2px 10px rgba(0,0,0,.25); }
    .card:hover { box-shadow: 0 10px 24px rgba(0,0,0,.35); }
    .tag { border-color: rgba(255,255,255,.16); color:#bdbdbd; }
  }
</style>

<div class="grid2">
  <!-- ================= CARD TEMPLATE =================
       Copy/paste one of the cards below and edit:
       - href:  link to the detailed page (e.g., /research/my-project/)
       - src:   image path (put files in assets/img/research/)
       - alt:   short, accessible image description
       - <h3>:  project title
       - <span class="tag">…</span>: keywords
       ================================================== -->

<!-- Common Senses -->
<a class="cardlink" href="{{ '/research/common-senses/' | relative_url }}">
  <div class="card">
    <img class="thumb"
         src="{{ '/assets/img/research/sensorbox.jpeg' | relative_url }}"
         alt="Portable 'Common Senses' sensor box measuring temperature and sound"
         loading="lazy" decoding="async">
    <h3>Common Senses — portable sensor box for temperature & sound</h3>
    <div class="tags">
      <span class="tag">Arduino</span>
      <span class="tag">C/C++</span>
      <span class="tag">Mechanical Design</span>
    </div>
  </div>
</a>

  <!-- SCALUP -->
  <a class="cardlink" href="{{ '/research/scalup/' | relative_url }}">
    <div class="card">
      <!-- Replace with your image; ensure the file exists -->
      <img class="thumb"
           src="{{ '/assets/img/research/dive.jpg' | relative_url }}"
           alt="SCALUP autonomous logging platform"
           loading="lazy" decoding="async">
      <!-- Project title -->
      <h3>SCALUP — Small Customizable Autonomous Logging Underwater Platform</h3>
      <!-- Tags/keywords (add/remove as needed) -->
      <div class="tags">
        <span class="tag">Embedded Systems</span>
        <span class="tag">C/C++</span>
        <span class="tag">Python</span>
        <span class="tag">Teensy</span>
      </div>
    </div>
  </a>

  <!-- Denitrification gradient -->
  <a class="cardlink" href="{{ '/research/denitrification-salt-marsh/' | relative_url }}">
    <div class="card">
      <img class="thumb"
           src="{{ '/assets/img/research/denitrification.jpg' | relative_url }}"
           alt="Salt-marsh creek and channels"
           loading="lazy" decoding="async">
      <h3>Denitrification process rates along a gradient of salt-marsh health</h3>
      <div class="tags">
        <span class="tag">Biogeochemistry</span>
        <span class="tag">Denitrification</span>
      </div>
    </div>
  </a>

  <!-- Salt-marsh multispectral -->
  <a class="cardlink" href="{{ '/research/wetlands-drone/' | relative_url }}">
    <div class="card">
      <img class="thumb"
           src="{{ '/assets/img/research/field.jpg' | relative_url }}"
           alt="Multispectral drone imagery over tidal wetlands"
           loading="lazy" decoding="async">
      <h3>Assessing salt-marsh health using multispectral imagery from drones</h3>
      <div class="tags">
        <span class="tag">Remote Sensing</span>
        <span class="tag">Wetlands</span>
        <span class="tag">Pore-water Chemistry</span>
      </div>
    </div>
  </a>

  <!-- Groundwater nutrients -->
  <a class="cardlink" href="{{ '/research/groundwater-nutrients/' | relative_url }}">
    <div class="card">
      <img class="thumb"
           src="{{ '/assets/img/research/boat.jpg' | relative_url }}"
           alt="Coastal groundwater sampling"
           loading="lazy" decoding="async">
      <h3>How does nutrient composition in groundwater flow affect coastal ocean primary production?</h3>
      <div class="tags">
        <span class="tag">Groundwater</span>
        <span class="tag">Radioisotopes</span>
        <span class="tag">Primary Production</span>
      </div>
    </div>
  </a>

</div>
