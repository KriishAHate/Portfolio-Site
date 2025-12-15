---
layout: page
title: "SCALUP — Small Customizable Autonomous Logging Underwater Platform"
permalink: /research/scalup/
nav: false
# description: "Autonomous underwater logging platform; embedded systems and comms (I²C/UART); antifouling efficacy experiments."
# hero_image: /assets/img/research/dive.jpg   # optional header image
# tags: [embedded systems, i2c, uart, teensy, antifouling]
---

## Overview
I worked on a **small, customizable autonomous logging platform** for underwater deployments. 
> Low-cost platforms such as these provide wider accessibility to underserved populations and help promote **citizen science**.

## My role
- Embedded-system bring-up and **systems integration** across sensors, storage, and power.
- Firmware design with an emphasis on **software reliability** (watchdogs, logging safeguards, sanity checks).
- Planning and execution of **antifouling efficacy experiments** and data analysis.

## Tech & methods
- **Comms / protocols:** I²C, UART  
- **Microcontrollers:** Teensy  
- **Languages / tools:** C/C++, **Embedded C**, Arduino **Sketch**, Python, MATLAB  
<!-- - Additional hardware and bench tooling across a variety of platforms. -->

<!-- Single image (click to enlarge in-page) -->
<div class="img-strip">
  <img src="/assets/img/research/dn01.png" alt="dn01" onclick="openImgModal(this)">
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

  
<!--- 
## Results / links
- Antifouling test campaign completed; logging stack validated in water.
- [Dataset or PDF](#)  
- [Video](#)
-->
