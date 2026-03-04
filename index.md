---
layout: home
---

<head>
  <link rel="icon" type="image/png" href="assets/RFC_icon.png">
  <link href="https://fonts.googleapis.com/css2?family=Notable&display=swap" rel="stylesheet">
</head>

<style>
  @font-face {
    font-family: 'Loubag';
    src: url('assets/loubag.ttf') format('truetype');
  }
  @font-face {
    font-family: 'Loubag-SemiBold';
    src: url('assets/loubag-semi-bold.ttf') format('truetype');
  }

  :root {
    --rfc-red: #CC0403;
    --rfc-blue: #053D5A;
    --rfc-tan: #FFF3DC;
    --rfc-gold: #CC8917;
  }

  html { font-size: 16px; }
  @media (max-width: 768px) { html { font-size: 14px; } }

  body { 
    margin: 0; padding: 0;
    font-family: 'Loubag', sans-serif;
    background: url('assets/bannerbackground.png') no-repeat center center fixed;
    background-size: cover;
    background-color: var(--rfc-blue);
    overflow-x: hidden;
  }

  header.site-header, .site-title, #header, .header-site { display: none !important; }

  /* 1. NAVIGATION */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 7rem; /* Increased height for the thin logo */
    background: #FFF3DC; 
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 0.25rem solid var(--rfc-gold);
    box-sizing: border-box;
  }

  /* NEW THIN LOGO - BIGGER */
  .nav-logo-img { 
    height: 6rem; /* Now much larger thanks to the thin aspect ratio */
    width: auto; 
    mix-blend-mode: darken; 
    transition: transform 0.3s ease;
  }
  .nav-logo-img:hover { transform: scale(1.02); }

  .nav-links { display: flex; gap: 1rem; align-items: center; }
  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; 
    font-size: 0.95rem; text-transform: uppercase; letter-spacing: 1px;
    padding: 0.6rem 1rem; transition: 0.3s;
  }
  .nav-item:hover { color: var(--rfc-red); }

  .menu-toggle { display: none; flex-direction: column; gap: 6px; cursor: pointer; z-index: 10001; }
  .menu-toggle span { width: 35px; height: 3px; background: var(--rfc-blue); border-radius: 10px; }

  /* 2. HERO SECTION */
  .hero-content-layer {
    position: fixed; top: 0; left: 0; width: 100%; height: 100vh;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    z-index: 5; color: white; text-align: center;
  }

  .animated-logo { width: 11rem; margin-bottom: 4rem; opacity: 0.75; }

  .hero-title { 
    font-family: 'Notable', sans-serif;
    font-size: 11.2vw; font-weight: 900; font-style: italic; line-height: 1; 
    margin: 0; text-transform: uppercase; width: 98vw; white-space: nowrap;
    text-shadow: 0 1rem 4rem rgba(0,0,0,0.8); color: var(--rfc-tan);
  }

  .hero-subtitle {
    font-family: 'Loubag-SemiBold', sans-serif;
    font-weight: 900; font-size: 2.8vw; text-transform: uppercase;
    letter-spacing: 2.4vw; margin-top: 1.8rem; padding-left: 2.4vw; color: var(--rfc-gold);
    text-shadow: 0 0.5rem 1.5rem rgba(0,0,0,0.5);
  }

  /* 3. MAIN CONTENT */
  .main-wrapper {
    background: var(--rfc-tan);
    position: relative; z-index: 100; margin-top: 100vh;
    border-radius: 4rem 4rem 0 0; padding: 6rem 8%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6);
  }

  .section-title {
    font-family: 'Notable', sans-serif;
    font-size: clamp(2.2rem, 5vw, 3.8rem);
    color: var(--rfc-blue);
    text-align: center;
    margin-bottom: 3rem;
  }

  /* 4. SOCIAL BUTTONS (Discord & Instagram) */
  .social-stack {
    position: fixed; bottom: 2.5rem; right: 2.5rem; 
    display: flex; flex-direction: column; gap: 1rem; z-index: 99999;
  }

  .social-fab {
    width: 4.5rem; height: 4.5rem; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 0.5rem 1.5rem rgba(0,0,0,0.3);
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    background: white; overflow: hidden;
  }
  .social-fab:hover { transform: scale(1.15) translateY(-5px); box-shadow: 0 1rem 2rem rgba(0,0,0,0.4); }
  .social-fab img { width: 100%; height: 100%; object-fit: cover; }

  /* Mobile Responsive */
  @media (max-width: 992px) {
    .menu-toggle { display: flex; }
    .nav-links {
      position: fixed; top: 0; right: -100%; width: 70%; height: 100vh;
      background: var(--rfc-tan); flex-direction: column; 
      justify-content: center; transition: 0.5s; z-index: 10000;
    }
    .nav-links.active { right: 0; }
  }

</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGOthin.png" class="nav-logo-img" alt="RFC Logo"></a>
  
  <div class="menu-toggle" id="mobile-menu">
    <span></span><span></span><span></span>
  </div>

  <div class="nav-links" id="nav-list">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/officer-team" class="nav-item">Officers</a>
    <a href="/calendar" class="nav-item">Calendar</a>
    <a href="/join" class="nav-item" style="background: var(--rfc-red); color: white; border-radius: 4px;">Join Us</a>
  </div>
</nav>

<div class="social-stack">
  <a href="https://www.instagram.com/rpiflyingclub/" class="social-fab" target="_blank">
    <img src="assets/Instagram_logo_2016.png" alt="Instagram">
  </a>
  <a href="https://discord.gg/rXG86ZeBwj" class="social-fab" target="_blank">
    <img src="assets/discord-logo-icon-editorial-free-vector.jpg" alt="Discord">
  </a>
</div>

<div class="hero-banner-bg" id="heroBg"></div>
<div class="hero-content-layer">
  <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" class="animated-logo" alt="RFC Logo">
  <h1 class="hero-title">YOUR JOURNEY STARTS HERE</h1>
  <p class="hero-subtitle">RPI FLYING CLUB</p>
</div>

<div class="main-wrapper">
  
  <div class="advancing-panel">
    <h2 class="section-title">Advancing Aviation at RPI</h2>
    <p>
      Students, Pilots, Engineers, Nerds. We are the community for all aviation enthusiasts at Rensselaer. We provide the resources, networking, and environment to jumpstart your aviation journey.
    </p>
  </div>

  <div class="achievement-panel">
    <div class="achievement-text">
      <h2 style="font-family: 'Notable', sans-serif; color: var(--rfc-blue); font-size: 2.8rem; margin: 0; line-height: 1.1;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.3rem; margin-top: 1.5rem; color: var(--rfc-blue); line-height: 1.5;">Winner of the RPI Brand Competition. Designed to reflect the speed and precision of aviation. Our identity is built to represent the future of flight on campus.</p>
      <p style="font-size: 0.9rem; color: #666; font-style: italic; margin-top: 1rem;">Brand design by Kaden Tennent '25</p>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-BG-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <h2 class="section-title">Life at RFC</h2>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr)); gap: 2rem;">
    <img src="assets/event1.jpg" style="width:100%; height:30rem; object-fit:cover; border-radius:2rem;" alt="Event 1">
    <img src="assets/event2.jpg" style="width:100%; height:30rem; object-fit:cover; border-radius:2rem;" alt="Event 2">
    <img src="assets/event3.jpg" style="width:100%; height:30rem; object-fit:cover; border-radius:2rem;" alt="Event 3">
    <img src="assets/event4.jpg" style="width:100%; height:30rem; object-fit:cover; border-radius:2rem;" alt="Event 4">
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="assets/RFCLOGOthin.png" style="height: 6rem; opacity: 0.9; margin-bottom: 2rem; mix-blend-mode: darken;" alt="RFC Logo">
    <p>© 2026 RPI Flying Club. All rights reserved.</p>
  </footer>
</div>

<script>
  window.onscroll = function() {
    var bg = document.getElementById("heroBg");
    if (document.documentElement.scrollTop > 60) {
      bg.classList.add("blurred-more");
    } else {
      bg.classList.remove("blurred-more");
    }
  };

  const menuToggle = document.getElementById('mobile-menu');
  const navList = document.getElementById('nav-list');
  menuToggle.addEventListener('click', () => {
    navList.classList.toggle('active');
  });
</script>
