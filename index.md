---
layout: home
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&display=swap');

  /* 1. Global Reset & Layout */
  :root {
    --rpi-red: #D6001C;
    --sidebar-width: 250px;
  }

  body { 
    font-family: 'Inter', sans-serif; 
    color: #333; 
    line-height: 1.6; 
    margin: 0;
    animation: fadeInPage 0.8s ease-in;
    display: flex; /* Flexbox for Sidebar + Main Content */
  }

  @keyframes fadeInPage {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  /* 2. Responsive Sidebar */
  .sidebar {
    width: var(--sidebar-width);
    height: 100vh;
    background: #f8f9fa;
    border-right: 1px solid #eee;
    position: fixed;
    padding: 40px 20px;
    display: flex;
    flex-direction: column;
    gap: 15px;
    z-index: 1000;
  }

  .sidebar-link {
    text-decoration: none;
    color: #555;
    font-weight: 600;
    padding: 10px 15px;
    border-radius: 8px;
    transition: all 0.2s;
  }

  .sidebar-link:hover {
    background: var(--rpi-red);
    color: white !important;
    transform: translateX(5px);
  }

  /* 3. Main Content Area */
  .main-content {
    margin-left: var(--sidebar-width); /* Push content past sidebar */
    width: calc(100% - var(--sidebar-width));
    min-height: 100vh;
  }

  /* 4. Full-Width Banner Strategy */
  .banner-container {
    width: 100%;
    overflow: hidden;
    line-height: 0;
  }

  .banner-img {
    width: 100%;
    height: auto;
    object-fit: cover;
    max-height: 500px; /* Limits height on ultra-wide screens */
  }

  /* 5. Typography & Buttons */
  .content-wrapper {
    max-width: 1000px;
    margin: 0 auto;
    padding: 40px 20px;
  }

  .btn-join { 
    background-color: var(--rpi-red); 
    color: white !important; 
    padding: 14px 35px; 
    text-decoration: none; 
    border-radius: 4px; 
    font-weight: 700; 
    display: inline-block;
    transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    box-shadow: 0 4px 15px rgba(214, 0, 28, 0.3);
  }

  .btn-join:hover { 
    transform: scale(1.05); 
    box-shadow: 0 8px 25px rgba(214, 0, 28, 0.4);
  }

  /* 6. Mobile Responsiveness */
  @media (max-width: 768px) {
    body { flex-direction: column; }
    .sidebar { 
      width: 100%; 
      height: auto; 
      position: relative; 
      flex-direction: row; 
      flex-wrap: wrap;
      padding: 15px;
      justify-content: center;
    }
    .main-content { margin-left: 0; width: 100%; }
    .sidebar-link { font-size: 0.8em; padding: 5px 10px; }
  }

  /* Grid Styling */
  .grid-container { 
    display: grid; 
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
    gap: 20px; 
    margin: 40px 0; 
  }
  .card { border: 1px solid #eee; padding: 25px; border-radius: 12px; background: #fff; transition: 0.3s; }
  .card:hover { transform: translateY(-10px); box-shadow: 0 20px 40px rgba(0,0,0,0.1); }
  
  .officer-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 10px; margin-top: 20px; }
  .officer-item { text-align: center; transition: 0.2s; }
  .officer-item:hover { transform: scale(1.1); }
  .officer-name { font-weight: 700; display: block; color: var(--rpi-red); }
  .officer-title { font-size: 0.8em; color: #666; }
</style>

<nav class="sidebar">
  <div style="font-weight: 800; color: #D6001C; margin-bottom: 20px; font-size: 1.2em;">RPI FLYING CLUB</div>
  <a href="/" class="sidebar-link">Home</a>
  <a href="/join" class="sidebar-link">Join Now</a>
  <a href="#calendar" class="sidebar-link">Calendar</a>
  <a href="#leadership" class="sidebar-link">Officer Team</a>
  <a href="#gallery" class="sidebar-link">Gallery</a>
  [cite_start]<a href="mailto:rpiflying@gmail.com" class="sidebar-link">Contact</a> [cite: 44]
</nav>

<main class="main-content">
  <div class="banner-container">
    <img src="assets/BANNER.png" class="banner-img" alt="RPI Flying Club Banner">
  </div>

  <div class="content-wrapper">
    <div style="text-align: center; margin-bottom: 60px;">
      [cite_start]<h1 style="font-weight: 700; font-size: 2.5em; color: #111;">Your Journey Starts Here</h1> [cite: 1]
      <p style="font-size: 1.2em; color: #666; max-width: 700px; margin: 0 auto 30px;">
        Pilot? Planespotter? [cite_start]Aviation enthusiast? [cite: 8, 9] [cite_start]We are the club for you. [cite: 13, 15] <br>
        Advancing aviation at Rensselaer by making flight accessible to everyone.
      </p>
      <a href="/join" class="btn-join">Get On The Flight List</a>
    </div>

  <h2 id="benefits" style="font-weight: 700;">Member Benefits</h2>
    <div class="grid-container">
      <div class="card">
        [cite_start]<h3 style="color: #D6001C;">Membership</h3> [cite: 46]
        [cite_start]<p><strong>$30 / Semester</strong> [cite: 19][cite_start]<br>Or save $10 with the $50 Annual Plan! [cite: 21, 22]</p>
        <ul style="padding-left: 18px;">
          [cite_start]<li>All club meetings, trips, & events [cite: 24, 25]</li>
          [cite_start]<li>Discounted paid trip fees [cite: 26]</li>
          [cite_start]<li>Free food & drinks at Social Nights [cite: 28, 29]</li>
          [cite_start]<li>Coming Soon: RFC Stickers & Merch [cite: 31, 32, 33]</li>
        </ul>
      </div>
      <div class="card">
        [cite_start]<h3 style="color: #D6001C;">Industry Connections</h3> [cite: 38]
        [cite_start]<p>Gain access to alumni at top-tier aviation companies: [cite: 38, 39]</p>
        <div style="font-weight: 700; color: #444; margin-top: 15px; font-size: 0.9em; letter-spacing: 1px;">
          BOEING | DELTA | LOCKHEED MARTIN | [cite_start]PRATT & WHITNEY [cite: 40, 41, 42, 43]
        </div>
      </div>
    </div>

  <h2 id="leadership" style="font-weight: 700;">Our Leadership</h2>
    <div class="officer-grid">
      [cite_start]<div class="officer-item"><span class="officer-name">Andreas</span><span class="officer-title">President</span></div> [cite: 58]
      [cite_start]<div class="officer-item"><span class="officer-name">Jordan</span><span class="officer-title">Vice President</span></div> [cite: 61, 62]
      [cite_start]<div class="officer-item"><span class="officer-name">Shane</span><span class="officer-title">Treasurer</span></div> [cite: 63]
      [cite_start]<div class="officer-item"><span class="officer-name">Stella</span><span class="officer-title">Secretary</span></div> [cite: 69]
      [cite_start]<div class="officer-item"><span class="officer-name">Matthew</span><span class="officer-title">Flight Safety Officer</span></div> [cite: 59, 60]
    </div>

  <h2 id="gallery" style="font-weight: 700; margin-top: 60px;">Gallery</h2>
    <div class="grid-container">
      <img src="assets/20240915_141521.jpg" style="width:100%; height:250px; object-fit:cover; border-radius:12px;" alt="Aviation 1">
      <img src="assets/20241027_1202123.jpg" style="width:100%; height:250px; object-fit:cover; border-radius:12px;" alt="Aviation 2">
      <img src="assets/pic3.jpg" style="width:100%; height:250px; object-fit:cover; border-radius:12px;" alt="Aviation 3">
    </div>

  <hr style="margin: 60px 0; border: 0; border-top: 1px solid #eee;">

  <div style="text-align: center; color: #999; font-size: 0.85em; padding-bottom: 40px;">
      <p>Rensselaer Union, Troy, NY | [cite_start]rpiflying@gmail.com</p> [cite: 44]<br>
      <p>© 2026 RPI Flying Club. [cite_start]All rights reserved.</p> [cite: 66, 67]
    </div>
  </div>
</main>
