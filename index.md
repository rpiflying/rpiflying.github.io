---
layout: home
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&display=swap');

  body { font-family: 'Inter', sans-serif; color: #333; line-height: 1.6; }
  
  /* Theme Overrides */
  #header { background: #ffffff; border-bottom: 1px solid #eee; padding: 20px 0; }
  #header h1 { color: #D6001C !important; font-weight: 700; letter-spacing: -1px; }
  
  .banner-container { width: 100%; margin-bottom: 40px; }
  .banner-img { width: 100%; border-radius: 4px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
  
  .btn-join { 
    background-color: #D6001C; 
    color: white !important; 
    padding: 12px 30px; 
    text-decoration: none; 
    border-radius: 2px; 
    font-weight: 600; 
    display: inline-block;
    transition: opacity 0.2s;
  }
  .btn-join:hover { opacity: 0.8; }

  /* Sections */
  .section-title { text-align: center; font-weight: 700; color: #111; margin-top: 50px; }
  .grid-container { 
    display: grid; 
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
    gap: 20px; 
    margin: 40px 0; 
  }
  
  .card { border: 1px solid #eee; padding: 20px; border-radius: 8px; background: #fafafa; }
  .benefit-list { list-style: none; padding: 0; }
  .benefit-list li::before { content: "✓ "; color: #D6001C; font-weight: bold; }

  .officer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 15px;
    text-align: center;
    margin-top: 30px;
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
  [cite_start]<div><span class="officer-name">Andreas</span><span class="officer-title">President</span></div> [cite: 58]
  [cite_start]<div><span class="officer-name">Jordan</span><span class="officer-title">Vice President</span></div> [cite: 61, 62]
  [cite_start]<div><span class="officer-name">Shane</span><span class="officer-title">Treasurer</span></div> [cite: 63]
  [cite_start]<div><span class="officer-name">Stella</span><span class="officer-title">Secretary</span></div> [cite: 69]
  [cite_start]<div><span class="officer-name">Matthew</span><span class="officer-title">Flight Safety</span></div> [cite: 59, 60]
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
