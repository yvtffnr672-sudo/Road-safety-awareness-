# Road-safety-awareness-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Safe Roads | Road Safety Awareness</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      background: #f7f7f7;
      color: #222;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* Header / Nav */
    header {
      background: #111827;
      color: #fff;
      padding: 0.8rem 1.5rem;
      position: sticky;
      top: 0;
      z-index: 999;
    }

    .nav {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-weight: 700;
      letter-spacing: 0.05em;
    }

    .logo-icon {
      width: 32px;
      height: 32px;
      border-radius: 50%;
      background: linear-gradient(135deg, #22c55e, #facc15, #ef4444);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.7rem;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1rem;
      font-size: 0.9rem;
    }

    nav li a:hover {
      text-decoration: underline;
    }

    /* Hero */
    .hero {
      background: linear-gradient(135deg, #fee2e2, #e0f2fe);
      padding: 3.5rem 1.5rem;
    }

    .hero-inner {
      max-width: 1100px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 2rem;
      align-items: center;
    }

    .hero h1 {
      font-size: 2.4rem;
      margin-bottom: 0.75rem;
      color: #111827;
    }

    .hero p {
      font-size: 1rem;
      margin-bottom: 1.5rem;
      color: #374151;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }

    .btn-primary {
      background: #111827;
      color: #fff;
      border-radius: 999px;
      padding: 0.65rem 1.4rem;
      font-size: 0.95rem;
      border: none;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
    }

    .btn-secondary {
      background: #fff;
      color: #111827;
      border-radius: 999px;
      padding: 0.6rem 1.3rem;
      font-size: 0.9rem;
      border: 1px solid #d1d5db;
      cursor: pointer;
    }

    .hero-tagline {
      margin-top: 0.75rem;
      font-size: 0.85rem;
      color: #6b7280;
    }

    .hero-card {
      background: #fff;
      border-radius: 1rem;
      box-shadow: 0 10px 30px rgba(15, 23, 42, 0.12);
      padding: 1.3rem 1.3rem 1.1rem;
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
    }

    .hero-card-title {
      font-weight: 600;
      font-size: 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .traffic-light {
      display: flex;
      flex-direction: column;
      gap: 0.2rem;
      padding: 0.4rem;
      background: #111827;
      border-radius: 999px;
    }

    .traffic-light span {
      width: 10px;
      height: 10px;
      border-radius: 999px;
    }

    .light-red { background: #ef4444; }
    .light-amber { background: #facc15; }
    .light-green { background: #22c55e; }

    .hero-card ul {
      list-style: none;
      font-size: 0.9rem;
      color: #374151;
    }

    .hero-card ul li::before {
      content: "• ";
      color: #22c55e;
      font-weight: 700;
    }

    /* Sections */
    section {
      padding: 2.5rem 1.5rem;
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
    }

    h2.section-title {
      font-size: 1.6rem;
      margin-bottom: 0.5rem;
      color: #111827;
    }

    .section-subtitle {
      font-size: 0.95rem;
      color: #6b7280;
      margin-bottom: 1.8rem;
    }

    /* About */
    .about-text {
      font-size: 1rem;
      color: #374151;
      max-width: 750px;
    }

    /* Tips grid */
    .tips-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.2rem;
    }

    .tip-card {
      background: #fff;
      border-radius: 0.9rem;
      padding: 1.1rem 1rem;
      border: 1px solid #e5e7eb;
      box-shadow: 0 8px 20px rgba(15, 23, 42, 0.04);
    }

    .tip-label {
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      margin-bottom: 0.3rem;
    }

    .tip-title {
      font-size: 1rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .tip-card ul {
      list-style: disc inside;
      font-size: 0.9rem;
      color: #4b5563;
    }

    .tip-drive .tip-label { color: #92400e; }
    .tip-protect .tip-label { color: #b91c1c; }
    .tip-pedestrians .tip-label { color: #166534; }

    /* Video section */
    .video-placeholder {
      margin-top: 1rem;
      background: #0f172a;
      border-radius: 1rem;
      padding: 1.2rem;
      color: #e5e7eb;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .video-text h3 {
      font-size: 1.1rem;
      margin-bottom: 0.2rem;
    }

    .video-text p {
      font-size: 0.9rem;
      color: #9ca3af;
    }

    .video-box {
      width: 260px;
      height: 150px;
      border-radius: 0.7rem;
      border: 2px dashed #6b7280;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.9rem;
      color: #9ca3af;
    }

    /* Social section */
    .social-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-bottom: 1rem;
    }

    .social-pill {
      background: #fff;
      border-radius: 999px;
      padding: 0.5rem 1rem;
      border: 1px solid #e5e7eb;
      font-size: 0.9rem;
    }

    .hashtag-list {
      font-size: 0.9rem;
      color: #4b5563;
    }

    /* Footer */
    footer {
      background: #111827;
      color: #9ca3af;
      padding: 1.5rem 1.5rem 1.8rem;
      font-size: 0.85rem;
    }

    footer .footer-inner {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 0.75rem;
      align-items: center;
    }

    footer a {
      color: #e5e7eb;
      text-decoration: underline;
    }

    /* Responsive */
    @media (max-width: 800px) {
      .hero-inner {
        grid-template-columns: minmax(0, 1fr);
      }

      .tips-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      nav ul {
        display: none; /* simple mobile nav – can be expanded later */
      }

      .hero h1 {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <header>
    <div class="nav">
      <div class="logo">
        <div class="logo-icon">SR</div>
        <span>Safe Roads</span>
      </div>
      <nav>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#tips">Safety Tips</a></li>
          <li><a href="#video">Video</a></li>
          <li><a href="#social">Social</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <div>
        <h1>Stay Alert. Stay Safe. Every Life Matters.</h1>
        <p>
          Safe Roads is a student-led campaign that spreads road safety
          awareness through simple tips, short videos, and social media.
          A small action today can prevent a serious accident tomorrow.
        </p>
        <div class="hero-buttons">
          <button class="btn-primary" onclick="document.getElementById('tips').scrollIntoView({behavior:'smooth'})">
            Explore Safety Tips →
          </button>
          <button class="btn-secondary" onclick="document.getElementById('video').scrollIntoView({behavior:'smooth'})">
            Watch Awareness Video
          </button>
        </div>
        <p class="hero-tagline">🚦 Drive responsibly • Protect yourself • Respect others on the road</p>
      </div>

      <aside class="hero-card" aria-label="Quick road safety checklist">
        <div class="hero-card-title">
          <div class="traffic-light" aria-hidden="true">
            <span class="light-red"></span>
            <span class="light-amber"></span>
            <span class="light-green"></span>
          </div>
          <span>Quick Road Safety Checklist</span>
        </div>
        <ul>
          <li>Wear your seatbelt before the car starts moving.</li>
          <li>Keep your eyes on the road, not on your phone.</li>
          <li>Slow down near schools and crosswalks.</li>
          <li>Follow traffic lights and road signs at all times.</li>
        </ul>
      </aside>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="container">
      <h2 class="section-title">About the Campaign</h2>
      <p class="section-subtitle">Why road safety matters.</p>
      <p class="about-text">
        Every year, thousands of people are injured or killed in preventable road
        accidents. Our goal is to build a culture where safe driving, wearing
        seatbelts, and respecting pedestrians are normal habits for everyone.
        We use simple designs, short videos, and social media posts to reach
        young drivers and students in a clear and friendly way.
      </p>
    </div>
  </section>

  <!-- SAFETY TIPS -->
  <section id="tips">
    <div class="container">
      <h2 class="section-title">Key Safety Tips</h2>
      <p class="section-subtitle">Three simple areas that make a big difference.</p>

      <div class="tips-grid">
        <div class="tip-card tip-drive">
          <p class="tip-label">Drive Safely</p>
          <p class="tip-title">Control your speed.</p>
          <ul>
            <li>Obey speed limits in all areas.</li>
            <li>Keep a safe distance from the car in front.</li>
            <li>Use indicators when turning or changing lanes.</li>
          </ul>
        </div>

        <div class="tip-card tip-protect">
          <p class="tip-label">Protect Yourself</p>
          <p class="tip-title">Think of your safety first.</p>
          <ul>
            <li>Always wear your seatbelt, even on short trips.</li>
            <li>Check mirrors and blind spots regularly.</li>
            <li>Never text or scroll on your phone while driving.</li>
          </ul>
        </div>

        <div class="tip-card tip-pedestrians">
          <p class="tip-label">Respect Pedestrians</p>
          <p class="tip-title">Share the road with care.</p>
          <ul>
            <li>Stop fully at zebra crossings.</li>
            <li>Slow down near schools, bus stops, and neighborhoods.</li>
            <li>Give pedestrians and cyclists extra space.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- VIDEO PLACEHOLDER -->
  <section id="video">
    <div class="container">
      <h2 class="section-title">Awareness Video</h2>
      <p class="section-subtitle">
        Add your Canva, Instagram, or TikTok road safety video here.
      </p>

      <div class="video-placeholder">
        <div class="video-text">
          <h3>“Road Safety Starts With You”</h3>
          <p>
            Create a 20–30 second video in Canva using the same colours and
            tips from this page. Then embed it here as an iframe or link.
          </p>
        </div>
        <div class="video-box">
          <!-- Replace this entire box with an iframe or video tag if you have one -->
          Video coming soon – paste your embed code here.
        </div>
      </div>
    </div>
  </section>

  <!-- SOCIAL / CONTACT -->
  <section id="social">
    <div class="container">
      <h2 class="section-title">Follow & Share</h2>
      <p class="section-subtitle">
        Help us spread the message on social media.
      </p>

      <div class="social-links">
        <div class="social-pill">Instagram: <strong>@SafeRoadsAwareness</strong></div>
        <div class="social-pill">TikTok: <strong>@SafeRoadsClips</strong></div>
        <div class="social-pill">YouTube: <strong>Safe Roads Campaign</strong></div>
      </div>

      <p class="hashtag-list">
        Use these hashtags in your posts:<br />
        <strong>#RoadSafety #DriveSafe #SeatbeltFirst #RespectPedestrians #SaveLives</strong>
      </p>
    </div>
  </section>

  <section id="contact">
    <div class="container">
      <h2 class="section-title">Contact</h2>
      <p class="section-subtitle">
        For collaborations, school events, or ideas, get in touch.
      </p>
      <p class="about-text">
        📧 Email: <a href="mailto:info@saferoads.example">info@saferoads.example</a><br />
        🏫 Organization: Safe Roads Awareness Campaign
      </p>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="footer-inner">
      <span>© 2025 Safe Roads Awareness Campaign. All rights reserved.</span>
      <span>Designed for a school road safety project.</span>
    </div>
  </footer>

</body>
</html>
