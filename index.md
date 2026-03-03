---
layout: home
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&display=swap');

  body { 
    font-family: 'Inter', sans-serif; 
    color: #333; 
    line-height: 1.6; 
    /* Fade in the whole page on load */
    animation: fadeInPage 0.8s ease-in;
  }

  @keyframes fadeInPage {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Dynamic Join Button */
  .btn-join { 
    background-color: #D6001C; 
    color: white !important; 
    padding: 14px 35px; 
    text-decoration: none; 
    border-radius: 4px; 
    font-weight: 700; 
    display: inline-block;
    transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275); /* Bouncy effect */
    box-shadow: 0 4px 15px rgba(214, 0, 28, 0.3);
  }

  .btn-join:hover { 
    transform: scale(1.05); 
    box-shadow: 0 8px 25px rgba(214, 0, 28, 0.4);
    background-color: #ff0022;
  }

  /* Interactive Cards (Benefits & Career) */
  .card { 
    border: 1px solid #eee; 
    padding: 25px; 
    border-radius: 12px; 
    background: #ffffff; 
    transition: all 0.3s ease;
  }

  .card:hover {
    transform: translateY(-10px); /* Lift up effect */
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    border-color: #D6001C;
  }

  /* Image Gallery Hover */
  .gallery-img { 
    width: 100%; 
    height: 250px; 
    object-fit: cover; 
    border-radius: 8px;
    transition: all 0.5s ease;
    filter: brightness(0.9);
  }

  .gallery-img:hover { 
    filter: brightness(1.1);
    transform: scale(1.02);
    cursor: pointer;
  }

  /* Officer Grid Interaction */
  .officer-item {
    padding: 10px;
    transition: transform 0.2s;
  }
  
  .officer-item:hover {
    transform: scale(1.1);
  }

  .officer-name { font-weight: 700; display: block; color: #D6001C; }
  .officer-title { font-size: 0.85em; text-transform: uppercase; color: #666; }
</style>

<div class="banner-container">
  <img src="assets/BANNER.png" class="banner-img" alt="RPI Flying Club">
</div>

<div style="text-align: center; max-width: 800px; margin: 0 auto;">
  <h1 style="font-weight: 700; color: #111;">Your Journey Starts Here</h1>
  <p style="font-size: 1.1em; color: #666;">
    Pilot? Planespotter? Aviation enthusiast? [cite: 8, 9] We are the club for you. [cite: 13, 15] 
    Advancing aviation at Rensselaer by making flight accessible to everyone.
  </p>
  <a href="/join" class="btn-join">Become a Member Today</a>
</div>

<h2 class="section-title">Member Benefits</h2>
<div class="grid-container">
  <div class="card">
    <h3 style="color: #D6001C;">$30 / Semester</h3>
    <p>Or save with $50 for the full year! [cite: 19, 21, 22]</p>
    <ul class="benefit-list">
      <li>Access to all club meetings, trips, & events [cite: 24, 25]</li>
      <li>Discounted trip fees [cite: 26]</li>
      <li>Free food & snacks at Social Nights [cite: 28, 29]</li>
      <li>Complimentary RFC stickers (Coming Soon) [cite: 31, 32]</li>
    </ul>
  </div>
  <div class="card">
    <h3 style="color: #D6001C;">Career & Connections</h3>
    <p>Gain access to alumni at top companies: [cite: 38, 39]</p>
    <div style="font-weight: 700; opacity: 0.7;">
      BOEING | DELTA | LOCKHEED MARTIN | PRATT & WHITNEY 
    </div>
  </div>
</div>

<h2 class="section-title">Our Leadership</h2>
<div class="officer-grid">
  <div class="officer-item"><span class="officer-name">Andreas</span><span class="officer-title">President</span></div>
  <div class="officer-item"><span class="officer-name">Jordan</span><span class="officer-title">Vice President</span></div>
  <div class="officer-item"><span class="officer-name">Shane</span><span class="officer-title">Treasurer</span></div>
  <div class="officer-item"><span class="officer-name">Stella</span><span class="officer-title">Secretary</span></div>
  <div class="officer-item"><span class="officer-name">Matthew</span><span class="officer-title">Flight Safety</span></div>
</div>

<h2 class="section-title">Gallery</h2>
<div class="grid-container">
  <img src="assets/20240915_141521.jpg" style="width:100%; height:250px; object-fit:cover; border-radius:4px;" alt="Aviation 1">
  <img src="assets/20241027_1202123.jpg" style="width:100%; height:250px; object-fit:cover; border-radius:4px;" alt="Aviation 2">
  <img src="assets/pic3.jpg" style="width:100%; height:250px; object-fit:cover; border-radius:4px;" alt="Aviation 3">
</div>

<hr>

<div style="text-align: center; color: #666; font-size: 0.9em; padding-bottom: 40px;">
  <p>Location: Rensselaer Union, Troy, NY | [cite_start]<a href="mailto:rpiflying@gmail.com">rpiflying@gmail.com</a></p> [cite: 44]
  <p>© 2026 RPI Flying Club. [cite_start]All rights reserved.</p> [cite: 66, 67]
</div>
