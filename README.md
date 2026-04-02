<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Mahi Patel | Developer Portfolio</title>
  <!-- Google Fonts: Space Grotesk & Inter for clean modern look -->
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (free icons) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #0a0f1e 0%, #0c1222 100%);
      font-family: 'Inter', 'Space Grotesk', sans-serif;
      color: #eef5ff;
      overflow-x: hidden;
      scroll-behavior: smooth;
    }

    /* custom scrollbar */
    ::-webkit-scrollbar {
      width: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #111827;
    }
    ::-webkit-scrollbar-thumb {
      background: #38bdf8;
      border-radius: 10px;
    }

    /* main container */
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* ========= ANIMATED NAME HERO ========= */
    .hero-name {
      text-align: center;
      margin-top: 40px;
      margin-bottom: 20px;
    }
    .glow-name {
      font-family: 'Space Grotesk', monospace;
      font-size: 4.5rem;
      font-weight: 800;
      background: linear-gradient(135deg, #c084fc, #60a5fa, #38bdf8, #34d399);
      background-size: 300% 300%;
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      animation: gradientFlow 5s ease infinite, textGlow 2s ease-in-out infinite alternate;
      letter-spacing: -0.02em;
      display: inline-block;
      text-shadow: 0 0 12px rgba(56,189,248,0.3);
    }
    @keyframes gradientFlow {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
    @keyframes textGlow {
      0% { text-shadow: 0 0 2px rgba(56,189,248,0.2);}
      100% { text-shadow: 0 0 20px rgba(56,189,248,0.6), 0 0 5px #a855f7;}
    }
    .typed-sub {
      font-size: 1.4rem;
      margin-top: 12px;
      font-weight: 500;
      color: #a5f3fc;
      background: rgba(15, 23, 42, 0.7);
      display: inline-block;
      padding: 8px 24px;
      border-radius: 60px;
      backdrop-filter: blur(4px);
      letter-spacing: 0.5px;
    }

    /* Summary block */
    .summary-card {
      background: rgba(17, 24, 39, 0.65);
      backdrop-filter: blur(12px);
      border-radius: 2rem;
      border: 1px solid rgba(56, 189, 248, 0.25);
      padding: 28px 32px;
      margin: 30px 0;
      transition: transform 0.2s ease, box-shadow 0.2s;
      box-shadow: 0 20px 35px -12px rgba(0,0,0,0.5);
    }
    .summary-card:hover {
      transform: translateY(-4px);
      border-color: #38bdf8;
      box-shadow: 0 25px 40px -12px rgba(56,189,248,0.2);
    }
    .summary-title {
      font-size: 1.9rem;
      font-weight: 700;
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 20px;
      border-left: 4px solid #38bdf8;
      padding-left: 20px;
    }
    .summary-title i {
      color: #38bdf8;
      font-size: 2rem;
    }
    .summary-text {
      font-size: 1.08rem;
      line-height: 1.6;
      color: #e2e8f0;
      margin-bottom: 24px;
    }
    .quick-facts {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: space-between;
      margin-top: 16px;
    }
    .fact-badge {
      background: #1e293b;
      padding: 8px 18px;
      border-radius: 40px;
      font-size: 0.9rem;
      font-weight: 500;
      display: flex;
      align-items: center;
      gap: 10px;
      border: 1px solid #334155;
    }
    .fact-badge i {
      color: #38bdf8;
    }

    /* Skills section (stacked layout: frontend, backend, tools) */
    .skills-stack {
      margin: 50px 0 40px;
    }
    .skills-heading {
      text-align: center;
      font-size: 2.3rem;
      font-weight: 700;
      margin-bottom: 40px;
      background: linear-gradient(120deg, #f0f9ff, #bae6fd);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .skill-category {
      background: rgba(15, 23, 42, 0.6);
      backdrop-filter: blur(8px);
      border-radius: 1.8rem;
      padding: 24px 28px;
      margin-bottom: 28px;
      transition: all 0.25s;
      border: 1px solid rgba(56, 189, 248, 0.2);
    }
    .skill-category:hover {
      border-color: #38bdf8;
      background: rgba(21, 32, 56, 0.7);
    }
    .category-header {
      font-size: 1.8rem;
      font-weight: 700;
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      gap: 14px;
      border-bottom: 2px dashed #38bdf8;
      display: inline-block;
      padding-bottom: 6px;
    }
    .category-header i {
      font-size: 1.8rem;
      color: #38bdf8;
    }
    .skills-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      margin-top: 20px;
    }
    .skill-item {
      background: #0f172a;
      border-radius: 50px;
      padding: 10px 24px;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      font-weight: 500;
      font-size: 1rem;
      transition: 0.2s;
      border: 1px solid #334155;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }
    .skill-item i {
      font-size: 1.3rem;
      color: #60a5fa;
    }
    .skill-item:hover {
      transform: scale(1.03);
      background: #1e2a47;
      border-color: #38bdf8;
    }

    /* GitHub stats cards */
    .github-stats {
      margin: 60px 0 50px;
    }
    .stats-title {
      font-size: 2rem;
      text-align: center;
      margin-bottom: 30px;
      display: flex;
      justify-content: center;
      gap: 12px;
      align-items: baseline;
    }
    .stats-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
    }
    .stat-card {
      background: rgba(0, 0, 0, 0.4);
      backdrop-filter: blur(8px);
      border-radius: 2rem;
      padding: 16px 20px;
      width: 100%;
      max-width: 480px;
      transition: all 0.2s;
      border: 1px solid #2d3a5e;
      text-align: center;
    }
    .stat-card img {
      width: 100%;
      border-radius: 1rem;
      transition: transform 0.2s;
    }
    .stat-card:hover {
      border-color: #38bdf8;
      transform: translateY(-5px);
    }
    /* extra note for dynamic feel */
    .footer-note {
      text-align: center;
      margin: 40px 0 50px;
      padding: 20px;
      font-size: 0.9rem;
      color: #94a3b8;
      border-top: 1px solid #1e293b;
    }

    @media (max-width: 720px) {
      .glow-name { font-size: 2.5rem; }
      .typed-sub { font-size: 1rem; }
      .summary-title { font-size: 1.5rem; }
      .category-header { font-size: 1.4rem; }
      .skills-grid { gap: 12px; }
      .skill-item { padding: 6px 18px; font-size: 0.85rem; }
    }

    /* wave border imitation (subtle) */
    .wave-divider {
      background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 60"><path fill="%2338bdf8" fill-opacity="0.1" d="M0,32L60,37.3C120,43,240,53,360,48C480,43,600,21,720,26.7C840,32,960,64,1080,64C1200,64,1320,32,1380,16L1440,0L1440,60L1380,60C1320,60,1200,60,1080,60C960,60,840,60,720,60C600,60,480,60,360,60C240,60,120,60,60,60L0,60Z"></path></svg>');
      background-repeat: repeat-x;
      height: 20px;
      opacity: 0.5;
      margin: 15px 0;
    }
    a {
      text-decoration: none;
      color: inherit;
    }
  </style>
</head>
<body>

<div class="container">
  <!-- 1. ANIMATED NAME SECTION (first: name animation) -->
  <div class="hero-name">
    <h1 class="glow-name">✦ MAHI PATEL ✦</h1>
    <div class="typed-sub">
      <i class="fas fa-code"></i> Web Developer • C Programmer • Game Dev • Creative Coder
    </div>
    <!-- small waving emoji for style -->
    <div style="margin-top: 12px; font-size: 1.6rem;">👩‍💻 🚀 🌊</div>
  </div>
  
  <div class="wave-divider"></div>

  <!-- 2. SUMMARY (with dynamic fact block) -->
  <div class="summary-card">
    <div class="summary-title">
      <i class="fas fa-user-astronaut"></i> 
      <span>⚡ About the Creator ⚡</span>
    </div>
    <div class="summary-text">
      <strong>Mahi Patel</strong> — 1st year student at <strong>CodingGita, Swaminarayan University</strong> (2nd Semester). 
      I'm obsessed with crafting elegant interfaces, solving logical challenges in C, and exploring the art of game mechanics. 
      I believe in code that's both functional and beautiful. My journey merges fundamentals (C, C++) with modern stacks (React, Node) 
      and a constant drive to build tools that matter. Future Product Manager in AI, currently sharpening my full-stack arsenal.
    </div>
    <div class="quick-facts">
      <div class="fact-badge"><i class="fas fa-map-marker-alt"></i> 📍 Kalol, Gujarat</div>
      <div class="fact-badge"><i class="fas fa-graduation-cap"></i> 🎓 1st Year • 2nd Sem</div>
      <div class="fact-badge"><i class="fas fa-bullseye"></i> 💼 Future PM in AI</div>
      <div class="fact-badge"><i class="fas fa-heart"></i> ⚡ Code. Create. Conquer.</div>
    </div>
  </div>

  <!-- 3. SKILLS IN STACKED MANNER: FRONTEND, BACKEND, TOOLS -->
  <div class="skills-stack">
    <h2 class="skills-heading"><i class="fas fa-layer-group"></i> Tech Arsenal & Skills</h2>
    
    <!-- Frontend Development -->
    <div class="skill-category">
      <div class="category-header">
        <i class="fab fa-react"></i> FRONTEND DEVELOPMENT
      </div>
      <div class="skills-grid">
        <div class="skill-item"><i class="fab fa-html5"></i> HTML5</div>
        <div class="skill-item"><i class="fab fa-css3-alt"></i> CSS3 / Tailwind</div>
        <div class="skill-item"><i class="fab fa-js"></i> JavaScript (ES6+)</div>
        <div class="skill-item"><i class="fab fa-react"></i> React.js</div>
        <div class="skill-item"><i class="fas fa-mobile-alt"></i> Responsive Design</div>
        <div class="skill-item"><i class="fab fa-figma"></i> Figma</div>
        <div class="skill-item"><i class="fas fa-code"></i> Pixel-perfect CSS</div>
      </div>
    </div>

    <!-- Backend & Programming Languages -->
    <div class="skill-category">
      <div class="category-header">
        <i class="fas fa-database"></i> BACKEND & PROGRAMMING
      </div>
      <div class="skills-grid">
        <div class="skill-item"><i class="fas fa-c"></i> C / C++</div>
        <div class="skill-item"><i class="fab fa-python"></i> Python</div>
        <div class="skill-item"><i class="fab fa-node-js"></i> Node.js</div>
        <div class="skill-item"><i class="fas fa-server"></i> Express.js</div>
        <div class="skill-item"><i class="fas fa-database"></i> MongoDB / SQL</div>
        <div class="skill-item"><i class="fas fa-gamepad"></i> Game Logic (C++/SFML)</div>
        <div class="skill-item"><i class="fas fa-microchip"></i> Data Structures & Algo</div>
      </div>
    </div>

    <!-- Tools & Devops / Creative Tools -->
    <div class="skill-category">
      <div class="category-header">
        <i class="fas fa-tools"></i> TOOLS & WORKFLOW
      </div>
      <div class="skills-grid">
        <div class="skill-item"><i class="fab fa-git-alt"></i> Git & GitHub</div>
        <div class="skill-item"><i class="fas fa-terminal"></i> VS Code / Vim</div>
        <div class="skill-item"><i class="fab fa-figma"></i> UI/UX prototyping</div>
        <div class="skill-item"><i class="fas fa-chalkboard-user"></i> Agile / Scrum</div>
        <div class="skill-item"><i class="fas fa-cloud-upload-alt"></i> Vercel / Netlify</div>
        <div class="skill-item"><i class="fas fa-palette"></i> Adobe Creative Suite</div>
        <div class="skill-item"><i class="fas fa-bug"></i> Debugging & Testing</div>
      </div>
    </div>
  </div>

  <!-- 4. GITHUB STATS SECTION (dynamic cards) -->
  <div class="github-stats">
    <div class="stats-title">
      <i class="fab fa-github" style="font-size: 2rem;"></i> 
      <span>📊 GitHub Chronicles</span>
      <i class="fas fa-chart-line"></i>
    </div>
    <div class="stats-grid">
      <!-- GitHub Stats Card -->
      <div class="stat-card">
        <a href="https://github.com/yourusername" target="_blank">
          <img src="https://github-readme-stats.vercel.app/api?username=yourusername&show_icons=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=38BDF8&icon_color=60A5FA&text_color=CBD5E1&ring_color=38BDF8" alt="GitHub Stats" loading="lazy">
        </a>
      </div>
      <!-- Top Languages Card (stacked) -->
      <div class="stat-card">
        <a href="https://github.com/yourusername" target="_blank">
          <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=yourusername&layout=compact&hide_border=true&bg_color=0D1117&title_color=38BDF8&text_color=CBD5E1&langs_count=8" alt="Top Languages">
        </a>
      </div>
    </div>
    <!-- additional streak or trophy? adding extra for completeness -->
    <div style="display: flex; justify-content: center; margin-top: 32px; flex-wrap: wrap; gap: 20px;">
      <div class="stat-card" style="max-width: 380px;">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=yourusername&theme=react&hide_border=true&background=0D1117&stroke=38BDF8&ring=38BDF8&fire=60A5FA&currStreakLabel=38BDF8" alt="GitHub Streak">
      </div>
      <div class="stat-card" style="max-width: 380px;">
        <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=yourusername&theme=2077" alt="Profile summary">
      </div>
    </div>
  </div>

  <!-- call to action / dynamic quote -->
  <div class="wave-divider"></div>
  <div style="text-align: center; margin: 20px 0 30px;">
    <span style="background: #0f172a80; padding: 10px 20px; border-radius: 40px; font-size: 1rem;">
      <i class="fas fa-terminal"></i> “Building the future, one line at a time.” 
    </span>
  </div>

  <!-- FOOTER with subtle animation -->
  <div class="footer-note">
    <i class="fas fa-crown"></i>  Mahi Patel — Product Manager in AI (in the making) 
    <i class="fas fa-heart" style="color:#f472b6;"></i> 
    <br/>
    <span style="font-size: 0.75rem;">⚡ Constantly learning, debugging dreams & shipping creativity</span>
  </div>
</div>

<!-- Additional interactive enhancement: custom cursor or glitter? optional, but makes clean -->
<script>
  // small console greeting and dynamic year effect (cosmetic)
  (function() {
    console.log("%c✨ Mahi Patel Portfolio | Full Stack Developer in progress ✨", "color: #38bdf8; font-size: 16px; font-weight: bold;");
    // make any link hover effect consistent
    const statsImgs = document.querySelectorAll('.stat-card img');
    statsImgs.forEach(img => {
      img.addEventListener('error', () => {
        // fallback if vercel api fails, but mostly works
        if(img.src.includes('github-readme-stats') && img.src.includes('yourusername')) {
          // optional keep as is, user can replace with actual username
        }
      });
    });
    // small floating effect on skill items
    const skillItems = document.querySelectorAll('.skill-item');
    skillItems.forEach(item => {
      item.addEventListener('mouseenter', (e) => {
        item.style.transition = '0.2s';
      });
    });
    // update year in footer optionally
    const footerNote = document.querySelector('.footer-note');
    if(footerNote) {
      let yearSpan = document.createElement('span');
      yearSpan.style.marginLeft = '8px';
      yearSpan.innerHTML = `© ${new Date().getFullYear()} ·`;
      footerNote.prepend(yearSpan);
    }
  })();
</script>

<!-- note: the github stats use "yourusername" as placeholder.
     For real profile, Mahi Patel should replace with actual GitHub username.
     But design remains consistent and functional. -->
</body>
</html>
