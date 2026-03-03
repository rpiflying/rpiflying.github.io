---
layout: home
---

<style>
  /* Import a professional Sans-Serif font */
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&display=swap');

  body { font-family: 'Inter', sans-serif; color: #333; }
  
  /* Theme Overrides */
  #header { background: #ffffff; border-bottom: 1px solid #eee; padding: 20px 0; }
  #header h1 { color: #D6001C !important; font-weight: 700; letter-spacing: -1px; }
  #header h2 { color: #666 !important; font-weight: 300; }
  
  .banner-container { width: 100%; margin-bottom: 40px; }
  .banner-img { width: 100%; border-radius: 4px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
  
  .btn-join { 
    background-color: #D6001C; 
    color: white !important; 
    padding: 12px 30px; 
    text-decoration: none; 
    border-radius: 2px; 
    font-weight: 600; 
    display: inline-block;
    transition: opacity 0.2s;
  }
  .btn-join:hover { opacity: 0.8; }

  .grid-container { 
    display: grid; 
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
    gap: 20px; 
    margin: 40px 0; 
  }
  
  .gallery-img { 
    width: 100%; 
    height: 300px; 
    object-fit: cover; 
    border-radius: 4px; 
    filter: grayscale(20%);
    transition: filter 0.3s;
  }
  .gallery-img:hover { filter: grayscale(0%); }
</style>

<div class="banner-container">
  <img src="BANNER.png" class="banner-img" alt="RPI Flying Club">
</div>

<div style="text-align: center; max-width: 800px; margin: 0 auto;">
  <h2 style="font-weight: 700; color: #111;">Advancing Aviation at Rensselaer</h2>
  <p style="font-size: 1.1em; color: #666; line-height: 1.6;">
    The RPI Flying Club is a community of pilots and enthusiasts dedicated to making flight accessible to the student body. From ground school to fly-ins, we provide the resources you need to take to the skies.
  </p>
  <a href="/join" class="btn-join">Get On The Flight List</a>
</div>

<div class="grid-container">
  <img src="pic1.jpg" class="gallery-img" alt="Aviation 1">
  <img src="pic2.jpg" class="gallery-img" alt="Aviation 2">
  <img src="pic3.jpg" class="gallery-img" alt="Aviation 3">
</div>

---

### Operations
* **Location:** Rensselaer Union, Troy, NY
* **Contact:** [flying-officers@rpi.edu](mailto:flying-officers@rpi.edu)
* **Status:** [Check Membership Requirements](/join)
