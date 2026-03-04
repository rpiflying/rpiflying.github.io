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

  /* SIDEBAR STACK */
  .social-stack {
    position: fixed; bottom: 2.5rem; right: 2.5rem; 
    display: flex; flex-direction: column; gap: 1rem; z-index: 99999;
  }
  .social-fab {
    width: 4.5rem; height: 4.5rem; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 0.5rem 1.5rem rgba(0,0,0,0.3);
    transition: 0.4s; background: white; overflow: hidden;
  }
  .social-fab img { width: 100%; height: 100%; object-fit: cover; }

  /* BACKGROUND & HERO */
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

  /* CONTENT WRAPPER */
  .main-wrapper {
    background: var(--rfc-tan); position: relative; z-index: 100;
    border-radius: 4rem 4rem 0 0; padding: 4rem 8%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6); min-height: 100vh;
  }

  .onboarding-box {
    background: white; border: 4px solid var(--rfc-blue);
    border-radius: 2rem; padding: 2.5rem; margin-bottom: 3rem;
    box-shadow: 0 1rem 2rem rgba(0,0,0,0.05);
  }
  .onboarding-box h2 { font-family: 'Notable', sans-serif; color: var(--rfc-blue); margin-top: 0; font-size: 1.8rem; }
  
  .step-list { list-style: none; padding: 0; margin: 1.5rem 0; }
  .step-list li { margin-bottom: 1rem; font-size: 1.1rem; display: flex; align-items: flex-start; gap: 1rem; line-height: 1.4; }
  .step-num { 
    background: var(--rfc-red); color: white; border-radius: 50%; 
    min-width: 1.8rem; height: 1.8rem; display: flex; align-items: center; 
    justify-content: center; font-weight: bold; font-size: 0.9rem; margin-top: 0.2rem;
  }

  /* BUTTON STYLING */
  .external-button {
    display: inline-block; background: var(--rfc-blue); color: white;
    text-decoration: none; padding: 1rem 2rem; border-radius: 12px;
    font-family: 'Loubag-SemiBold', sans-serif; text-transform: uppercase;
    letter-spacing: 1px; transition: 0.3s; margin-bottom: 2rem;
    border: 2px solid var(--rfc-blue);
  }
  .external-button:hover { background: transparent; color: var(--rfc-blue); transform: scale(1.02); }

  .form-container {
    background: white; border-radius: 2rem; border: 4px solid var(--rfc-gold);
    overflow: hidden; box-shadow: 0 2rem 4rem rgba(0,0,0,0.15);
  }

  @media (max-width: 900px) {
    .hero-title-small { font-size: 14vw; }
    .main-wrapper { padding: 3rem 5%; }
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
    <a href="{{ '/officer-team' | relative_url }}" class="nav-item">Officers</a>
    <a href="{{ '/calendar' | relative_url }}" class="nav-item">Calendar</a>
    <a href="{{ '/join' | relative_url }}" class="nav-item" style="background: var(--rfc-red); color: white; border-radius: 4px;">Join Us</a>
  </div>
</nav>

<div class="social-stack">
  <a href="https://www.instagram.com/flyrpi" class="social-fab" target="_blank"><img src="{{ '/assets/Instagram_logo_2016.png' | relative_url }}" alt="Instagram"></a>
  <a href="https://discord.gg/rXG86ZeBwj" class="social-fab" target="_blank"><img src="{{ '/assets/discord-logo-icon-editorial-free-vector.jpg' | relative_url }}" alt="Discord"></a>
</div>

<div class="join-hero">
  <h1 class="hero-title-small">READY FOR TAKEOFF?</h1>
  <p style="font-family: 'Loubag-SemiBold'; letter-spacing: 0.5rem; color: var(--rfc-red); text-shadow: 0 5px 15px rgba(0,0,0,0.5);">JOIN THE RPI FLYING CLUB</p>
</div>

<div class="main-wrapper">
  
  <div class="onboarding-box">
    <h2>Become a Member</h2>
    <ul class="step-list">
      <li><div class="step-num">1</div> <span>Complete the <strong>RPI Flying Club Membership Sign-Up | Spring 2026</strong> form below.</span></li>
      <li><div class="step-num">2</div> <span>Join our <strong>Discord server</strong> (bottom right button) for immediate updates.</span></li>
      <li><div class="step-num">3</div> <span>Check the <strong>Calendar</strong> for our next Phalanx Room meeting!</span></li>
    </ul>

    <a href="https://docs.google.com/forms/d/e/1FAIpQLScA8EwJXh_nF05OwQ8YK7MFxR7l7vNgNr0qqi2jQ5tdF0d3gQ/viewform" target="_blank" class="external-button">
      Open Form in New Tab ↗
    </a>
  </div>

  <div class="form-container">
    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScA8EwJXh_nF05OwQ8YK7MFxR7l7vNgNr0qqi2jQ5tdF0d3gQ/viewform?embedded=true" width="100%" height="1500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" style="height: 4rem; opacity: 0.9; margin-bottom: 2rem; display: block; margin-left: auto; margin-right: auto; mix-blend-mode: darken;" alt="RFC Logo">
    <p><a href="https://www.linkedin.com/in/andreas-spiratos/" target="_blank" class="developer-credit">✈︎ Made by Andreas Spiratos ✈︎</a></p>
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
</script>
