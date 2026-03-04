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

  body { 
    margin: 0; padding: 0;
    font-family: 'Loubag', sans-serif;
    background: url('{{ "/assets/bannerbackground.png" | relative_url }}') no-repeat center center fixed;
    background-size: cover;
    background-color: var(--rfc-blue);
    overflow-x: hidden;
  }

  .top-nav {
    position: fixed; top: 0; left: 0; width: 100%; height: 5rem;
    background: #FFF3DC; display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999; border-bottom: 0.2rem solid var(--rfc-gold); box-sizing: border-box;
  }
  .nav-logo-img { height: 3.5rem; mix-blend-mode: darken; }
  .nav-links { display: flex; gap: 1rem; }
  .nav-item { text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 0.85rem; text-transform: uppercase; padding: 0.6rem 1.2rem; transition: 0.3s; }
  .nav-item:hover { color: var(--rfc-red); transform: translateY(-2px); }

  .calendar-hero {
    height: 45vh; display: flex; flex-direction: column; align-items: center; justify-content: center;
    color: var(--rfc-gold); text-align: center; position: relative; z-index: 5;
  }
  .hero-title-small { font-family: 'Notable', sans-serif; font-size: 6vw; text-shadow: 0 1rem 3rem rgba(0,0,0,0.8); margin: 0; }

  .main-wrapper {
    background: var(--rfc-tan); position: relative; z-index: 100;
    border-radius: 4rem 4rem 0 0; padding: 4rem 8%;
    box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6); min-height: 100vh;
  }

  /* Info Section Grid */
  .meeting-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    margin-bottom: 3rem;
  }

  .meeting-info-box {
    background: white; border: 4px solid var(--rfc-blue);
    border-radius: 2rem; padding: 2rem;
    box-shadow: 0 1rem 2rem rgba(0,0,0,0.05);
  }

  .meeting-info-box h2 { 
    font-family: 'Notable', sans-serif; 
    color: var(--rfc-blue); 
    font-size: 1.6rem; 
    margin: 0 0 1rem 0; 
  }

  .calendar-embed-container {
    position: relative; padding-bottom: 75%; height: 0; overflow: hidden;
    border-radius: 2rem; border: 4px solid var(--rfc-gold);
    box-shadow: 0 2rem 4rem rgba(0,0,0,0.15); background: white;
  }

  .calendar-embed-container iframe {
    position: absolute; top: 0; left: 0; width: 100%; height: 100%;
  }

  @media (max-width: 900px) {
    .meeting-grid { grid-template-columns: 1fr; }
    .hero-title-small { font-size: 14vw; }
    .main-wrapper { padding: 3rem 5%; border-radius: 2.5rem 2.5rem 0 0; }
    .calendar-embed-container { padding-bottom: 150%; }
  }

  .developer-credit { text-decoration: none; color: var(--rfc-blue); font-weight: 800; transition: 0.3s; }
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
  
  <div class="meeting-grid">
    <div class="meeting-info-box">
      <h2>General Meetings</h2>
      <p style="font-size: 1.1rem; line-height: 1.6; margin: 0;">
        <strong style="color: var(--rfc-red);">WHEN:</strong> Wednesdays, 8:00 PM <br>
        <strong style="color: var(--rfc-red);">WHERE:</strong> Phalanx Room (RU3502)
      </p>
      <p style="opacity: 0.7; font-size: 0.9rem; margin-top: 10px;">Open to all RPI students and aviation enthusiasts.</p>
    </div>

  <div class="meeting-info-box" style="border-color: var(--rfc-gold);">
      <h2>Officer Meetings</h2>
      <p style="font-size: 1.1rem; line-height: 1.6; margin: 0;">
        <strong style="color: var(--rfc-red);">WHEN:</strong> Tuesdays, 5:00 PM – 6:00 PM <br>
        <strong style="color: var(--rfc-red);">WHERE:</strong> Room 3602 (RU3602)
      </p>
      <p style="opacity: 0.7; font-size: 0.9rem; margin-top: 10px;">Executive board planning and organizational sessions.</p>
    </div>
  </div>

  <div class="calendar-embed-container">
    <iframe id="rfc-calendar" src="https://calendar.google.com/calendar/embed?src=rpiflying%40gmail.com&ctz=America%2FNew_York" frameborder="0" scrolling="no"></iframe>
  </div>

  <footer style="text-align: center; padding-top: 5rem; margin-top: 5rem; border-top: 3px solid var(--rfc-gold); color: var(--rfc-blue);">
    <p><a href="https://www.linkedin.com/in/andreas-spiratos/" target="_blank" class="developer-credit">✈︎ Made by Andreas Spiratos ✈︎</a></p>
  </footer>
</div>

<script>
  function optimizeCalendar() {
    const calendar = document.getElementById('rfc-calendar');
    const isMobile = window.innerWidth < 768;
    let calendarUrl = "https://calendar.google.com/calendar/embed?src=rpiflying%40gmail.com&ctz=America%2FNew_York&showTitle=0&showNav=1&showPrint=0&color=%23CC0403";
    
    if (isMobile) {
      calendar.src = calendarUrl + "&mode=AGENDA";
    } else {
      calendar.src = calendarUrl;
    }
  }
  window.addEventListener('load', optimizeCalendar);
  window.addEventListener('resize', optimizeCalendar);
</script>
