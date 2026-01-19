---
layout: page
title: "Denitrification process rates along a gradient of salt-marsh health"
permalink: /research/denitrification-salt-marsh/
nav: false
# description: "Independent study to relate marsh condition and historical ditching to denitrification rates, leveraging multispectral drone mapping as context."
hero_image: /assets/img/research/denitrification.jpg
tags: [biogeochemistry, denitrification, wetlands, nutrient cycling]
---

> Independent study to relate marsh condition and historical ditching to denitrification rates, leveraging multispectral drone mapping as context.

## Overview
Following the NJDEP mapping work, I developed an **independent proposal** to examine how **marsh condition and historical ditching** influence **denitrification rates**. The goal is to place measured rates in the context of **multispectral drone indices** and site condition to understand **ecosystem functioning and service retention** across a marsh-health gradient.

[View Full Project Report (PDF)](/assets/img/denitrificationreport.pdf){:target="_blank"}

## My role
- Designed the study and field sampling plan across contrasting marsh conditions.  
- Coordinated with the drone-imagery team to align sites/indices with rate measurements.  
- Managed data collection, QA, and organization for analysis.

## Tech & methods
- **Field:** Transects across ditching gradients; pore-water/soil sampling at fixed plots.  
- **Rates:** Potential denitrification assays / incubation approaches (site-appropriate).  
- **Context data:** Use of **multispectral drone products** and site notes for interpretation.

## Results
- Working hypothesis: **ditching and degraded condition reduce denitrification capacity**.  
- Outputs will link rate measurements to spectral indices and site condition.

<!-- Single image (click to enlarge in-page) -->
<div class="img-strip">
  <img src="/assets/img/research/dn011.png" alt="dn01" onclick="openImgModal(this)">
</div>

<!-- Modal -->
<div id="imgModal" class="img-modal" onclick="closeImgModal(event)">
  <span class="img-close" onclick="closeImgModal(event)">&times;</span>
  <img class="img-modal-content" id="imgModalContent" alt="">
</div>

<style>
  .img-strip{
    display:flex;
    padding:12px 0;
    margin:10px 0 24px 0;
  }
  .img-strip img{
    height:200px;
    width:auto;
    border-radius:12px;
    cursor: zoom-in;
  }

  .img-modal{
    display:none;
    position:fixed;
    z-index:9999;
    left:0; top:0;
    width:100%; height:100%;
    background: rgba(0,0,0,0.85);
    align-items:center;
    justify-content:center;
    padding:24px;
  }
  .img-modal-content{
    max-width:92vw;
    max-height:88vh;
    border-radius:14px;
  }
  .img-close{
    position:fixed;
    top:18px; right:24px;
    font-size:40px;
    color:white;
    cursor:pointer;
    line-height:1;
    user-select:none;
  }
</style>

<script>
  function openImgModal(img){
    const modal = document.getElementById("imgModal");
    const modalImg = document.getElementById("imgModalContent");
    modal.style.display = "flex";
    modalImg.src = img.src;
    modalImg.alt = img.alt || "";
    document.body.style.overflow = "hidden";
  }

  function closeImgModal(e){
    const modal = document.getElementById("imgModal");
    const modalImg = document.getElementById("imgModalContent");
    if (e.target.id === "imgModal" || e.target.className === "img-close") {
      modal.style.display = "none";
      modalImg.src = "";
      document.body.style.overflow = "";
    }
  }

  document.addEventListener("keydown", (e) => {
    if (e.key === "Escape") {
      const modal = document.getElementById("imgModal");
      const modalImg = document.getElementById("imgModalContent");
      modal.style.display = "none";
      modalImg.src = "";
      document.body.style.overflow = "";
    }
  });
</script>


<!--- ## Links & media-->
<!--- [Study plan / doc](#)-->
<!--- - [Data / repo](#)-->
<!--- - [Poster / slides](#)-->


<!--- ## Gallery (optional)-->
<!--- ![Sampling along a salt-marsh creek and channels](/assets/img/research/denitrification.jpg)-->

