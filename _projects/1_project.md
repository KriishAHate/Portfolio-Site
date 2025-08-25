---
layout: page
title: Electric Cycle
# description: with background image
img: assets/img/cycle.png
importance: 1
# category: work
# related_publications: true
---
<!-- Centered, adjustable-size YouTube embed -->
<style>
  /* Wrapper: centered, with an adjustable max width via --w */
  .video-wrap{
    width: 100%;
    max-width: var(--w, 300px); /* <- change this inline to try sizes */
    margin-inline: auto;        /* centers it in the page column */
  }
  /* 16:9 responsive box */
  .video-wrap .frame{
    position: relative;
    width: 100%;
    padding-top: 56.25%; /* 16:9 aspect */
  }
  .video-wrap iframe{
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    border: 0;
    display: block;
  }
</style>

<!-- Try different sizes by changing --w below (e.g., 640px, 780px, 960px, 60ch, etc.) -->
<div class="video-wrap" style="--w: 880px;">
  <div class="frame">
    <iframe
      src="https://www.youtube.com/embed/afiizOBq-4g"
      title="Electric Cycle"
      loading="lazy"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen>
    </iframe>
  </div>
</div>


---

## Highlights

- End-to-end build: mechanical integration, wiring, safety, testing, and tuning  
- Modular electrical architecture for easy swapping/upgrading of components  
- Focus on reliability and maintainability: tidy harnessing, protected connectors, serviceable layout  
- Real-world testing on city streets (acceleration, braking, range feel)

## What I did

- Mechanical: mounting the drive system, aligning chainline / belt run, vibration isolation  
- Electrical: battery management, motor controller wiring, throttle/brake signaling, fusing & safety  
- Firmware/controls: controller configuration and basic tuning for smooth starts  
- Field testing: iterative test–fix–test cycles to validate performance and robustness

## Build Gallery

> Drop images in `/assets/img/projects/electric-cycle/` and update the file names below.

![Frame + drive mockup](/assets/img/projects/electric-cycle/01.jpg)
*Early fit-up of the drive & controls.*

![Harnessing & controller](/assets/img/projects/electric-cycle/02.jpg)
*Controller and wiring neatly packaged for serviceability.*

![Road test](/assets/img/projects/electric-cycle/03.jpg)
*Shakedown rides to tune throttle response and braking feel.*

## Notes & safety

- Use appropriate fusing, wire gauges, strain relief and insulation; protect against vibration and weather.  
- Validate braking performance and safe speeds for your local roads.  
- Charge/store batteries safely and follow manufacturer guidance.

## Links

- 🎥 Full video: <https://www.youtube.com/watch?v=afiizOBq-4g>
