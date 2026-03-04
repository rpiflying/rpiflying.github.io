---
layout: home
---

<head>
  <link rel="icon" type="image/png" href="assets/RFC_icon.png">
  <link href="https://fonts.googleapis.com/css2?family=Notable&display=swap" rel="stylesheet">
</head>

<style>
  /* Base brand colors */
  :root {
    --rfc-red: #CC0403;
    --rfc-blue: #053D5A;
    --rfc-tan: #FFF3DC;
    --rfc-gold: #CC8917;
  }

  /* Loubag font style for body/secondary text */
  body { 
    margin: 0; padding: 0;
    font-family: 'Loubag', sans-serif; /* Ensure Loubag is hosted in your assets */
    background: url('assets/bannerbackground.png') no-repeat center center fixed;
    background-size: cover;
    background-color: var(--rfc-blue);
    color: var(--rfc-blue);
  }

  /* NUCLEAR HEADER REMOVAL */
  header.site-header, .site-title, #header, .header-site, .nav-bar { 
    display: none !important; 
    height: 0 !important;
  }

  /* 1. NAVIGATION */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 85px;
    background: rgba(255, 243, 220, 0.95); /* Light Tan Background */
    backdrop-filter: blur(15px);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 3px solid var(--rfc-gold); /* Gold accent line */
    box-sizing: border-box;
  }

  .nav-logo-img { height: 55px; }
  .nav-links { display: flex; gap: 12px; align-items: center; }
  
  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 0.85rem; 
    text-transform: uppercase; letter-spacing: 1px; padding: 10px 14px; transition: 0.3s;
  }
  .nav-item:hover { color: var(--rfc-red); }

  .nav-btn-join { 
    background: var(--rfc-red); color: white !important; border-radius: 4px;
    border: 2px solid var(--rfc-red);
  }
  .nav-btn-join:hover { background: transparent; color: var(--rfc-red) !important; }

  /* 2. HERO SECTION (LOCKED) */
  .hero-container {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }

  .hero-banner-bg {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: url('assets/BANNER.png') no-repeat center center;
    background-size: cover;
    filter: blur(3px) brightness(0.6); /* Start light unblurred */
    transform: scale(1.05);
    z-index: 1;
    transition: filter 0.6s ease-out;
  }

  .blurred-more { filter: blur(18px) brightness(0.35) !important; }

  .hero-content-layer {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 5;
    color: white;
    text-align: center;
    animation: onLoadFadeUp 1.2s cubic-bezier(0.2, 1, 0.3, 1);
  }

  .animated-logo { 
    width: 160px; 
    margin-bottom: 50px; /* Moved higher */
    filter: drop-shadow(0 0 30px rgba(204, 137, 23, 0.4)); /* Gold Glow */
  }

  .hero-title { 
    font-family: 'Notable', sans-serif;
    font-size: 11.2vw; 
    font-weight: 900; 
    font-style: italic;
    line-height: 1; 
    letter-spacing: -0.05em; 
    margin: 0;
    text-transform: uppercase;
    width: 98vw;
    white-space: nowrap;
    text-shadow: 0 15px 60px rgba(0,0,0,0.9);
    color: var(--rfc-tan);
  }

  .hero-subtitle {
    font-size: 2.2vw;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 2.8vw;
    margin-top: 25px;
    padding-left: 2.8vw;
    color: var(--rfc-gold);
  }

  /* 3. SCROLLABLE CONTENT */
  .main-wrapper {
    background: var(--rfc-tan); /* Light Tan Section */
    position: relative;
    z-index: 100;
    margin-top: 100vh;
    border-radius: 60px 60px 0 0;
    padding: 100px 8%;
    box-shadow: 0 -50px 100px rgba(0,0,0,0.7);
  }

  /* Award Section */
  .achievement-panel {
    background: white;
    padding: 60px;
    border-radius: 30px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    margin-bottom: 80px;
    border: 8px solid var(--rfc-red);
    box-shadow: 0 20px 50px rgba(5, 61, 90, 0.1);
  }

  .bar-logo { height: 180px; }

  h2 { font-family: 'Notable', sans-serif; color: var(--rfc-blue); }

  .discord-fab {
    position: fixed; bottom: 30px; right: 30px; 
    background: #5865F2; width: 70px; height: 70px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 10px 25px rgba(88, 101, 242, 0.4); z-index: 99999;
    overflow: hidden;
  }
  .discord-fab img { width: 100%; height: 100%; object-fit: cover; }

  @keyframes onLoadFadeUp {
    0% { opacity: 0; transform: translateY(60px); }
    100% { opacity: 1; transform: translateY(0); }
  }
</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/officer-team" class="nav-item">Officers</a>
    <a href="/calendar" class="nav-item">Calendar</a>
    <a href="/join" class="nav-item nav-btn-join">Join Us</a>
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
    <div style="max-width: 450px;">
      <h2 style="font-size: 2.5rem; margin: 0;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.2rem; margin-top: 15px; color: var(--rfc-blue);">Winner of the RPI Brand Competition. Designed to reflect the speed and precision of aviation[cite: 58].</p>
      <span style="font-size: 0.8rem; color: #888; font-style: italic;">Logo designed by Kaden Tennent, Ex-President '23-'25</span>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-BG-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <div style="text-align: center; margin: 80px 0;">
    <h2 style="font-size: 3.5rem; letter-spacing: -1px;">Advancing Aviation at RPI</h2>
    <p style="color: #444; font-size: 1.3rem; max-width: 800px; margin: 25px auto;">
      Students, Pilots, Engineers, Nerds. We are the community for all aviation enthusiasts at Rensselaer[cite: 64, 65].
    </p>
  </div>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
    <img src="assets/event1.jpg" style="width:100%; height:450px; object-fit:cover; border-radius:25px;" alt="Event 1">
    <img src="assets/event2.jpg" style="width:100%; height:450px; object-fit:cover; border-radius:25px;" alt="Event 2">
    <img src="assets/event3.jpg" style="width:100%; height:450px; object-fit:cover; border-radius:25px;" alt="Event 3">
  </div>

  <footer style="text-align: center; padding-top: 100px; margin-top: 100px; border-top: 1px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="assets/RFCLOGO.png" style="height: 80px; opacity: 0.9; margin-bottom: 20px;" alt="RFC Logo">
    <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com [cite: 44]</p>
    <p>© 2025 RPI Flying Club. All rights reserved[cite: 66, 67].</p>
  </footer>
</div>

<script>
  window.onscroll = function() {
    var bg = document.getElementById("heroBg");
    if (document.body.scrollTop > 60 || document.documentElement.scrollTop > 60) {
      bg.classList.add("blurred-more");
    } else {
      bg.classList.remove("blurred-more");
    }
  };
</script>
