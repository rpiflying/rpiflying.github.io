---
layout: home
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&display=swap');

  :root {
    --rpi-red: #D6001C;
    --sidebar-width: 250px;
  }

  body { 
    font-family: 'Inter', sans-serif; 
    color: #333; 
    margin: 0;
    background-color: #fff; /* Solid background for the bottom */
  }

  /* 1. The Blurred Background Hero */
  .hero-section {
    position: relative;
    height: 60vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .hero-bg {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background-image: url('assets/BANNER.png');
    background-attachment: fixed; /* This keeps it from moving */
    background-position: center;
    background-size: cover;
    filter: blur(4px) brightness(0.7); /* Subtle blur and darken for text readability */
    transform: scale(1.1); /* Prevents white edges from the blur */
    z-index: -1;
  }

  .hero-text {
    text-align: center;
    color: white;
    z-index: 1;
    padding: 20px;
  }

  /* 2. Sidebar Navigation */
  .sidebar {
    width: var(--sidebar-width);
    height: 100vh;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    border-right: 1px solid #eee;
    position: fixed;
    padding: 40px 20px;
    z-index: 1000;
  }

  .sidebar-link {
    display: block;
    text-decoration: none;
    color: #555;
    font-weight: 600;
    padding: 12px 15px;
    margin-bottom: 5px;
    border-radius: 8px;
    transition: 0.3s;
  }

  .sidebar-link:hover {
    background: var(--rpi-red);
    color: white !important;
  }

  /* 3. Main Content (The "Solid" Part) */
  .main-content {
    margin-left: var(--sidebar-width);
    background: white; /* This ensures it stays solid while scrolling */
    position: relative;
    box-shadow: 0 -20px 40px rgba(0,0,0,0.1);
  }

  .content-wrapper {
    max-width: 900px;
    margin: 0 auto;
    padding: 60px 40px;
  }

  /* 4. Interactive Elements */
  .btn-join { 
    background-color: var(--rpi-red); 
    color: white !important; 
    padding: 15px 40px; 
    text-decoration: none; 
    border-radius: 50px; 
    font-weight: 700; 
    display: inline-block;
    transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    box-shadow: 0 10px 20px rgba(214, 0, 28, 0.3);
  }

  .btn-join:hover { transform: scale(1.05) translateY(-3px); }

  .card { 
    border: 1px solid #f0f0f0; 
    padding: 30px; 
    border-radius: 16px; 
    background: #fff; 
    transition: 0.4s; 
    margin-bottom: 20px;
  }
  .card:hover { transform: translateY(-10px); box-shadow: 0 20px 40px rgba(0,0,0,0.05); }

  /* Responsive Fixes */
  @media (max-width: 768px) {
    .sidebar { width: 100%; height: auto; position: relative; display: flex; flex-wrap: wrap; justify-content: center; }
    .main-content { margin-left: 0; }
  }
</style>

<nav class="sidebar">
  <div style="font-weight: 800; color: #D6001C; margin-bottom: 30px; font-size: 1.3em; letter-spacing: -1px;">RPI FLYING CLUB</div>
  <a href="/" class="sidebar-link">Home</a>
  <a href="/join" class="sidebar-link">Join Now</a>
  <a href="#benefits" class="sidebar-link">Benefits</a>
  <a href="#leadership" class="sidebar-link">Leadership</a>
  <a href="mailto:rpiflying@gmail.com" class="sidebar-link">Contact</a>
</nav>

<main class="main-content">
  <section class="hero-section">
    <div class="hero-bg"></div>
    <div class="hero-text">
      <h1 style="font-size: 3.5em; font-weight: 800; margin-bottom: 10px;">Your Journey Starts Here</h1>
      <p style="font-size: 1.4em; font-weight: 300; opacity: 0.9;">Advancing Aviation at Rensselaer</p>
    </div>
  </section>

  <div class="content-wrapper">
    <div style="text-align: center; margin-bottom: 80px;">
      <h2 style="font-size: 2em; color: #111;">Pilot? Planespotter? Aviation enthusiast?</h2>
      <p style="color: #666; font-size: 1.1em; max-width: 600px; margin: 20px auto;">
        We are the club for you. We provide the resources, community, and connections to help you take to the skies.
      </p>
      <br>
      <a href="/join" class="btn-join">Get On The Flight List</a>
    </div>

  <div id="benefits" style="display: grid; grid-template-columns: 1fr 1fr; gap: 30px;">
      <div class="card">
        <h3 style="color: var(--rpi-red);">Membership</h3>
        <p><strong>$30 / Semester</strong> or <strong>$50 / Year</strong></p>
        <ul style="padding-left: 20px; color: #555;">
          <li>Access to all club meetings & trips</li>
          <li>Discounted paid trip fees</li>
          <li>Free food & drinks at Social Nights</li>
          <li>Exclusive club merchandise</li>
        </ul>
      </div>
      <div class="card">
        <h3 style="color: var(--rpi-red);">Career Growth</h3>
        <p>Connect with alumni at industry leaders:</p>
        <div style="font-weight: 700; color: #333; margin-top: 15px; display: flex; flex-wrap: wrap; gap: 10px;">
          <span>BOEING</span> | <span>DELTA</span> | <span>LOCKHEED</span> | <span>PRATT & WHITNEY</span>
        </div>
      </div>
    </div>

  <h2 id="leadership" style="margin-top: 80px; text-align: center;">Our Leadership</h2>
    <div style="display: flex; justify-content: space-around; flex-wrap: wrap; gap: 20px; margin-top: 40px;">
      <div style="text-align: center;"><strong style="color: var(--rpi-red);">Andreas</strong><br><small>President</small></div>
      <div style="text-align: center;"><strong style="color: var(--rpi-red);">Jordan</strong><br><small>Vice President</small></div>
      <div style="text-align: center;"><strong style="color: var(--rpi-red);">Shane</strong><br><small>Treasurer</small></div>
      <div style="text-align: center;"><strong style="color: var(--rpi-red);">Stella</strong><br><small>Secretary</small></div>
      <div style="text-align: center;"><strong style="color: var(--rpi-red);">Matthew</strong><br><small>Safety Officer</small></div>
    </div>

  <hr style="margin: 80px 0; border: 0; border-top: 1px solid #eee;">
    
  <div style="text-align: center; color: #aaa; font-size: 0.9em;">
      <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com</p>
      <p>© 2026 RPI Flying Club</p>
    </div>
  </div>
</main>
