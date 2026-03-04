---
layout: home
---

<head>
  <link rel="icon" type="image/png" href="assets/RFC_icon.png">
  <link href="https://fonts.googleapis.com/css2?family=Notable&display=swap" rel="stylesheet">
</head>

<style>
  :root {
    --rfc-red: #CC0403;
    --rfc-blue: #053D5A;
    --rfc-tan: #FFF3DC;
    --rfc-gold: #CC8917;
  }

  /* GLOBAL SCALING */
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

  /* KILL DEFAULT HEADERS */
  header.site-header, .site-title, #header, .header-site { display: none !important; }

  /* 1. NAVIGATION & HAMBURGER */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 5rem;
    background: rgba(255, 243, 220, 0.95);
    backdrop-filter: blur(15px);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 0.2rem solid var(--rfc-gold);
    box-sizing: border-box;
  }

  .nav-logo-img { height: 3.5rem; width: auto; }

  /* Desktop Links */
  .nav-links { display: flex; gap: 1rem; align-items: center; }
  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; 
    font-size: 0.8rem; text-transform: uppercase; letter-spacing: 1px;
    padding: 0.6rem 1rem; transition: 0.3s;
  }

  /* Mobile Sidebar Toggle (The "Lined" Sidebar Icon) */
  .menu-toggle {
    display: none;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
    z-index: 10001;
  }
  .menu-toggle span {
    width: 30px; height: 3px;
    background: var(--rfc-blue);
    border-radius: 10px;
    transition: 0.3s;
  }

  /* 2. HERO SECTION */
  .hero-container { position: relative; width: 100%; height: 100vh; overflow: hidden; }
  .hero-banner-bg {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: url('assets/BANNER.png') no-repeat center center;
    background-size: cover;
    filter: blur(3px) brightness(0.6);
    z-index: 1; transition: filter 0.6s ease-out;
  }
  .blurred-more { filter: blur(18px) brightness(0.3) !important; }

  .hero-content-layer {
    position: fixed; top: 0; left: 0; width: 100%; height: 100vh;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    z-index: 5; color: white; text-align: center;
  }

  .animated-logo { width: 10rem; margin-bottom: 3rem; }

  .hero-title { 
    font-family: 'Notable', sans-serif;
    font-size: 11vw; font-weight: 900; font-style: italic; line-height: 1; 
    margin: 0; text-transform: uppercase; width: 98vw; white-space: nowrap;
    text-shadow: 0 1rem 4rem rgba(0,0,0,0.8); color: var(--rfc-tan);
  }

  .hero-subtitle {
    font-size: 2vw; font-weight: 800; text-transform: uppercase;
    letter-spacing: 2.5vw; margin-top: 1.5rem; padding-left: 2.5vw; color: var(--rfc-gold);
  }

  /* 3. MAIN CONTENT */
  .main-wrapper {
    background: var(--rfc-tan);
    position: relative; z-index: 100; margin-top: 100vh;
    border-radius: 4rem 4rem 0 0; padding: 5rem 8%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6);
  }

  .achievement-panel {
    background: white; padding: 4rem; border-radius: 2rem;
    display: flex; align-items: center; justify-content: space-around;
    flex-wrap: wrap; margin-bottom: 5rem; border: 0.5rem solid var(--rfc-red);
    gap: 2rem;
  }

  .bar-logo { height: 11rem; width: auto; }

  /* MOBILE RESPONSIVENESS */
  @media (max-width: 768px) {
    .menu-toggle { display: flex; }
    
    .nav-links {
      position: fixed; top: 0; right: -100%; width: 70%; height: 100vh;
      background: var(--rfc-tan); flex-direction: column; 
      justify-content: center; transition: 0.5s; z-index: 10000;
      box-shadow: -10px 0 30px rgba(0,0,0,0.2);
    }

    .nav-links.active { right: 0; }

    .hero-title { font-size: 12vw; white-space: normal; width: 90vw; }
    .hero-subtitle { font-size: 4vw; letter-spacing: 1vw; }
    .bar-logo { height: 8rem; }
    .achievement-panel { padding: 2rem; text-align: center; }
  }

  .discord-fab {
    position: fixed; bottom: 2rem; right: 2rem; 
    background: #5865F2; width: 4.5rem; height: 4.5rem; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 1rem 2rem rgba(0,0,0,0.3); z-index: 99999;
  }
  .discord-fab img { width: 100%; height: 100%; border-radius: 50%; }

</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" class="nav-logo-img" alt="RFC Logo"></a>
  
  <div class="menu-toggle" id="mobile-menu">
    <span></span>
    <span></span>
    <span></span>
  </div>

  <div class="nav-links" id="nav-list">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/officer-team" class="nav-item">Officers</a>
    <a href="/calendar" class="nav-item">Calendar</a>
    <a href="/join" class="nav-item" style="background: var(--rfc-red); color: white; border-radius: 4px;">Join Us</a>
  </div>
</nav>

<a href="https://discord.gg/rXG86ZeBwj" class="discord-fab" target="_blank">
  <img src="assets/discord-logo-icon-editorial-free-vector.jpg" alt="Discord">
</a>

<div class="hero-banner-bg" id="heroBg"></div>
<div class="hero-content-layer">
  <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" class="animated-logo" alt="RFC Logo">
  <h1 class="hero-title">YOUR JOURNEY STARTS HERE</h1>
  <p class="hero-subtitle">RPI FLYING CLUB</p>
</div>

<div class="main-wrapper">
  <div class="achievement-panel">
    <div style="max-width: 30rem;">
      <h2 style="font-family: 'Notable', sans-serif; color: var(--rfc-blue); font-size: 2.2rem; margin: 0;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.1rem; margin-top: 1rem; color: var(--rfc-blue);">Winner of the RPI Brand Competition. Designed to reflect the speed and precision of aviation.</p>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-BG-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <div style="text-align: center; margin: 5rem 0;">
    <h2 style="font-family: 'Notable', sans-serif; font-size: 2.5rem; color: var(--rfc-blue);">Advancing Aviation at RPI</h2>
    <p style="color: #444; font-size: 1.2rem; max-width: 50rem; margin: 2rem auto; line-height: 1.6;">
      Students, Pilots, Engineers, Nerds. We are the community for all aviation enthusiasts at Rensselaer.
    </p>
  </div>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr)); gap: 1.5rem;">
    <img src="assets/event1.jpg" style="width:100%; height:25rem; object-fit:cover; border-radius:1.5rem;" alt="Event 1">
    <img src="assets/event2.jpg" style="width:100%; height:25rem; object-fit:cover; border-radius:1.5rem;" alt="Event 2">
    <img src="assets/event3.jpg" style="width:100%; height:25rem; object-fit:cover; border-radius:1.5rem;" alt="Event 3">
  </div>

  <footer style="text-align: center; padding-top: 6rem; margin-top: 6rem; border-top: 2px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="assets/RFCLOGO.png" style="height: 5rem; opacity: 0.9; margin-bottom: 1.5rem;" alt="RFC Logo">
    <p>© 2025 RPI Flying Club. All rights reserved.</p>
  </footer>
</div>

<script>
  // Dynamic Blur Logic
  window.onscroll = function() {
    var bg = document.getElementById("heroBg");
    if (document.documentElement.scrollTop > 60) {
      bg.classList.add("blurred-more");
    } else {
      bg.classList.remove("blurred-more");
    }
  };

  // Mobile Menu Logic
  const menuToggle = document.getElementById('mobile-menu');
  const navList = document.getElementById('nav-list');

  menuToggle.addEventListener('click', () => {
    navList.classList.toggle('active');
  });
</script>