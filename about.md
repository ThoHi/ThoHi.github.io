---
layout: page
title: About
permalink: /about/
---

# About Me

Hello! I'm ThoHi, a technology enthusiast and data scientist. I'm passionate about using technology to solve real-world problems and create meaningful impact.

## Skills

- Data Science & Analysis
- Web Development
- GIS & Mapping
- Programming (Python, JavaScript, R)

## Certifications

<div class="certificate-slider">
  <div class="slider-container">
    <div class="slider">
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/NASA ML.png" alt="NASA Machine Learning Certificate">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/NASA SAR.png" alt="NASA SAR Certificate">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/GIS for Climate Action.png" alt="GIS for Climate Action">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/Spatial Analysis.png" alt="Spatial Analysis Certificate">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/Cartography.png" alt="Cartography Certificate">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/ESRI Geo apps.png" alt="ESRI Geo Apps Certificate">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/NASA methane.png" alt="NASA Methane Certificate">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/ArcGIS Lab.png" alt="ArcGIS Lab Certificate">
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="certificate-box">
          <div class="image-container">
            <img src="/assets/images/certificates/NASA Waterborne Disease Risk.png" alt="NASA Waterborne Disease Risk">
          </div>
        </div>
      </div>
    </div>
    <button class="slider-nav prev" onclick="moveSlide(-1)">❮</button>
    <button class="slider-nav next" onclick="moveSlide(1)">❯</button>
  </div>
  <div class="slider-dots"></div>
</div>

<style>
.certificate-slider {
  max-width: 900px;
  margin: 40px auto;
  padding: 20px;
  background: transparent;
  border-radius: 8px;
}

.slider-container {
  position: relative;
  overflow: hidden;
  border-radius: 0;
  background: transparent;
  height: 500px;
  width: 100%;
}

.slider {
  display: flex;
  transition: transform 0.5s ease-in-out;
  height: 100%;
  width: 100%;
  position: relative;
}

.slide {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

.slide.active {
  opacity: 1;
}

.certificate-box {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px;
}

.image-container {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.slide img {
  max-width: 100%;
  max-height: 100%;
  width: auto;
  height: auto;
  object-fit: contain;
}

.slider-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(52, 152, 219, 0.9);
  color: white;
  border: none;
  width: 40px;
  height: 40px;
  cursor: pointer;
  font-size: 20px;
  border-radius: 50%;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
}

.prev {
  left: 10px;
}

.next {
  right: 10px;
}

@media (max-width: 768px) {
  .slider-container {
    height: 400px;
  }
}
</style>

<script>
let currentSlide = 0;
const slides = document.querySelectorAll('.slide');
const dots = document.querySelector('.slider-dots');

// Create dots
slides.forEach((_, index) => {
  const dot = document.createElement('span');
  dot.className = 'dot';
  if (index === 0) dot.classList.add('active');
  dot.onclick = () => showSlide(index);
  dots.appendChild(dot);
});

function moveSlide(n) {
  showSlide(currentSlide + n);
}

function showSlide(n) {
  const slider = document.querySelector('.slider');
  const dots = document.querySelectorAll('.dot');
  const slides = document.querySelectorAll('.slide');
  
  if (n >= slides.length) n = 0;
  if (n < 0) n = slides.length - 1;
  
  // Remove active class from all slides
  slides.forEach(slide => {
    slide.style.opacity = '0';
    slide.style.position = 'absolute';
  });
  
  // Show current slide
  slides[n].style.opacity = '1';
  slides[n].style.position = 'relative';
  
  currentSlide = n;
  
  dots.forEach((dot, index) => {
    dot.classList.toggle('active', index === currentSlide);
  });
}

// Initialize first slide
showSlide(0);
</script>

## Projects

I work on various projects, with a particular focus on:

- Data visualization
- Interactive web applications
- Geospatial analysis
- Open source contributions

## Contact

Feel free to reach out to me:

- Email: [{{ site.author.email }}](mailto:{{ site.author.email }})
- GitHub: [@{{ site.github_username }}](https://github.com/{{ site.github_username }})

I'm always interested in collaborating on interesting projects and discussing new ideas. 