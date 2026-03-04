---
layout: home
title: Join Us
permalink: /join/
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

  /* 1. NAVIGATION - Standardized across all pages */
  .top-nav {
    position: fixed; top: 0; left: 0; width: 100%; height: 5rem;
    background: #FFF3DC; display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999; border-bottom: 0.2rem solid var(--rfc-gold);
    box-sizing: border-box;
  }

  .nav-logo-img { height: 3.5rem; width: auto; mix-blend-mode: darken; transition: transform 0.3s; }
  .nav-logo-img:hover { transform: scale(1.05); }

  .nav-links { display: flex; gap: 1rem; align-items: center; }

  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 0.85rem; 
    text-transform: uppercase; letter-spacing: 1px; padding: 0.6rem 1.2rem; 
    border-radius: 8px; transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative; display: inline-block;
  }

  .nav-item:hover { 
    background-color: rgba(5, 61, 90, 0.08); 
    color: var(--rfc-red); 
    transform: translateY(-2px); 
  }

  .nav-links a[style*="background: var(--rfc-red)"]:hover {
    background-color: #a30302 !important;
    box-shadow: 0 4px 15px rgba(204, 4, 3, 0.3);
    transform: scale(1.05) translateY(-2px) !important;
    color: white !important;
  }

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
  .social-fab:hover { transform: scale(1.15) translateY(-5px); }
  .social-fab img { width: 100%; height: 100%; object-fit: cover; }

  /* 3. HERO SECTION */
  .hero-banner-bg {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: url('{{ "/assets/Heading.png" | relative_url }}') no-repeat center center;
    background-size: cover; filter: blur(3px) brightness(0.6);
    z-index: 1; transition: filter 0.6s ease-out;
  }
  .blurred-more { filter: blur(18px) brightness(0.35) !important; }

  .join-hero {
    height: 45vh; display: flex; flex-direction: column; align-items: center; justify-content: center;
    color: var(--rfc-tan); text-align: center; position: relative; z-index: 5;
  }
  .hero-title-small { font-family: 'Notable', sans-serif; font-size: 6vw; text-shadow: 0 1rem 3rem rgba(0,0,0,0.8); margin: 0; }

  /* 4. MAIN CONTENT WRAPPER */
  .main-wrapper {
    background: var(--rfc-tan); position: relative; z-index: 100;
    border-radius: 4rem 4rem 0 0; padding: 6rem 8%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6); min-height: 100vh;
  }

  /* DUES & BENEFITS GRID */
  .benefits-grid { display: grid; grid-template-columns: 1fr 1.5fr; gap: 2rem; margin-bottom: 4rem; }
  
  .dues-card {
    background: var(--rfc-blue); color: white; border-radius: 2rem; padding: 2.5rem;
    display: flex; flex-direction: column; justify-content: center; text-align: center;
    border: 0.4rem solid var(--rfc-gold);
  }
  .dues-price { font-size: 3.5rem; font-family: 'Notable', sans-serif; color: var(--rfc-gold); margin: 0.5rem 0; }
  .dues-sub { font-size: 0.9rem; opacity: 0.8; text-transform: uppercase; letter-spacing: 2px; }

  .benefits-card {
    background: white; border: 4px solid var(--rfc-blue); border-radius: 2rem; padding: 2.5rem;
    box-shadow: 0 1rem 2rem rgba(0,0,0,0.05);
  }
  .benefits-card h2 { font-family: 'Notable', sans-serif; color: var(--rfc-blue); margin-top: 0; font-size: 1.8rem; }
  
  /* GROUND SCHOOL SPECIAL SECTION */
  .ground-school-promo {
    background: white; border: 4px dashed var(--rfc-red); border-radius: 2rem;
    padding: 3rem; margin-bottom: 4rem; position: relative;
  }
  .promo-tag {
    position: absolute; top: -15px; right: 20px; background: var(--rfc-red);
    color: white; padding: 8px 20px; border-radius: 25px; font-weight: bold; font-size: 0.9rem;
    font-family: 'Loubag-SemiBold', sans-serif;
  }

  .onboarding-box {
    background: white; border: 4px solid var(--rfc-blue);
    border-radius: 2rem; padding: 3rem; margin-bottom: 4rem;
  }
  
  .step-list { list-style: none; padding: 0; margin: 1.5rem 0; }
  .step-list li { margin-bottom: 1.2rem; font-size: 1.15rem; display: flex; align-items: flex-start; gap: 1.2rem; line-height: 1.5; color: var(--rfc-blue); }
  .step-num { 
    background: var(--rfc-red); color: white; border-radius: 50%; 
    min-width: 2rem; height: 2rem; display: flex; align-items: center; 
    justify-content: center; font-weight: bold; font-size: 1rem; margin-top: 0.1rem;
  }

  .external-button {
    display: inline-block; background: var(--rfc-blue); color: white;
    text-decoration: none; padding: 1.2rem 2.5rem; border-radius: 12px;
    font-family: 'Loubag-SemiBold', sans-serif; text-transform: uppercase;
    letter-spacing: 1.5px; transition: 0.3s; border: 2px solid var(--rfc-blue);
    margin-top: 1rem;
  }
  .external-button:hover { background: transparent; color: var(--rfc-blue); transform: translateY(-3px); box-shadow: 0 5px 15px rgba(5,61,90,0.2); }

  .form-container {
    background: white; border-radius: 2.5rem; border: 0.5rem solid var(--rfc-gold);
    overflow: hidden; box-shadow: 0 2rem 5rem rgba(0,0,0,0.2);
  }

  /* FOOTER & CREDITS */
  .developer-credit {
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 1.1rem;
    transition: all 0.3s ease; display: inline-block;
  }
  .developer-credit span { font-size: 0.8rem; margin: 0 4px; transition: transform 0.3s ease; display: inline-block; }
  .developer-credit:hover { color: var(--rfc-red); transform: translateY(-2px); }
  .developer-credit:hover span { transform: translate(2px, -2px); }

  /* MOBILE RESPONSIVENESS */
  @media (max-width: 992px) {
    .menu-toggle { display: flex; }
    .nav-links {
      position: fixed; top: 0; right: -100%; width: 70%; height: 100vh;
      background: var(--rfc-tan); display: flex; flex-direction: column; 
      justify-content: flex-start; padding-top: 6rem; transition: 0.5s; z-index: 10000;
      box-shadow: -10px 0 30px rgba(0,0,0,0.3);
    }
    .nav-links.active { right: 0; }
    .nav-item { font-size: 1.5rem; width: 100%; text-align: center; padding: 1.5rem 0; }
  }

  @media (max-width: 900px) {
    .benefits-grid { grid-template-columns: 1fr; }
    .hero-title-small { font-size: 12vw; }
    .main-wrapper { padding: 4rem 5%; border-radius: 2.5rem 2.5rem 0 0; }
    .social-stack { bottom: 1.5rem; right: 1.5rem; }
    .social-fab { width: 3.5rem; height: 3.5rem; }
  }
</style>

<div class="hero-banner-bg" id="heroBg"></div>

<nav class="top-nav">
  <a href="{{ '/' | relative_url }}"><img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" class="nav-logo-img" alt="RFC Logo"></a>
  
  <div class="menu-toggle" id="mobile-menu">
    <span></span><span></span><span></span>
  </div>

  <div class="nav-links" id="nav-list">
    <a href="{{ '/about' | relative_url }}" class="nav-item">About</a>
    <a href="{{ '/ground-school' | relative_url }}" class="nav-item">Ground School</a>
    <a href="{{ '/officer-team' | relative_url }}" class="nav-item">Officers</a>
    <a href="{{ '/calendar' | relative_url }}" class="nav-item">Calendar</a>
    <a href="{{ '/join' | relative_url }}" class="nav-item" style="background: var(--rfc-red); color: white; border-radius: 4px;">Join Us</a>
  </div>
</nav>

<div class="social-stack">
  <a href="https://www.instagram.com/flyrpi" class="social-fab" target="_blank">
    <img src="{{ '/assets/Instagram_logo_2016.png' | relative_url }}" alt="Instagram">
  </a>
  <a href="https://discord.gg/rXG86ZeBwj" class="social-fab" target="_blank">
    <img src="{{ '/assets/discord-logo-icon-editorial-free-vector.jpg' | relative_url }}" alt="Discord">
  </a>
</div>

<div class="join-hero">
  <h1 class="hero-title-small">READY FOR TAKEOFF?</h1>
  <p style="font-family: 'Loubag-SemiBold'; letter-spacing: 0.5rem; color: var(--rfc-red); text-shadow: 0 5px 15px rgba(0,0,0,0.5);">JOIN THE RPI FLYING CLUB</p>
</div>

<div class="main-wrapper">

  <div class="benefits-grid">
    <div class="dues-card">
      <span class="dues-sub">Membership Dues</span>
      <div class="dues-price">$30</div>
      <span style="font-weight: bold; letter-spacing: 1px;">PER SEMESTER</span>
      <div style="margin: 2rem 0; height: 2px; background: rgba(255,255,255,0.2);"></div>
      <div class="dues-price" style="font-size: 2.5rem;">$50</div>
      <span style="font-weight: bold; letter-spacing: 1px;">FULL YEAR (SAVE $10!)</span>
    </div>

  <div class="benefits-card">
      <h2>Member Benefits</h2>
      <ul class="step-list" style="margin: 0;">
        <li><div class="step-num" style="background: var(--rfc-gold);">✈</div> <span>Access to all club meetings, trips, & events</span></li>
        <li><div class="step-num" style="background: var(--rfc-gold);">✈</div> <span>Discounted paid trip fees (Fly-ins, Hangar tours)</span></li>
        <li><div class="step-num" style="background: var(--rfc-gold);">✈</div> <span>Free food & drinks at Social Nights</span></li>
        <li><div class="step-num" style="background: var(--rfc-gold);">✈</div> <span>Members-only merchandise store access</span></li>
        <li><div class="step-num" style="background: var(--rfc-gold);">✈</div> <span>Exclusive networking with industry alumni</span></li>
      </ul>
    </div>
  </div>

  <div class="ground-school-promo">
    <div class="promo-tag">NEW FOR 2026/27</div>
    <h2 style="font-family: 'Notable', sans-serif; color: var(--rfc-red); margin-top: 0; font-size: 2rem;">Ground School Discounts</h2>
    <p style="font-size: 1.2rem; line-height: 1.6; color: var(--rfc-blue);">
      Our <strong>Ground School</strong> program (hosted in partnership with <strong>Hewison Aviation</strong>) is open to the entire RPI community. However, RFC members receive significant tuition subsidies:
    </p>
    <ul class="step-list">
      <li><strong>Non-Members:</strong> Pay full student rate (Approx. $60).</li>
      <li><strong>One-Semester Members:</strong> $20 discount substituted from membership income.</li>
      <li><strong>Full-Year Members:</strong> $40 discount substituted from membership income.</li>
    </ul>
    <a href="{{ '/ground-school' | relative_url }}" class="external-button" style="background: var(--rfc-red); border-color: var(--rfc-red);">Learn More About Ground School</a>
  </div>
  
  <div class="onboarding-box">
    <h2 style="font-family: 'Notable', sans-serif; color: var(--rfc-blue); margin-top: 0; font-size: 2rem;">How to Join</h2>
    <ul class="step-list">
      <li><div class="step-num">1</div> <span>Complete the <strong>RPI Flying Club Membership Sign-Up</strong> form below.</span></li>
      <li><div class="step-num">2</div> <span>Join our <strong>Discord server</strong> (bottom right) for immediate updates.</span></li>
      <li><div class="step-num">3</div> <span>Check the <strong>Calendar</strong> for our next meeting in the Phalanx Room!</span></li>
    </ul>

  <a href="https://docs.google.com/forms/d/e/1FAIpQLScA8EwJXh_nF05OwQ8YK7MFxR7l7vNgNr0qqi2jQ5tdF0d3gQ/viewform" target="_blank" class="external-button">
      Open Form in New Tab ↗
  </a>
  </div>

  <div class="form-container">
    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScA8EwJXh_nF05OwQ8YK7MFxR7l7vNgNr0qqi2jQ5tdF0d3gQ/viewform?embedded=true" width="100%" height="1000" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" 
         style="height: 4rem; opacity: 0.9; margin-bottom: 2rem; display: block; margin-left: auto; margin-right: auto; mix-blend-mode: darken;" 
         alt="RFC Logo">
  
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
