---
layout: home
title: Meet the Officers
permalink: /officer-team/
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

  /* 1. NAVIGATION - Standardized */
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

  .officer-hero {
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

  /* OFFICER GRID LOGIC */
  .officer-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 3rem;
    max-width: 1400px;
    margin: 0 auto;
  }

  .officer-card {
    background: white;
    border-radius: 2rem;
    overflow: hidden;
    border: 4px solid var(--rfc-blue);
    box-shadow: 0 1rem 2rem rgba(0,0,0,0.1);
    transition: 0.3s ease;
    text-align: center;
    flex: 1 1 380px; /* Increased base width from 350px to 380px */
    max-width: 480px; /* Increased max width */
    display: flex;
    flex-direction: column;
  }
  .officer-card:hover { transform: translateY(-10px); border-color: var(--rfc-red); }

  .officer-img { width: 100%; height: 380px; object-fit: cover; border-bottom: 4px solid var(--rfc-gold); }
  .officer-info { padding: 2rem; display: flex; flex-direction: column; flex-grow: 1; }
  .officer-name { font-family: 'Notable', sans-serif; color: var(--rfc-blue); font-size: 1.5rem; margin: 0; text-transform: uppercase; }
  .officer-title { color: var(--rfc-red); font-family: 'Loubag-SemiBold'; letter-spacing: 2px; text-transform: uppercase; font-size: 0.9rem; margin-top: 5px; display: block; }
  
  .officer-meta { margin-top: 1rem; font-size: 0.9rem; color: var(--rfc-blue); opacity: 0.9; line-height: 1.8; }
  .officer-meta a { color: var(--rfc-red); text-decoration: none; font-weight: bold; }

  .officer-fact { 
    margin-top: 1.5rem; padding-top: 1.5rem; border-top: 1px solid #eee;
    font-size: 1rem; color: #444; line-height: 1.5; font-style: italic;
  }

  /* FOOTER & CREDITS */
  .developer-credit {
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 1.1rem;
    transition: all 0.3s ease; display: inline-block;
  }
  .developer-credit span { font-size: 0.8rem; margin: 0 4px; transition: transform 0.3s ease; display: inline-block; }
  .developer-credit:hover { color: var(--rfc-red); transform: translateY(-2px); }
  .developer-credit:hover span { transform: translate(2px, -2px); }

  /* RESPONSIVENESS */
  @media (max-width: 1100px) {
      .officer-card { flex: 1 1 45%; max-width: 500px; }
  }

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

  @media (max-width: 768px) {
    .hero-title-small { font-size: 12vw; }
    .officer-card { flex: 1 1 100%; max-width: 100%; }
    .main-wrapper { padding: 4rem 1.5rem; }
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
    <a href="{{ '/officer-team' | relative_url }}" class="nav-item" style="color: var(--rfc-red);">Officers</a>
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

<div class="officer-hero">
  <h1 class="hero-title-small">MEET THE OFFICERS</h1>
  <p style="font-family: 'Loubag-SemiBold'; letter-spacing: 0.5rem; color: var(--rfc-red); text-shadow: 0 5px 15px rgba(0,0,0,0.5);">STUDENTS, PILOTS, ENGINEERS, NERDS.</p>
</div>

<div class="main-wrapper">
  
  <div class="officer-grid">
    <div class="officer-card">
      <img src="{{ '/assets/AndreasSpiratos.jpg' | relative_url }}" class="officer-img" alt="Andreas Spiratos">
      <div class="officer-info">
        <h3 class="officer-name">Andreas Spiratos</h3>
        <span class="officer-title">President</span>
        <div class="officer-meta">
          📍 Lyndhurst, NJ <br>
          📧 <a href="mailto:spiraa2@rpi.edu">spiraa2@rpi.edu</a> <br>
          ✈️ <b>Favorite Plane:</b> Concorde
        </div>
        <p class="officer-fact">"Fun Fact: I own a 1989 VW Jetta."</p>
      </div>
    </div>

  <div class="officer-card">
      <img src="{{ '/assets/JordanWoodman.jpg' | relative_url }}" class="officer-img" alt="Jordan Woodman">
      <div class="officer-info">
        <h3 class="officer-name">Jordan Woodman</h3>
        <span class="officer-title">Vice President</span>
        <div class="officer-meta">
          📍 Bethel, CT <br>
          📧 <a href="mailto:woodmj2@rpi.edu">woodmj2@rpi.edu</a> <br>
          ✈️ <b>Favorite Plane:</b> F-35B
        </div>
        <p class="officer-fact">"Fun Fact: My dog is fat."</p>
      </div>
    </div>

  <div class="officer-card">
      <img src="{{ '/assets/JackPirrong.jpg' | relative_url }}" class="officer-img" alt="Jack Pirrong">
      <div class="officer-info">
        <h3 class="officer-name">Jack Pirrong</h3>
        <span class="officer-title">Treasurer</span>
        <div class="officer-meta">
          📍 WHO KNOWS?? <br>
          📧 <a href="mailto:pirroj3@rpi.edu">pirroj3@rpi.edu</a> <br>
          ✈️ <b>Favorite Plane:</b> Cirrus SR22
        </div>
        <p class="officer-fact">"Fun Fact: I have logged over 500 hours in Microsoft Flight Simulator!"</p>
      </div>
    </div>

  <div class="officer-card">
      <img src="{{ '/assets/StellaGiarratana.jpg' | relative_url }}" class="officer-img" alt="Stella Giarratana">
      <div class="officer-info">
        <h3 class="officer-name">Stella Giarratana</h3>
        <span class="officer-title">Secretary</span>
        <div class="officer-meta">
          📍 Boston, MA <br>
          📧 <a href="mailto:giarrj@rpi.edu">giarrj@rpi.edu</a> <br>
          ✈️ <b>Favorite Plane:</b> Piper Archer
        </div>
        <p class="officer-fact">"Fun Fact: I am currently working on my Private Pilot License!"</p>
      </div>
    </div>
  
  <div class="officer-card">
      <img src="{{ '/assets/MatthewFiorenza.jpg' | relative_url }}" class="officer-img" alt="Matthew Fiorenza">
      <div class="officer-info">
        <h3 class="officer-name">Matthew Fiorenza</h3>
        <span class="officer-title">Flight Safety Officer</span>
        <div class="officer-meta">
          📍 New York, NY <br>
          📧 <a href="mailto:fiorem2@rpi.edu">fiorem2@rpi.edu</a> <br>
          ✈️ <b>Favorite Plane:</b> Airbus A350
        </div>
        <p class="officer-fact">"Fun Fact: My dream destination to fly to is the Swiss Alps!"</p>
      </div>
    </div>
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" 
         style="height: 4rem; opacity: 0.9; margin-bottom: 2rem; display: block; margin-left: auto; margin-right: auto; mix-blend-mode: darken;" 
         alt="RFC Logo">
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
