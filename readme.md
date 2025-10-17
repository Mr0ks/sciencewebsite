<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SDG 6 — Life Before Water</title>
  <meta name="description" content="One-page site about Sustainable Development Goal 6: Life Before Water." />
  <style>
    html{scroll-behavior:smooth}
    body{margin:0;font-family:sans-serif;background:#0b1215;color:#e7f5ff}
    header{position:sticky;top:0;background:#0f1a1f;padding:10px 20px;z-index:10}
    nav ul{margin:0;padding:0;display:flex;list-style:none;gap:10px;flex-wrap:wrap}
    nav a{color:#a9c6d6;text-decoration:none;padding:8px 12px;border-radius:8px}
    nav a:hover,nav a.active{background:#38bdf8;color:#001018}
    section{padding:80px 20px;max-width:1000px;margin:auto}
    h1,h2{color:#38bdf8}
    .hero{padding:120px 20px 80px;background:radial-gradient(circle at top,#14212a,#0b1215)}
    footer{background:#0f1a1f;color:#a9c6d6;padding:40px 20px;text-align:center}
    .card{background:rgba(255,255,255,.05);padding:20px;border-radius:12px;margin-bottom:16px}
  </style>
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#home" class="active">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#challenges">Challenges</a></li>
        <li><a href="#solutions">Solutions</a></li>
        <li><a href="#cases">Case Studies</a></li>
        <li><a href="#resources">Resources</a></li>
      </ul>
    </nav>
  </header>

  <section id="home" class="hero">
    <h1>Life Before Water</h1>
    <p>
      Imagine a world where water is scarce, rivers are dry, and life struggles to exist.
      “Life Before Water” highlights the importance of water as the foundation of all living systems,
      reminding us how fragile life would be without it.
    </p>
  </section>

  <section id="about">
    <h2>About</h2>
    <p>
      Water sustains every organism on Earth. This section explores what happens when we
      imagine life before water — barren landscapes, lifeless ecosystems, and the absence of growth.
      Understanding this helps us value and protect water resources for all living beings.
    </p>
  </section>

  <section id="challenges">
    <h2>Challenges</h2>
    <div class="card">
      <h3>Scarcity</h3>
      <p>Regions face drought and depletion of groundwater, threatening human and ecological survival.</p>
    </div>
    <div class="card">
      <h3>Pollution</h3>
      <p>Contamination from industries, waste, and chemicals makes clean water harder to access.</p>
    </div>
    <div class="card">
      <h3>Inequality</h3>
      <p>Billions still lack access to safe water and sanitation, deepening global disparities.</p>
    </div>
  </section>

  <section id="solutions">
    <h2>Solutions</h2>
    <p>
      To avoid returning to a “life before water,” we must preserve and restore our water systems.
      Conservation, innovation, and education are key to sustainable management.
    </p>
    <ul>
      <li>Protect rivers, lakes, and groundwater.</li>
      <li>Use water efficiently in homes, farms, and industries.</li>
      <li>Adopt renewable energy and nature-based water treatment.</li>
      <li>Reduce pollution and strengthen global cooperation.</li>
    </ul>
  </section>

  <section id="cases">
    <h2>Case Studies</h2>
    <div class="card">
      <h3>Wetland Restoration</h3>
      <p>Communities restored natural wetlands to filter water and revive biodiversity.</p>
    </div>
    <div class="card">
      <h3>Urban Water Recycling</h3>
      <p>Cities reuse treated wastewater for irrigation and green spaces, reducing scarcity.</p>
    </div>
  </section>

  <section id="resources">
    <h2>Resources</h2>
    <ul>
      <li><a href="https://sdgs.un.org/goals/goal6" target="_blank">UN SDG 6 Overview</a></li>
      <li><a href="https://www.unicef.org/wash" target="_blank">UNICEF — WASH Initiatives</a></li>
      <li><a href="https://www.who.int/teams/environment-climate-change-and-health/water-sanitation-and-health" target="_blank">WHO Water and Health</a></li>
    </ul>
  </section>

  <footer>
    <p><strong>Life Before Water</strong> — Awareness for Sustainable Water Use</p>
  </footer>

  <script>
    // Smooth scroll and active nav highlighting
    const sections=[...document.querySelectorAll('section')];
    const links=[...document.querySelectorAll('nav a')];
    window.addEventListener('scroll',()=>{
      let fromTop=window.scrollY+200;
      sections.forEach(sec=>{
        if(sec.offsetTop<=fromTop && sec.offsetTop+sec.offsetHeight>fromTop){
          links.forEach(a=>a.classList.remove('active'));
          const link=document.querySelector('a[href="#'+sec.id+'"]');
          if(link)link.classList.add('active');
        }
      });
    });
  </script>
</body>
</html>
