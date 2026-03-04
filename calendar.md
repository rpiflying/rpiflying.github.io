---
layout: home
title: Events Calendar
permalink: /calendar/
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

  /* Force identical box model as index.md */
  * { box-sizing: border-box; }

  body { 
    margin: 0; padding: 0;
    font-family: 'Loubag', sans-serif;
    background: url('{{ "/assets/bannerbackground.png" | relative_url }}') no-repeat center center fixed;
    background-size: cover;
    background-color: var(--rfc-blue);
    overflow-x: hidden;
  }

  /* NAVIGATION - 100% Match to Index.md */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 5rem;
    background: #FFF3DC; 
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 0.2rem solid var(--rfc-gold);
  }

  .nav-logo-img { 
    height: 3.5rem; 
    width: auto; 
    mix-blend-mode: darken; 
    transition: transform 0.3s;
  }
  .nav-logo-img:hover { transform: scale(1.05); }

  .nav-links { display: flex; gap: 1rem; align-items: center; }

  .nav-item { 
    text-decoration: none; 
    color: var(--rfc-blue); 
    font-weight: 800; 
    font-size: 0.85rem; 
    text-transform: uppercase; 
    letter-spacing: 1px;
    padding: 0.6rem 1.2rem; 
    border-radius: 8px; 
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); 
    position: relative;
    display: inline-block;
  }
  
  .nav-item:hover { 
    background-color: rgba(5, 61, 90, 0.08); 
    color: var(--rfc-red); 
    transform: translateY(-2px); 
  }

  /* SIDEBAR */
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

  /* MOBILE FIXES */
  @media (max-width: 768px) {
    .top-nav { height: 4.5rem; }
    .nav-logo-img { height: 3rem; }
    .nav-links { display: none; } /* Or keep your toggle script if you use it */
  }

  .developer-credit { text-decoration: none; color: var(--rfc-blue); font-weight: 800; transition: 0.3s; display: inline-block; }
  .developer-credit:hover { color: var(--rfc-red); transform: translateY(-2px); }
</style>

<div class="hero-banner-bg" id="heroBg"></div>

<nav class="top-nav">
  <a href="{{ '/' | relative_url }}">
    <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" class="nav-logo-img" alt="RFC Logo">
  </a>
  
  <div class="nav-links">
    <a href="{{ '/about' | relative_url }}" class="nav-item">About</a>
    <a href="{{ '/ground-school' | relative_url }}" class="nav-item">Ground School</a>
    <a href="{{ '/officer-team' | relative_url }}" class="nav-item">Officers</a>
    <a href="{{ '/calendar' | relative_url }}" class="nav-item" style="color: var(--rfc-red);">Calendar</a>
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

<div class="calendar-hero">
  <h1 class="hero-title-small">FLIGHT SCHEDULE</h1>
  <p style="font-family: 'Loubag-SemiBold'; letter-spacing: 0.5rem; color: var(--rfc-red); text-shadow: 0 5px 15px rgba(0,0,0,0.5);">EVENTS & MEETINGS</p>
</div>

<div class="main-wrapper">
  <div class="meeting-grid">
    <div class="meeting-info-box">
      <h2>General Meetings</h2>
      <p style="font-size: 1.1rem; line-height: 1.6; margin: 0;">
        <strong style="color: var(--rfc-red);">WHEN:</strong> Wednesdays, 8:00 PM – 9:00 PM <br>
        <strong style="color: var(--rfc-red);">WHERE:</strong> Phalanx Room (RU3502)
      </p>
    </div>
    <div class="meeting-info-box" style="border-color: var(--rfc-red);">
      <h2>Officer Meetings</h2>
      <p style="font-size: 1.1rem; line-height: 1.6; margin: 0;">
        <strong style="color: var(--rfc-red);">WHEN:</strong> Tuesdays, 5:00 PM – 6:00 PM <br>
        <strong style="color: var(--rfc-red);">WHERE:</strong> Union 3rd Floor Room 3602 (RU3602)
      </p>
    </div>
  </div>

  <div class="calendar-embed-container">
    <iframe id="rfc-calendar" src="https://calendar.google.com/calendar/embed?src=rpiflying%40gmail.com&ctz=America%2FNew_York" frameborder="0" scrolling="no"></iframe>
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
  <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" 
       style="height: 4rem; opacity: 0.9; margin-bottom: 2rem; display: block; margin-left: auto; margin-right: auto;" 
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
  function optimizeCalendar() {
    const calendar = document.getElementById('rfc-calendar');
    const isMobile = window.innerWidth < 768;
    let calendarUrl = "https://calendar.google.com/calendar/embed?src=rpiflying%40gmail.com&ctz=America%2FNew_York&showTitle=0&showNav=1&showPrint=0&color=%23CC0403";
    calendar.src = isMobile ? calendarUrl + "&mode=AGENDA" : calendarUrl;
  }

  // Scroll Blur Logic
  window.onscroll = function() {
    var bg = document.getElementById("heroBg");
    if (document.documentElement.scrollTop > 60) {
      bg.classList.add("blurred-more");
    } else {
      bg.classList.remove("blurred-more");
    }
  };

  window.addEventListener('load', optimizeCalendar);
  window.addEventListener('resize', optimizeCalendar);
</script>
