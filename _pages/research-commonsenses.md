---
layout: page
title: "low-cost design of a novel temperature and sound monitoring sensor box"
permalink: /research/common-senses/
nav: false
---


## Overview

Cities expose residents to environmental stressors such as extreme heat and noise that directly affect health and quality of life, yet most monitoring systems are too sparse or expensive to capture neighborhood-scale conditions. To address this gap, a low-cost, solar-powered environmental sensor box was developed as part of my Master’s thesis work at the [Environmental Sensors Lab](https://envsensorslab.sites.northeastern.edu/) to measure temperature, humidity, and sound every minute and upload data via LTE in near-real time. Designed to cost under $500, the system enables dense, community-scale deployments that are not feasible with commercial devices, and 55 units are now deployed across Boston’s Blue Hill neighborhood to support resident advocacy and more equitable urban planning.

## My role

- Led **hardware design**, including enclosure and electronics prototyping  
- Supported **manufacturing and assembly** using standardized, repeatable processes in an on-campus machine shop  
- Conducted **bench-level testing** for sensor accuracy, power performance, and weather resistance  
- Supported **field deployment**, including LTE connectivity validation and solar charging performance  
- Performed **ongoing maintenance and reliability checks** across deployed units  

<!-- Image strip (click to enlarge in-page) -->
<div class="img-strip">
  <img src="/assets/img/research/IMG_0754.JPG" alt="Photo 1" onclick="openImgModal(this)">
  <img src="/assets/img/research/IMG_0938.jpg" alt="Photo 2" onclick="openImgModal(this)">
  <img src="/assets/img/research/IMG_2410.jpg" alt="Photo 3" onclick="openImgModal(this)">
  <img src="/assets/img/research/IMG_2458.jpg" alt="Photo 4" onclick="openImgModal(this)">
  <img src="/assets/img/research/IMG_2736.jpg" alt="Photo 5" onclick="openImgModal(this)">
</div>

<!-- Modal -->
<div id="imgModal" class="img-modal" onclick="closeImgModal(event)">
  <span class="img-close" onclick="closeImgModal(event)">&times;</span>
  <img class="img-modal-content" id="imgModalContent" alt="">
</div>

<style>
  .img-strip{
    display:flex; gap:12px; overflow-x:auto;
    padding:12px 0; margin:10px 0 24px 0;
  }
  .img-strip img{
    height:140px; width:auto; border-radius:12px;
    cursor: zoom-in;
  }

  .img-modal{
    display:none;
    position:fixed; z-index:9999;
    left:0; top:0; width:100%; height:100%;
    background: rgba(0,0,0,0.85);
    align-items:center; justify-content:center;
    padding: 24px;
  }
  .img-modal-content{
    max-width: 92vw;
    max-height: 88vh;
    border-radius: 14px;
  }
  .img-close{
    position: fixed;
    top: 18px; right: 24px;
    font-size: 40px;
    color: white;
    cursor: pointer;
    line-height: 1;
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




<!--
## Tech & methods
- **Arduino** microcontroller (C/C++)
- Temperature & microphone modules, ADC
- 3D-printed/laser-cut enclosure; fast-prototyping

## Results / links
- [Repo / docs](#)
- [Demo video](#)
  -->

