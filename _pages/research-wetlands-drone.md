---
layout: page
title: "Assessing salt-marsh health using multispectral imagery from drones"
permalink: /research/wetlands-drone/
nav: false
# description: "NJDEP project pairing drone multispectral imagery with pore-water chemistry ground truth to assess the health of New Jersey’s tidal wetlands."
hero_image: /assets/img/research/field.jpg   # change or remove if you don't want a hero image
tags: [wetlands, remote sensing, drones, pore-water chemistry]
---

> NJDEP project pairing drone multispectral imagery with pore-water chemistry ground truth to assess the health of New Jersey’s tidal wetlands.

## Overview
As part of an **NJDEP (New Jersey Department of Environmental Protection)** effort to develop a **novel method for assessing the health of New Jersey’s ~200,000 acres of tidal wetlands**, we paired **multispectral drone imagery** with **on-site pore-water chemistry**.  
This was part of a project that focused on developing a **faster, cost-effective, and labor-efficient** wetland mapping and condition assessment method.

## My role
- Learned and performed **pore-water sampling** as the **ground-truthing** component for drone flights.  
- Coordinated field collection with the flight team to align sampling locations/times with imagery coverage.  
- Assisted with basic QA/labeling and data handoff for downstream analysis and mapping.

## Tech & methods
- **Remote sensing:** Multispectral drone imagery (vegetation/health indices from spectral bands).  
- **Ground truth:** In-situ **pore-water chemistry** sampling at targeted wetland locations.  
- **Workflow:** Field planning → flights → pore-water sampling → data collation for mapping/assessment.  

## Results
- The resulting workflow **reduced assessment time** while providing a **cost-effective** way to map wetland condition.  
- Ground-truth chemistry increased confidence in image-based estimates of wetland health.

<!-- Image strip (click to enlarge in-page) -->
<div class="img-strip">
  <img src="/assets/img/research/md01.JPG" alt="Photo 1" onclick="openImgModal(this)">
  <img src="/assets/img/research/md02.JPG" alt="Photo 2" onclick="openImgModal(this)">
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


<!--## Links & media-->
<!--- [PDF / poster](#)-->
<!--- [Dataset / repo](#)-->
<!--- [Video / demo](#)-->

<!--## Gallery (optional)-->
<!--![Field sampling during drone operations](/assets/img/research/field.jpg)-->

