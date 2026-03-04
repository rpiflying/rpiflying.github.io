---
layout: home
title: Officer Team
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

  * { box-sizing: border-box; }
  html { overflow-y: scroll; } 

  body { 
    margin: 0; padding: 0;
    font-family: 'Loubag', sans-serif;
    background: url('{{ "/assets/bannerbackground.png" | relative_url }}') no-repeat center center fixed;
    background-size: cover;
    background-color: var(--rfc-blue);
    overflow-x: hidden;
  }

  /* NAVIGATION */
  .top-nav {
    position: fixed; top: 0; left: 0; width: 100%; height: 5rem;
    background: #FFF3DC; display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999; border-bottom: 0.2rem solid var(--rfc-gold);
  }
  .nav-logo-img { height: 3.5rem; width: auto; mix-blend-mode: darken; transition: 0.3s; }
  .nav-logo-img:hover { transform: scale(1.05); }
  .nav-links { display: flex; gap: 1rem; align-items: center; }
  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 0.85rem; 
    text-transform: uppercase; letter-spacing: 1px; padding: 0.6rem 1.2rem; 
    border-radius: 8px; transition: 0.3s; display: inline-block;
  }
  .nav-item:hover { color: var(--rfc-red); background-color: rgba(5, 61, 90, 0.08); transform: translateY(-2px); }

  /* SIDEBAR STACK - CONSISTENT WITH JOIN/INDEX */
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

  /* BACKGROUND & HERO */
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

  /* CONTENT WRAPPER */
  .main-wrapper {
    background: var(--rfc-tan); position: relative; z-index: 100;
    border-radius: 4rem 4rem 0 0; padding: 6rem 8%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6); min-height: 100vh;
  }

  /* OFFICER GRID */
  .officer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 3rem;
  }

  .officer-card {
    background: white; border-radius: 2rem; overflow: hidden;
    border: 4px solid var(--rfc-blue); box-shadow: 0 1rem 2rem rgba(0,0,0,0.1);
    transition: 0.3s ease; text-align: center;
  }
  .officer-card:hover { transform: translateY(-10px); border-color: var(--rfc-red); }

  .officer-img {
    width: 100%; height: 350px; object-fit: cover;
    border-bottom: 4px solid var(--rfc-gold);
  }

  .officer-info { padding: 2rem; }
  .officer-name { font-family: 'Notable', sans-serif; color: var(--rfc-blue); font-size: 1.5rem; margin: 0; text-transform: uppercase; }
  .officer-title { color: var(--rfc-red); font-family: 'Loubag-SemiBold'; letter-spacing: 2px; text-transform: uppercase; font-size: 0.9rem; margin-top: 5px; display: block; }
  
  .officer-fact { 
    margin-top: 1.5rem; padding-top: 1.5rem; border-top: 1px solid #eee;
    font-size: 1rem; color: #444; line-height: 1.5; font-style: italic;
  }

  @media (max-width: 900px) {
    .hero-title-small { font-size: 12vw; }
    .main-wrapper { padding: 4rem 5%; }
    .social-stack { bottom: 1.5rem; right: 1.5rem; }
    .social-fab { width: 3.5rem; height: 3.5rem; }
  }

  .developer-credit { text-decoration: none; color: var(--rfc-blue); font-weight: 800; transition: 0.3s; }
  .developer-credit:hover { color: var(--rfc-red); }
</style>

<div class="hero-banner-bg" id="heroBg"></div>

<nav class="top-nav">
  <a href="{{ '/' | relative_url }}"><img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
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
  <h1 class="hero-title-small">MEET THE TEAM</h1>
  <p style="font-family: 'Loubag-SemiBold'; letter-spacing: 0.5rem; color: var(--rfc-red); text-shadow: 0 5px 15px rgba(0,0,0,0.5);">STUDENTS, PILOTS, ENGINEERS, NERDS. [cite: 64]</p>
</div>

<div class="main-wrapper">
  
  <div class="officer-grid">
    <div class="officer-card">
      <img src="{{ '/assets/officer_andreas.jpg' | relative_url }}" class="officer-img" alt="Andreas Spiratos">
      <div class="officer-info">
        <h3 class="officer-name">Andreas Spiratos [cite: 58]</h3>
        <span class="officer-title">President [cite: 58]</span>
        <p class="officer-fact">"Fun Fact: I once [Add Fun Fact Here]!"</p>
      </div>
    </div>

  <div class="officer-card">
      <img src="{{ '/assets/officer_jordan.jpg' | relative_url }}" class="officer-img" alt="Jordan Woodman">
      <div class="officer-info">
        <h3 class="officer-name">Jordan Woodman [cite: 61]</h3>
        <span class="officer-title">Vice President [cite: 62]</span>
        <p class="officer-fact">"Fun Fact: My favorite aircraft is the [Add Plane Here]!"</p>
      </div>
    </div>

  <div class="officer-card">
      <img src="{{ '/assets/officer_jack.jpg' | relative_url }}" class="officer-img" alt="Jack Pirrong">
      <div class="officer-info">
        <h3 class="officer-name">Jack Pirrong</h3>
        <span class="officer-title">Treasurer</span>
        <p class="officer-fact">"Fun Fact: I have logged over [X] hours in flight sims!"</p>
      </div>
    </div>

  <div class="officer-card">
      <img src="{{ '/assets/officer_stella.jpg' | relative_url }}" class="officer-img" alt="Stella Giarratana">
      <div class="officer-info">
        <h3 class="officer-name">Stella Giarratana [cite: 69]</h3>
        <span class="officer-title">Secretary [cite: 69]</span>
        <p class="officer-fact">"Fun Fact: I am currently working on my [License Type]!"</p>
      </div>
    </div>

  <div class="officer-card">
      <img src="{{ '/assets/officer_matthew.jpg' | relative_url }}" class="officer-img" alt="Matthew Fiorenza">
      <div class="officer-info">
        <h3 class="officer-name">Matthew Fiorenza [cite: 59]</h3>
        <span class="officer-title">Flight Safety Officer [cite: 60]</span>
        <p class="officer-fact">"Fun Fact: My dream destination to fly to is [Place]!"</p>
      </div>
    </div>
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" style="height: 4rem; opacity: 0.9; margin-bottom: 2rem; display: block; margin-left: auto; margin-right: auto; mix-blend-mode: darken;" alt="RFC Logo">
    <p><a href="https://www.linkedin.com/in/andreas-spiratos/" target="_blank" class="developer-credit">✈︎ Made by Andreas Spiratos ✈︎</a></p>
    <p style="font-size: 0.9rem; opacity: 0.7;">© 2026 RPI Flying Club. All rights reserved. </p>
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
