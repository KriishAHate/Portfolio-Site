---
layout: page                      # or layout: project (if your theme has it)
title: "PROJECT TITLE"
permalink: /projects/<slug>/
date: 2025-01-01
image: /assets/img/projects/<slug>/cover.jpg     # OG/hero
tags: [category, skills, tools]
# Optional quick facts (shown below in the page body)
role: "Your specific responsibilities"
timeframe: "e.g., Jan–Apr 2024 (10 weeks)"
collaborators: "Names / orgs"
tools: "CAD, Python, Arduino, etc."
---

> **One-liner:** What the project is, who it’s for, and the result in one sentence.

<!-- Optional: hero video -->
<!--
<div style="position:relative; padding-top:56.25%; margin:0 0 1rem 0;">
  <iframe src="https://www.youtube.com/embed/VIDEO_ID" title="Demo"
          allowfullscreen style="position:absolute; inset:0; width:100%; height:100%; border:0;"></iframe>
</div>
-->

![Cover image]({{ '/assets/img/projects/<slug>/cover.jpg' | relative_url }})

---

## Quick facts
| | |
|---|---|
| **Context** | Class / personal / client / research; constraints & success criteria |
| **Role** | {{ page.role }} |
| **Timeframe** | {{ page.timeframe }} |
| **Collaborators** | {{ page.collaborators }} |
| **Tools** | {{ page.tools }} |

---

## 1) Context
Why this project existed. Problem background, users, constraints (budget, materials, time, safety), and how success is measured.

**Parameters / requirements**
- Requirement A (with numeric target if possible)
- Requirement B
- Edge cases / environments

---

## 2) Your role
What *you* owned end-to-end. Be concrete about independent contributions and decision-making.

- Owned: ___, ___, ___  
- Contributed to: ___ (with X, Y)
- Interfaces with: ___ (EE/FW/ME, vendors, lab)

---

## 3) What, How, **Why**
Describe the solution, how you built it, and—most important—**why** you chose that approach.

**System at a glance**
- Architecture / concept sketch (link below)
- Key tradeoffs & rationale (why X over Y)
- Safety, manufacturability, cost, serviceability

_Visuals_  
![Concept]({{ '/assets/img/projects/<slug>/concept-1.jpg' | relative_url }})
![Architecture]({{ '/assets/img/projects/<slug>/arch-1.jpg' | relative_url }})

---

## 4) Process (show your work)
Short, visual timeline of the build with checks and learning.

**Milestones**
1. Research & requirements → insight …
2. Prototyping 0 → 1: what I tested, what failed, what changed
3. Design iteration (CAD/EE/FW) → validation
4. Integration & test → fixes

**Sketches / CAD / code**
- CAD screenshots, BOM snippets, test jigs
- Links to repos or gists if public

_Visuals_  
<div>
  <img src="{{ '/assets/img/projects/<slug>/proto-1.jpg' | relative_url }}" style="width:32%;margin-right:1%">
  <img src="{{ '/assets/img/projects/<slug>/proto-2.jpg' | relative_url }}" style="width:32%;margin-right:1%">
  <img src="{{ '/assets/img/projects/<slug>/proto-3.jpg' | relative_url }}" style="width:32%">
</div>

---

## 5) Results & verification
How you measured success (numbers > adjectives).

- Metric 1: target → actual (method)
- Metric 2: …
- Reliability / safety checks
- Cost & time summary (if relevant)

**Outcome**
- Deployed? Demoed? Used by N people?
- Awards / publications (links)

---

## 6) What I’d improve next
Top 3 follow-ups and why. (This shows judgment.)

- Improvement A → expected impact
- Improvement B → tradeoff
- Tech debt to pay down

---

## 7) Links & media
- [Repo / code](#) • [Datasheet / BOM](#) • [Poster / slide deck](#) • [Demo video](#)

_Extra gallery (optional)_  
![Detail]({{ '/assets/img/projects/<slug>/detail-1.jpg' | relative_url }})
![Test rig]({{ '/assets/img/projects/<slug>/test-1.jpg' | relative_url }})
