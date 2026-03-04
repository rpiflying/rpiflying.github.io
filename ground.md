---
layout: home
title: Ground School
permalink: /ground-school/
---

<head>
  <link rel="icon" type="image/png" href="{{ '/assets/RFC_icon.png?v=2' | relative_url }}">
  <link rel="apple-touch-icon" href="{{ '/assets/RFC_icon.png' | relative_url }}">
  <link href="https://fonts.googleapis.com/css2?family=Notable&display=swap" rel="stylesheet">
</head>

<style>
  @font-face { font-family: 'Loubag'; src: url('{{ "/assets/loubag.ttf" | relative_url }}') format('truetype'); }
  @font-face { font-family: 'Loubag-SemiBold'; src: url('{{ "/assets/loubag-semi-bold.ttf" | relative_url }}') format('truetype'); }

  :root {
    --rfc-red: #CC0403;
    --rfc-blue: #053D5A;
    --rfc-tan: #FFF3DC;
    --rfc-gold: #CC8917;
  }

  /* UI CONSISTENCY FIXES */
  * { box-sizing: border-box; }
  html { overflow-y: scroll; font-size: 16px; }
  @media (max-width: 768px) { html { font-size: 14px; } }

  body { 
    margin: 0; padding: 0;
    font-family: 'Loubag', sans-serif;
    background: url('{{ "/assets/bannerbackground.png" | relative_url }}') no-repeat center center fixed;
    background-size: cover;
    background-color: var(--rfc-blue);
    overflow-x: hidden;
  }

  header.site-header, .site-title, #header, .header-site { display: none !important; }

  /* 1. NAVIGATION */
  .top-nav {
    position: fixed; top: 0; left: 0; width: 100%; height: 5rem;
    background: #FFF3DC; display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999; border-bottom: 0.2rem solid var(--rfc-gold);
    box-sizing: border-box;
  }

  @media (max-width: 768px) { 
    .top-nav { height: 4.5rem; } 
    .nav-logo-img { height: 3rem !important; width: auto; mix-blend-mode: darken; }
  }

  .nav-logo-img { height: 3.5rem; width: auto; mix-blend-mode: darken; transition: transform 0.3s; }
  .nav-logo-img:hover { transform: scale(1.05); }

  .nav-links { display: flex; gap: 1rem; align-items: center; }
  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 0.85rem; 
    text-transform: uppercase; letter-spacing: 1px; padding: 0.6rem 1.2rem; 
    border-radius: 8px; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  }
  .nav-item:hover { background-color: rgba(5, 61, 90, 0.08); color: var(--rfc-red); transform: translateY(-2px); }

  .menu-toggle { display: none; flex-direction: column; gap: 5px; cursor: pointer; z-index: 10001; }
  .menu-toggle span { width: 30px; height: 3px; background: var(--rfc-blue); border-radius: 10px; }

  /* 2. SIDEBAR STACK */
  .social-stack {
    position: fixed; bottom: 2.5rem; right: 2.5rem; 
    display: flex; flex-direction: column; gap: 1rem; z-index: 99999;
  }
  .social-fab {
    width: 4.5rem; height: 4.5rem; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 0.5rem 1.5rem rgba(0,0,0,0.3);
    transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    background: white; overflow: hidden;
  }
  .social-fab img { width: 100%; height: 100%; object-fit: cover; }

  /* 3. HERO SECTION */
  .hero-banner-bg {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: url('{{ "/assets/Heading.png" | relative_url }}') no-repeat center center;
    background-size: cover; filter: blur(3px) brightness(0.6);
    z-index: 1; transition: filter 0.6s ease-out;
  }
  .blurred-more { filter: blur(18px) brightness(0.35) !important; }

  .gs-hero {
    height: 45vh; display: flex; flex-direction: column; align-items: center; justify-content: center;
    color: var(--rfc-tan); text-align: center; position: relative; z-index: 5;
  }
  .hero-title-small { font-family: 'Notable', sans-serif; font-size: 6vw; text-shadow: 0 1rem 3rem rgba(0,0,0,0.8); margin: 0; }

  /* 4. MAIN CONTENT WRAPPER */
  .main-wrapper {
    background: var(--rfc-tan); position: relative; z-index: 100;
    border-radius: 4rem 4rem 0 0; padding: 6rem 10%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6); min-height: 100vh;
  }

  .gs-section { margin-bottom: 5rem; }
  .gs-h2 { 
    font-family: 'Notable', sans-serif; color: var(--rfc-blue); 
    font-size: 2.5rem; border-left: 8px solid var(--rfc-red); 
    padding-left: 1.5rem; margin-bottom: 2rem; 
  }
  .gs-p { font-size: 1.2rem; line-height: 1.8; color: #333; margin-bottom: 1.5rem; }

  /* ROADMAP CARDS (Uniform with Officer Cards) */
  .roadmap-grid {
    display: flex; flex-wrap: wrap; justify-content: center; gap: 2.5rem; margin-top: 3rem;
  }
  .roadmap-card {
    background: white; border-radius: 2rem; border: 4px solid var(--rfc-blue);
    padding: 2.5rem; flex: 1 1 300px; max-width: 400px;
    box-shadow: 0 1rem 2rem rgba(0,0,0,0.05); transition: 0.3s ease;
  }
  .roadmap-card:hover { transform: translateY(-10px); border-color: var(--rfc-red); }
  .step-num { font-family: 'Notable', sans-serif; color: var(--rfc-red); font-size: 1.2rem; display: block; margin-bottom: 0.5rem; }
  .step-title { font-family: 'Notable', sans-serif; color: var(--rfc-blue); font-size: 1.5rem; display: block; margin-bottom: 1rem; }

  @media (max-width: 992px) {
    .menu-toggle { display: flex; }
    .nav-links {
      position: fixed; top: 0; right: -100%; width: 70%; height: 100vh;
      background: var(--rfc-tan); display: flex; flex-direction: column; 
      justify-content: flex-start; padding-top: 6rem; transition: 0.5s; z-index: 10000;
    }
    .nav-links.active { right: 0; }
    .nav-item { font-size: 1.5rem; width: 100%; text-align: center; padding: 1.5rem 0; }
  }

  @media (max-width: 768px) {
    .hero-title-small { font-size: 12vw; }
    .main-wrapper { padding: 4rem 8%; }
  }
</style>

<div class="hero-banner-bg" id="heroBg"></div>

<nav class="top-nav">
  <a href="{{ '/' | relative_url }}"><img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="menu-toggle" id="mobile-menu"><span></span><span></span><span></span></div>
  <div class="nav-links" id="nav-list">
    <a href="{{ '/about' | relative_url }}" class="nav-item">About</a>
    <a href="{{ '/ground-school' | relative_url }}" class="nav-item" style="color: var(--rfc-red);">Ground School</a>
    <a href="{{ '/officer-team' | relative_url }}" class="nav-item">Officers</a>
    <a href="{{ '/calendar' | relative_url }}" class="nav-item">Calendar</a>
    <a href="{{ '/join' | relative_url }}" class="nav-item" style="background: var(--rfc-red); color: white; border-radius: 4px;">Join Us</a>
  </div>
</nav>

<div class="social-stack">
  <a href="https://www.instagram.com/flyrpi" class="social-fab" target="_blank"><img src="{{ '/assets/Instagram_logo_2016.png' | relative_url }}" alt="Instagram"></a>
  <a href="https://discord.gg/rXG86ZeBwj" class="social-fab" target="_blank"><img src="{{ '/assets/discord-logo-icon-editorial-free-vector.jpg' | relative_url }}" alt="Discord"></a>
</div>

<div class="gs-hero">
  <h1 class="hero-title-small">GROUND SCHOOL</h1>
  <p style="font-family: 'Loubag-SemiBold'; letter-spacing: 0.5rem; color: var(--rfc-red); text-shadow: 0 5px 15px rgba(0,0,0,0.5);">MASTER THE SKY, STARTING HERE.</p>
</div>

<div class="main-wrapper">
  
  <div class="gs-section">
    <h2 class="gs-h2">LEARN TO FLY</h2>
    <p class="gs-p">Ground school is where every pilot's journey begins. Before you take control of an aircraft, you must understand the science, law, and environment of the sky. The RPI Flying Club offers student-led sessions that cover the essential knowledge required for the FAA Private Pilot Knowledge Test.</p>
  </div>

  <h2 class="gs-h2">THE PILOT ROADMAP</h2>
  <div class="roadmap-grid">
    <div class="roadmap-card">
      <span class="step-num">STEP 01</span>
      <span class="step-title">Aerodynamics</span>
      <p class="gs-p" style="font-size: 1rem;">Understand the four forces of flight, how wings generate lift, and how flight controls manipulate the air.</p>
    </div>
    <div class="roadmap-card">
      <span class="step-num">STEP 02</span>
      <span class="step-title">Instruments</span>
      <p class="gs-p" style="font-size: 1rem;">Learn the 'Six Pack' of flight instruments that tell you your speed, altitude, and orientation.</p>
      
  </div>
    <div class="roadmap-card">
      <span class="step-num">STEP 03</span>
      <span class="step-title">Weather</span>
      <p class="gs-p" style="font-size: 1rem;">Decode METARs and TAFs, and learn to identify dangerous clouds, fronts, and wind shear.</p>
    </div>
    <div class="roadmap-card">
      <span class="step-num">STEP 04</span>
      <span class="step-title">Navigation</span>
      <p class="gs-p" style="font-size: 1rem;">Plot your course using VORs, GPS, and traditional paper sectionals and E6B flight computers.</p>
    </div>
  </div>

  <div class="gs-section" style="margin-top: 6rem;">
    <h2 class="gs-h2">MEETING TIMES</h2>
    <p class="gs-p">Ground school sessions are held weekly on campus. These sessions are free for all members and are designed to be interactive, featuring group problem-solving and flight simulator demonstrations.</p>
    <div style="background: white; padding: 2rem; border-radius: 1.5rem; border: 2px dashed var(--rfc-gold); text-align: center;">
       <p class="gs-p" style="margin:0;"><strong>Check the <a href="{{ '/calendar' | relative_url }}" style="color:var(--rfc-red); text-decoration:none;">Club Calendar</a> for this semester's schedule and room location.</strong></p>
    </div>
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" style="height: 4rem; opacity: 0.9; margin-bottom: 2rem; display: block; margin-left: auto; margin-right: auto; mix-blend-mode: darken;" alt="RFC Logo">
    <div style="margin-bottom: 1.5rem;">
    <p style="font-family: 'Notable', sans-serif; font-size: 0.9rem; margin-bottom: 0.5rem; letter-spacing: 1px;">RADIO IN / CONTACT US</p>
    <a href="mailto:rpiflying@gmail.com" 
       style="text-decoration: none; color: var(--rfc-red); font-family: 'Loubag-SemiBold'; font-size: 1.2rem; transition: 0.3s opacity;"
       onmouseover="this.style.opacity='0.7'" onmouseout="this.style.opacity='1'">
       rpiflying@gmail.com
    </a>
  </div>
    <p style="margin-bottom: 0.5rem;">
      <a href="https://www.linkedin.com/in/andreas-spiratos/" target="_blank" class="developer-credit">
        <span>✈︎</span> Made by Andreas Spiratos (President '25-'26) <span>✈︎</span>
      </a>
    </p>
    <p style="font-size: 0.9rem; opacity: 0.7;">© 2026 RPI Flying Club. All rights reserved.</p>
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
