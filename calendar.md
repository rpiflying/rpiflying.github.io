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
  /* REUSING YOUR EXACT DESIGN TOKENS */
  @font-face { font-family: 'Loubag'; src: url('{{ "/assets/loubag.ttf" | relative_url }}') format('truetype'); }
  @font-face { font-family: 'Loubag-SemiBold'; src: url('{{ "/assets/loubag-semi-bold.ttf" | relative_url }}') format('truetype'); }

  :root {
    --rfc-red: #CC0403;
    --rfc-blue: #053D5A;
    --rfc-tan: #FFF3DC;
    --rfc-gold: #CC8917;
  }

  body { 
    margin: 0; padding: 0;
    font-family: 'Loubag', sans-serif;
    background: url('{{ "/assets/bannerbackground.png" | relative_url }}') no-repeat center center fixed;
    background-size: cover;
    background-color: var(--rfc-blue);
  }

  /* 1. NAVIGATION REUSE */
  .top-nav {
    position: fixed; top: 0; left: 0; width: 100%; height: 5rem;
    background: #FFF3DC; display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999; border-bottom: 0.2rem solid var(--rfc-gold); box-sizing: border-box;
  }
  .nav-logo-img { height: 3.5rem; mix-blend-mode: darken; }
  .nav-links { display: flex; gap: 1rem; }
  .nav-item { 
    text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 0.85rem; 
    text-transform: uppercase; padding: 0.6rem 1.2rem; transition: all 0.3s;
  }
  .nav-item:hover { color: var(--rfc-red); transform: translateY(-2px); }

  /* 2. CALENDAR SPECIFIC HERO */
  .calendar-hero {
    height: 60vh; /* Shorter than home hero */
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    color: var(--rfc-tan); text-align: center; position: relative; z-index: 5;
  }
  .hero-title-small { 
    font-family: 'Notable', sans-serif; font-size: 6vw; 
    text-shadow: 0 1rem 3rem rgba(0,0,0,0.8); margin: 0;
  }

  /* 3. CALENDAR CONTENT WRAPPER */
  .main-wrapper {
    background: var(--rfc-tan); position: relative; z-index: 100;
    border-radius: 4rem 4rem 0 0; padding: 4rem 8%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6); min-height: 100vh;
  }

  .meeting-info-box {
    background: white; border: 4px solid var(--rfc-blue);
    border-radius: 2rem; padding: 2.5rem; margin-bottom: 4rem;
    display: flex; flex-direction: column; gap: 1rem;
    box-shadow: 0 1rem 2rem rgba(0,0,0,0.05);
  }

  /* RESPONSIVE IFRAME */
  .calendar-embed-container {
    position: relative; padding-bottom: 75%; height: 0; overflow: hidden;
    border-radius: 2rem; border: 4px solid var(--rfc-gold);
    box-shadow: 0 2rem 4rem rgba(0,0,0,0.15);
  }
  .calendar-embed-container iframe {
    position: absolute; top: 0; left: 0; width: 100%; height: 100%;
  }

  @media (max-width: 768px) {
    .hero-title-small { font-size: 12vw; }
    .main-wrapper { padding: 3rem 5%; }
  }

  /* Developer Credit (Reused) */
  .developer-credit { text-decoration: none; color: var(--rfc-blue); font-weight: 800; transition: 0.3s; }
  .developer-credit:hover { color: var(--rfc-red); }
</style>

<nav class="top-nav">
  <a href="/"><img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/officer-team" class="nav-item">Officers</a>
    <a href="/calendar" class="nav-item" style="color: var(--rfc-red);">Calendar</a>
    <a href="/join" class="nav-item" style="background: var(--rfc-red); color: white; border-radius: 4px;">Join Us</a>
  </div>
</nav>

<div class="calendar-hero">
  <h1 class="hero-title-small">FLIGHT SCHEDULE</h1>
  <p style="font-family: 'Loubag-SemiBold'; letter-spacing: 0.5rem; color: var(--rfc-red); text-shadow: 0 5px 15px rgba(0,0,0,0.5);">EVENTS & MEETINGS</p>
</div>

<div class="main-wrapper">
  
  <div class="meeting-info-box">
    <h2 style="font-family: 'Notable', sans-serif; color: var(--rfc-blue); font-size: 2rem; margin: 0;">Weekly General Meetings</h2>
    <p style="font-size: 1.2rem; color: #333; margin: 0.5rem 0;">
      <strong style="color: var(--rfc-red);">WHEN:</strong> Wednesdays, 8:00 PM – 9:00 PM <br>
      <strong style="color: var(--rfc-red);">WHERE:</strong> Phalanx Room (RU3502), Rensselaer Union
    </p>
    <p style="opacity: 0.8; line-height: 1.5;">Our meetings are open to all students. Whether you are a licensed pilot or just like planes, come join the community!</p>
  </div>

  <div class="calendar-embed-container">
    <iframe src="https://calendar.google.com/calendar/embed?height=600&wkst=1&ctz=America%2FNew_York&showPrint=0&src=cnBpZmx5aW5nQGdtYWlsLmNvbQ&src=MzU3MWU2ZjNlZDZlOTRjZDAwOWViNTMzYmE3YmQ3OTQ4ZTNkZTIyYzk1MmExZDc3ZGZmMDQ2NzY3NjI3MTEzY0Bncm91cC5jYWxlbmRhci5nb29nbGUuY29t&color=%23CC0403&color=%23053D5A" frameborder="0" scrolling="no"></iframe>
  </div>

  <footer style="text-align: center; padding-top: 8rem; margin-top: 8rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" style="height: 4rem; opacity: 0.9; margin-bottom: 2rem; mix-blend-mode: darken;" alt="RFC Logo">
    <p style="margin-bottom: 0.5rem;">
      <a href="https://www.linkedin.com/in/andreas-spiratos/" target="_blank" class="developer-credit">
        <span>✈︎</span> Made by Andreas Spiratos (President '25-'26) <span>✈︎</span>
      </a>
    </p>
    <p style="font-size: 0.9rem; opacity: 0.7;">© 2026 RPI Flying Club. All rights reserved.</p>
  </footer>
</div>
