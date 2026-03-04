---
layout: home
---

<head>
  <link rel="icon" type="image/png" href="{{ '/assets/RFC_icon.png?v=2' | relative_url }}">
  <link rel="apple-touch-icon" href="{{ '/assets/RFC_icon.png' | relative_url }}">
  <link href="https://fonts.googleapis.com/css2?family=Notable&display=swap" rel="stylesheet">
</head>

<style>
  @font-face {
    font-family: 'Loubag';
    src: url('{{ "/assets/loubag.ttf" | relative_url }}') format('truetype');
  }
  @font-face {
    font-family: 'Loubag-SemiBold';
    src: url('{{ "/assets/loubag-semi-bold.ttf" | relative_url }}') format('truetype');
  }

  :root {
    --rfc-red: #CC0403;
    --rfc-blue: #053D5A;
    --rfc-tan: #FFF3DC;
    --rfc-gold: #CC8917;
  }

  /* 1. UI CONSISTENCY FIXES */
  * { box-sizing: border-box; }
  html { font-size: 16px; overflow-y: scroll; }
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

  /* 2. NAVIGATION - Standardized Height */
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

  /* 3. HERO SECTION */
  .hero-banner-bg {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: url('{{ "/assets/BANNER.png" | relative_url }}') no-repeat center center;
    background-size: cover; filter: blur(3px) brightness(0.6);
    z-index: 1; transition: filter 0.6s ease-out;
  }
  .blurred-more { filter: blur(18px) brightness(0.35) !important; }

  .hero-content-layer {
    position: fixed; top: 0; left: 0; width: 100%; height: 100vh;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    z-index: 5; color: white; text-align: center;
  }

  .animated-logo { 
    width: 11rem; margin-bottom: 4rem; opacity: 0.75; 
    border-radius: 50%; border: 4px solid var(--rfc-gold); 
    background: rgba(255,255,255,0.1); box-shadow: 0 0 20px rgba(0,0,0,0.5); 
  }

  .hero-title { 
    font-family: 'Notable', sans-serif; font-size: 11.2vw; font-weight: 900; font-style: italic; line-height: 1; 
    margin: 0; text-transform: uppercase; width: 90vw; text-shadow: 0 1rem 4rem rgba(0,0,0,0.8); color: var(--rfc-tan);
  }

  .hero-subtitle {
    font-family: 'Loubag-SemiBold', sans-serif; font-weight: 900; font-size: 2.8vw; text-transform: uppercase;
    letter-spacing: 2.4vw; margin-top: 1.8rem; padding-left: 2.4vw; color: var(--rfc-red);
    text-shadow: 0 1rem 4rem rgba(0,0,0,0.8);
  }

  /* 4. MAIN CONTENT */
  .main-wrapper {
    background: var(--rfc-tan); position: relative; z-index: 100; margin-top: 100vh;
    border-radius: 4rem 4rem 0 0; padding: 6rem 8%; box-shadow: 0 -3rem 6rem rgba(0,0,0,0.6);
  }

  .section-title { font-family: 'Notable', sans-serif; font-size: 3.5rem; color: var(--rfc-blue); text-align: center; margin-bottom: 2rem; line-height: 1.1; }
  #main-heading { font-size: 3rem; margin-top: 1rem; white-space: nowrap; }
  
  .advancing-panel { text-align: center; margin-bottom: 6rem; }
  .advancing-panel p { color: #333; font-size: 1.4rem; max-width: 900px; margin: 0 auto; line-height: 1.7; }

  .achievement-panel {
    background: white; 
    padding: 4rem; 
    border-radius: 2.5rem;
    display: flex; 
    align-items: center; 
    justify-content: center; /* Changed from space-between to center */
    flex-wrap: wrap; 
    margin-bottom: 6rem; 
    border: 0.6rem solid var(--rfc-red);
    gap: 4rem; /* Increased gap for better breathing room */
    width: 100%; 
    box-sizing: border-box;
  }

  .achievement-text { 
    flex: 1; 
    min-width: 300px; /* Prevents text from becoming too narrow */
  }

  .bar-logo { height: 13rem; width: auto; object-fit: contain ;}

  /* 5. CLICKABLE EVENT PICTURES (BOARDS) */
  .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr)); gap: 3rem; }

  .gallery-item {
    position: relative;
    border-radius: 2rem;
    overflow: hidden;
    /* The "Board" border - makes them pop from the tan background */
    border: 8px solid white; 
    box-shadow: 0 1rem 3rem rgba(0,0,0,0.15);
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    cursor: pointer;
    background: white;
    display: block;
  }

  .gallery-item:hover {
    transform: scale(1.03) translateY(-15px);
    border-color: var(--rfc-gold);
    box-shadow: 0 2rem 4rem rgba(204, 137, 23, 0.3);
  }

  .gallery-img { 
    width: 100%; height: 30rem; object-fit: cover; 
    display: block; transition: filter 0.4s ease;
  }

  /* Overlay indication that they are clickable */
  .gallery-item::after {
    content: "OPEN GALLERY ↗";
    position: absolute; bottom: 0; left: 0; width: 100%;
    background: var(--rfc-blue); color: white;
    font-family: 'Loubag-SemiBold', sans-serif; font-size: 0.9rem;
    text-align: center; padding: 1rem 0;
    opacity: 0; transform: translateY(100%);
    transition: all 0.3s ease;
  }

  .gallery-item:hover::after { opacity: 1; transform: translateY(0); }
  .gallery-item:hover .gallery-img { filter: brightness(0.7); }

  /* 6. SOCIAL STACK */
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

  /* 7. LIGHTBOX STYLING */
  .lightbox {
    display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(0, 0, 0, 0.9); z-index: 100000; align-items: center; justify-content: center;
  }
  .lightbox:target { display: flex; }
  .lightbox-content { position: relative; max-width: 90%; max-height: 80vh; display: flex; flex-direction: column; align-items: center; }
  .lightbox-content img { max-height: 70vh; max-width: 100%; border-radius: 10px; border: 2px solid var(--rfc-gold); }
  
  .exit-btn {
    position: absolute; top: 10px; right: 20px; color: white; font-size: 50px; 
    text-decoration: none; font-weight: bold; z-index: 100001; text-shadow: 0 0 10px rgba(0,0,0,0.8); transition: 0.3s;
  }
  .exit-btn:hover { color: var(--rfc-red); }
  .lightbox-caption { text-align: center; margin-top: 15px; color: var(--rfc-tan); }
  .lightbox-caption h3 { font-family: 'Notable', sans-serif; margin: 0; color: var(--rfc-gold); }
  .lightbox-close-overlay { position: absolute; width: 100%; height: 100%; cursor: default; }

  /* 8. FOOTER */
  .developer-credit { text-decoration: none; color: var(--rfc-blue); font-weight: 800; font-size: 1.1rem; transition: all 0.3s ease; display: inline-block; }
  .developer-credit span { font-size: 0.8rem; margin-left: 4px; transition: transform 0.3s ease; display: inline-block; }
  .developer-credit:hover { color: var(--rfc-red); transform: translateY(-2px); }
  .developer-credit:hover span { transform: translate(2px, -2px); }

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
    #main-heading { white-space: normal; font-size: 2.5rem; }
    .hero-title { font-size: 14vw; } 
    .hero-subtitle { font-size: 4.5vw; letter-spacing: 1vw; }
    .top-nav { height: 4.5rem; }
    .nav-logo-img { height: 3rem !important; width: auto; mix-blend-mode: darken; }
    .achievement-panel {
      flex-direction: column; /* Stacks text on top of logo */
      justify-content: center;
      align-items: center;
      text-align: center;      /* Centers the text lines */
      padding: 2.5rem;
    }

    .achievement-text {
      flex: none;
      width: 100%;
      min-width: 0;
    }
  }
</style>

<nav class="top-nav">
  <a href="{{ '/' | relative_url }}"><img src="{{ '/assets/RFCLOGOthin.png' | relative_url }}" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="menu-toggle" id="mobile-menu"><span></span><span></span><span></span></div>
  <div class="nav-links" id="nav-list">
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

<div class="hero-banner-bg" id="heroBg"></div>
<div class="hero-content-layer">
  <img src="{{ '/assets/RFC-Discord-Logo-Animated-Extended.gif' | relative_url }}" class="animated-logo" alt="RFC Logo">
  <h1 class="hero-title">YOUR JOURNEY STARTS HERE</h1>
  <p class="hero-subtitle">RPI FLYING CLUB</p>
</div>

<div class="main-wrapper">
  
  <div class="advancing-panel">
    <h2 class="section-title" id="main-heading">Advancing Aviation at RPI</h2>
    <p>Students, Pilots, Engineers, Nerds. We are the community for all aviation enthusiasts at Rensselaer. We provide the resources, networking, and environment to jumpstart your aviation journey.</p>
  </div>

  <div class="achievement-panel">
    <div class="achievement-text">
      <h2 style="font-family: 'Notable', sans-serif; color: var(--rfc-blue); font-size: 2.8rem; margin: 0; line-height: 1.1;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.3rem; margin-top: 1.5rem; color: var(--rfc-blue); line-height: 1.5;">Winner of the RPI Brand Competition. Designed to reflect the speed and precision of aviation. Our identity is built to represent the future of flight on campus.</p>
      <p style="font-size: 0.9rem; color: #666; font-style: italic; margin-top: 1rem;">Brand design by Kaden Tennent, Ex-President '23-'25</p>
    </div>
    <img src="{{ '/assets/RPI-Brand-Comp_Runway-Bar_Black-BG-Logo.png' | relative_url }}" class="bar-logo" alt="Runway Bar Award">
  </div>

  <h2 class="section-title">Life at RFC</h2>
  <div class="gallery-grid">
    <a href="#event1" class="gallery-item">
      <img src="{{ '/assets/event1.jpg' | relative_url }}" class="gallery-img" alt="Event 1">
    </a>
    <div id="event1" class="lightbox">
      <a href="#!" class="lightbox-close-overlay"></a>
      <div class="lightbox-content">
        <a href="#!" class="exit-btn">&times;</a>
        <img src="{{ '/assets/event1.jpg' | relative_url }}">
        <div class="lightbox-caption">
          <h3>Green Mountain Aviation Field Day</h3>
          <p>Fall 2024 • Burlington International Airport (BTV), VT</p>
        </div>
      </div>
    </div>

  <a href="#event2" class="gallery-item">
      <img src="{{ '/assets/event2.jpg' | relative_url }}" class="gallery-img" alt="Event 2">
    </a>
    <div id="event2" class="lightbox">
      <a href="#!" class="lightbox-close-overlay"></a>
      <div class="lightbox-content">
        <a href="#!" class="exit-btn">&times;</a>
        <img src="{{ '/assets/event2.jpg' | relative_url }}">
        <div class="lightbox-caption">
          <h3>KittyHawk Rentals Aircraft Tour</h3>
          <p>Fall 2024 • Schenectady County Airport (SCH), NY</p>
        </div>
      </div>
    </div>

  <a href="#event3" class="gallery-item">
      <img src="{{ '/assets/event3.jpg' | relative_url }}" class="gallery-img" alt="Event 3">
    </a>
    <div id="event3" class="lightbox">
      <a href="#!" class="lightbox-close-overlay"></a>
      <div class="lightbox-content">
        <a href="#!" class="exit-btn">&times;</a>
        <img src="{{ '/assets/event3.jpg' | relative_url }}">
        <div class="lightbox-caption">
          <h3>Flight Simulator Night</h3>
          <p>Fall 2025 • Union 3rd Floor RU3202</p>
        </div>
      </div>
    </div>

  <a href="#event4" class="gallery-item">
      <img src="{{ '/assets/event4.jpg' | relative_url }}" class="gallery-img" alt="Event 4">
    </a>
    <div id="event4" class="lightbox">
      <a href="#!" class="lightbox-close-overlay"></a>
      <div class="lightbox-content">
        <a href="#!" class="exit-btn">&times;</a>
        <img src="{{ '/assets/event4.jpg' | relative_url }}">
        <div class="lightbox-caption">
          <h3>KittyHawk Rentals Aircraft Tour</h3>
          <p>Fall 2025 • Schenectady County Airport (SCH), NY</p>
        </div>
      </div>
    </div>
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
