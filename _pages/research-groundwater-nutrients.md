---
layout: page
title: "How does nutrient composition in groundwater flow affect coastal ocean primary production?"
permalink: /research/groundwater-nutrients/
nav: false
# description: "Investigating nutrient transport via submarine groundwater discharge using ship-based, groundwater, and radioisotope sampling."
hero_image: /assets/img/research/boat.jpg
tags: [groundwater, radioisotopes, nutrients, coastal, primary production]
---

> Investigating nutrient transport via submarine groundwater discharge using ship-based, groundwater, and radioisotope sampling.

[View Full Project Paper (PDF)](/assets/img/research/catalystpaper.pdf){:target="_blank"}

## Overview
Researching the interaction between **groundwater discharge** and the **coastal ocean** is crucial because it transports key nutrients—particularly **nitrate, phosphate, and ammonia**—that help sustain phytoplankton and fisheries. In this study, we focused on **understudied links between anthropogenic activity and the outflow of nutrients in groundwater**, with implications for coastal ecosystem productivity and resilience.

## My role
- Conducted **ship-based ocean sampling** and **shore/nearshore groundwater sampling**.  
- Applied **radioisotope tracers** as effective indicators of groundwater inputs.  
- Built hands-on experience with **groundwater, radioisotope, and marine chemistry** techniques.  
- Organized field notes, metadata, and initial QA for downstream analyses.

## Tech & methods
- **Field:** ocean and groundwater sampling to characterize nutrient composition.  
- **Analytical:** nutrient measurements (NO₃⁻, PO₄³⁻, NH₄⁺) and **radioisotope tracers** for groundwater contributions.  
- **Synthesis:** relate nutrient signatures to potential **anthropogenic influences** affecting outflow.

## Results
- The work targeted **how increased human activity may alter nutrient export** from groundwater to coastal waters, with consequences for **primary production**.  
- A key takeaway is the **need for advances in real-time monitoring** to better resolve dynamic groundwater–ocean interactions under diverse anthropogenic pressures.

<!-- Single image (click to enlarge in-page) -->
<div class="img-strip">
  <img src="/assets/img/research/cg01.png" alt="Project image" onclick="openImgModal(this)">
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
    height:200px; /* increase/decrease if you want */
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



<!--## Links & media-->
<!--- [Methods / SOPs](#)-->
<!--- [Dataset / repo](#)-->
<!--- [Cruise notes / media](#)-->


<!--## Gallery (optional)-->
<!--![Coastal groundwater sampling aboard a small research vessel](/assets/img/research/boat.jpg)-->

