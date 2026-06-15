---
layout: page
title: "low-cost design of a novel temperature and sound monitoring sensor box"
permalink: /research/common-senses/
nav: false
---

---

📄 [Download Portfolio Entry (PDF)](/assets/img/projects/Sensor_box_project.pdf){:target="_blank"} 

📖 [Read the full thesis](https://hdl.handle.net/2047/D20859626)

---

## Overview

Most urban environmental monitoring systems are too sparse or expensive to capture conditions at the neighborhood scale — leaving residents exposed to heat and noise hazards that go unmeasured and unaddressed.

As part of my Master's thesis at the [Environmental Sensors Lab](https://envsensorslab.sites.northeastern.edu/) at Northeastern University, I developed a solar-powered sensor box that measures temperature, humidity, and sound every minute and uploads data via LTE in near-real time. At under $500 per unit, it makes dense community-scale deployments feasible where commercial devices cannot. **55 units are now deployed across Boston's Blue Hill neighborhood**, generating continuous environmental data to support resident advocacy and more equitable urban planning.

## What I did

- Designed the full hardware system — enclosure and electronics integration — through iterative prototyping and bench testing
- Validated sensor accuracy, power consumption, solar charging performance, and weather resistance across 5 prototypes
- Built a standardized manufacturing workflow in an on-campus machine shop, producing 55 units with 100% QA/QC pass rate
- Led field deployment including LTE connectivity validation and ongoing reliability checks across all deployed units

## Results

- **55 units deployed** across Blue Hill, Boston — June 2025
- **Zero mechanical failures** observed through April 2026
- Data actively used by community partners for environmental advocacy



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