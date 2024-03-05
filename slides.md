---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
persist: false
defaults:
  foo: true
transition: slide-left
title: Introduction to Artificial Intelligence and Computer Vision
mdc: true
---

# Artificial Intelligence and Computer Vision

Workshop

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <!-- <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button> -->
  <a href="https://github.com/antoniomtz/ai-cv-workshop" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-left
---

# Outline

<ol>
  <li>Introduction of AI and CV</li>
  <li>AI and CV Basics</li>
  <li>Intel SW and HW</li>
  <li>Intel openVINO toolkit</li>
  <li>Hands-on with openVINO</li>
  <li>Questions</li>
</ol>    

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<!-- <style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style> -->

<!--
Here is another comment.
-->

---
transition: slide-left
---

# Table of contents

<Toc maxDepth="1"></Toc>

---
layout: cover
transition: slide-left
---
# Introduction of AI and CV

---
transition: slide-left
level: 2
---

# Use case: Intelligence queue management
<br/>
<center>
  <video width="600" height="300" controls>
    <source src="/assets/intelligent-queue.mp4" type="video/mp4">
  </video>
</center>

---
layout: image-right
transition: slide-left
image: /assets/intel-ai-graphic.png
---

# Definitions

* **AI** involves teaching computers to process data in a way that **mimics the human brain**.
* **Computer Vision** is a field of AI that focuses on enabling computers to **interpret visual data**
* AI and CV are important in our lives for several reasons:
  * Automation
  * Healthcare
  * Safety
  * Customer experience

---
transition: slide-left
---
# Computer Vision Use Cases

<div grid="~ cols-2 gap-4">
  <div>
    <ul>
      <li>Robotics</li>
      <li>Facial Recognition</li>
      <li>Object Detection</li>
      <li>Medical Imaging</li>
    </ul>
  </div>

  <div>
    <img src="/assets/cv-use-cases.jpg" />
  </div>

</div>

---
transition: slide-left
---
# Robotics Use Cases

* Self-driving Cars
  * Commercial vehicles
  * Delivery robots
* Surveillance robots
* Drones

<div grid="~ cols-2 gap-2" m="t-2">

  <img border="rounded" src="/assets/Autonomous-driving-Barcelona.jpg" alt="">

  <iframe width="450" height="250" src="https://www.youtube.com/embed/kN0MLclnWa0?si=w1yJBFJ_IS81y-eo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

</div>


---
transition: slide-left
---
# Object Detection Use Cases

<div grid="~ cols-2 gap-4">
  <div>
    <ul>
      <li>Retail:
        <ul>
          <li>Automated Self Checkout</li>
          <li>Inventory Magagement</li>
          <li>Customer Experience</li>
        </ul>
      </li>
      <li>Self-driving Vehicles:
        <ul>
          <li>Pedestrian detection</li>
          <li>Trees,cars,etc detection</li>
          <li>Lane detection</li>
        </ul>
      </li>
    </ul>
  </div>

  <div>
   <iframe width="350" height="200" src="https://www.youtube.com/embed/lEWFmKI5RYY?si=bsUWXxiUOfh4KId3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
   <br/>
   <iframe width="350" height="200" src="https://www.youtube.com/embed/3B8369neIHI?si=dpDsaq8x1yyDsv41" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  </div>

</div>

---
transition: slide-left
---
# Facial Recognition Use Cases

* Facial Authentication
  * Buildings
  * Phones
* Criminal detection
  * Airports
  * Stores

<div grid="~ cols-2 gap-2" m="t-2">

  <img border="rounded" src="/assets/airport.jpg" alt="">

  <iframe width="450" height="250" src="https://www.youtube.com/embed/SnH5qe8_rps?si=ym6M0GQGbs73GCzK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

</div>


---
transition: slide-left
---
# How does AI/CV work?
<br/>
<br/>
<br/>
<br/>
<br/>
<center>
```mermaid {theme: 'default',scale: 1, alt: 'A simple sequence diagram'}
flowchart LR
    data["Data Collection"]
    model["Model Creation"]
    inference["Inferencing Application"]
    data --> Annotation --> Training --> model --> inference   
```
</center>
---
layout: center
class: text-center
---

# Learn More

[Documentations](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/showcases.html)
