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
    top: 0; left: 0; width: 100%; height: 5.5rem;
    background: #FFF3DC; /* Solid Tan to match logo blend */
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 0.25rem solid var(--rfc-gold);
    box-sizing: border-box;
  }

  .nav-logo-img { 
    height: 4rem; 
    width: auto; 
    /* Ensures logo transparency works perfectly with the tan background */
    mix-blend-mode: darken; 
  }

  .nav-links { display: flex; gap: 1rem; align-items: center; }
  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; 
    font-size: 0.85rem; text-transform: uppercase; letter-spacing: 1px;
    padding: 0.6rem 1rem; transition: 0.3s;
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
  .blurred-more { filter: blur(18px) brightness(0.35) !important; }

  .hero-content-layer {
    position: fixed; top: 0; left: 0; width: 100%; height: 100vh;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    z-index: 5; color: white; text-align: center;
    padding: 0 2%;
  }

  .animated-logo { width: 11rem; margin-bottom: 3rem; opacity: 0.65; }

  .hero-title { 
    font-family: 'Notable', sans-serif;
    font-size: 11vw; font-weight: 900; font-style: italic; line-height: 1; 
    margin: 0; text-transform: uppercase; width: 100%; white-space: nowrap;
    text-shadow: 0 1rem 4rem rgba(0,0,0,0.8); color: var(--rfc-tan);
  }

  .hero-subtitle {
    font-family: 'Loubag-SemiBold', sans-serif;
    font-size: 2.8vw; /* Increased Size */
    font-weight: 900; /* Max Boldness */
    text-transform: uppercase;
    letter-spacing: 2.4vw; 
    margin-top: 2rem; 
    padding-left: 2.4vw; 
    color: var(--rfc-gold);
    text-shadow: 0 0.5rem 1.5rem rgba(0,0,0,0.5);
  }

  /* 3. MAIN CONTENT */
  .main-wrapper {
    background: var(--rfc-tan);
    position: relative; z-index: 100; margin-top: 100vh;
    border-radius: 4rem 4rem 0 0; 
    padding: 6rem 5%; /* Adjusted padding for better internal alignment */
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6);
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .advancing-panel { 
    text-align: center; 
    margin-bottom: 6rem;
    width: 100%;
    max-width: 1200px; /* Constrains header within a column */
  }

  .advancing-panel h2 {
    font-family: 'Notable', sans-serif; 
    font-size: clamp(1.2rem, 4vw, 3.8rem); 
    color: var(--rfc-blue);
    margin: 0 auto 1.5rem auto;
    width: fit-content;
    white-space: nowrap; 
  }

  .advancing-panel p {
    color: #333; font-size: 1.4rem; max-width: 900px; margin: 0 auto; line-height: 1.7;
  }

  /* Fixed Award Panel Layout */
  .achievement-panel {
    background: white; padding: 4rem; border-radius: 2.5rem;
    display: flex; align-items: center; justify-content: space-between;
    flex-wrap: nowrap; /* Prevents overlapping */
    margin-bottom: 6rem; border: 0.6rem solid var(--rfc-red);
    gap: 4rem; 
    width: 100%;
    max-width: 1200px;
    box-sizing: border-box;
  }

  .achievement-text { flex: 2; text-align: left; }
  .achievement-text h2 { white-space: nowrap; font-size: 2.2rem !important; }

  .bar-logo { 
    flex: 1;
    height: auto; 
    max-height: 13rem; 
    width: auto; 
    object-fit: contain;
  }

  .gallery-section { width: 100%; max-width: 1200px; text-align: center; }
  .gallery-title { font-family: 'Notable', sans-serif; font-size: 2.5rem; color: var(--rfc-blue); margin-bottom: 3rem; }
  .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr)); gap: 2rem; }
  .gallery-img { width: 100%; height: 25rem; object-fit: cover; border-radius: 2rem; }

  @media (max-width: 1024px) {
    .achievement-panel { flex-wrap: wrap; justify-content: center; text-align: center; }
    .achievement-text { text-align: center; flex: none; width: 100%; }
    .achievement-text h2 { white-space: normal; }
    .advancing-panel h2 { white-space: normal; line-height: 1.2; }
  }

  @media (max-width: 768px) {
    .hero-subtitle { font-size: 4.5vw; letter-spacing: 1.5vw; }
    .main-wrapper { padding: 4rem 8%; }
  }

</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/officer-team" class="nav-item">Officers</a>
    <a href="/calendar" class="nav-item">Calendar</a>
    <a href="/join" class="nav-item" style="background: var(--rfc-red); color: white; border-radius: 4px;">Join Us</a>
  </div>
</nav>

<div class="hero-banner-bg" id="heroBg"></div>
<div class="hero-content-layer">
  <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" class="animated-logo" alt="RFC Logo">
  <h1 class="hero-title">YOUR JOURNEY STARTS HERE</h1>
  <p class="hero-subtitle">RPI FLYING CLUB</p>
</div>

<div class="main-wrapper">
  
  <div class="advancing-panel">
    <h2>Advancing Aviation at RPI</h2>
    <p>
      Students, Pilots, Engineers, Nerds. We are the community for all aviation enthusiasts at Rensselaer. We provide the resources, networking, and environment to jumpstart your aviation journey.
    </p>
  </div>

  <div class="achievement-panel">
    <div class="achievement-text">
      <h2 style="font-family: 'Notable', sans-serif; color: var(--rfc-blue); margin: 0; line-height: 1.1;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.3rem; margin-top: 1.5rem; color: var(--rfc-blue); line-height: 1.5;">Winner of the RPI Brand Competition. Designed to reflect the speed and precision of aviation. Our identity is built to represent the future of flight on campus.</p>
      <span style="font-size: 0.9rem; color: #888; font-style: italic; display: block; margin-top: 1rem;">Logo designed by Kaden Tennent, Ex-President '23-'25</span>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-BG-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <div class="gallery-section">
    <h2 class="gallery-title">Life at RFC</h2>
    <div class="gallery-grid">
      <img src="assets/event1.jpg" class="gallery-img" alt="Event 1">
      <img src="assets/event2.jpg" class="gallery-img" alt="Event 2">
      <img src="assets/event3.jpg" class="gallery-img" alt="Event 3">
      <img src="assets/event4.jpg" class="gallery-img" alt="Event 4">
    </div>
  </div>

  <footer style="text-align: center; padding: 6rem 0; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue); width: 100%;">
    <img src="assets/RFCLOGO.png" style="height: 6rem; opacity: 0.9; margin-bottom: 2rem; mix-blend-mode: darken;" alt="RFC Logo">
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
</script>
