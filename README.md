<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Luxury Beauty | Glassmorphism Edition</title>

<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600&family=Jost:wght@200;300;400;500&display=swap" rel="stylesheet">

<style>
:root {
  /* 💜 GLASS PURPLE SYSTEM */
  --purple: #8B5CF6;
  --purple-soft: rgba(139,92,246,.25);
  --purple-glow: rgba(139,92,246,.35);

  --glass: rgba(255,255,255,.06);
  --glass-strong: rgba(255,255,255,.1);

  --border: rgba(139,92,246,.25);

  --black: #07070A;
  --text: #F5F0E8;

  --blur: blur(18px);

  --font-display: 'Cormorant Garamond', serif;
  --font-body: 'Jost', sans-serif;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background:
    radial-gradient(circle at 20% 20%, rgba(139,92,246,.25), transparent 40%),
    radial-gradient(circle at 80% 60%, rgba(168,85,247,.18), transparent 45%),
    var(--black);
  color: var(--text);
  font-family: var(--font-body);
  overflow-x: hidden;
}

/* 🌫️ GLASS NAV */
nav {
  position: fixed;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  width: 92%;
  padding: 14px 24px;

  display: flex;
  justify-content: space-between;
  align-items: center;

  background: var(--glass);
  backdrop-filter: var(--blur);
  border: 1px solid var(--border);
  border-radius: 18px;

  box-shadow: 0 10px 40px rgba(0,0,0,.4);
}

.logo-icon {
  width: 38px;
  height: 38px;
  border-radius: 50%;
  display: grid;
  place-items: center;

  background: var(--glass-strong);
  backdrop-filter: var(--blur);

  border: 1px solid var(--border);
  box-shadow: 0 0 25px var(--purple-glow);
}

/* 🌌 HERO */
#hero {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  padding: 40px;
}

.hero-card {
  width: min(900px, 92%);
  padding: 60px;

  background: var(--glass);
  backdrop-filter: var(--blur);

  border: 1px solid var(--border);
  border-radius: 28px;

  box-shadow:
    0 20px 60px rgba(0,0,0,.5),
    inset 0 1px 0 rgba(255,255,255,.08);

  text-align: center;
}

.hero-eyebrow {
  color: var(--purple);
  letter-spacing: .35em;
  font-size: .75rem;
  text-transform: uppercase;
  margin-bottom: 20px;
}

.hero-title {
  font-family: var(--font-display);
  font-size: clamp(2.8rem, 6vw, 5.5rem);
  font-weight: 300;
  line-height: 1;
}

.hero-title em {
  color: var(--purple);
  font-style: italic;
  text-shadow: 0 0 20px var(--purple-glow);
}

.hero-sub {
  margin-top: 18px;
  opacity: .7;
  line-height: 1.8;
}

/* 💜 BUTTONS */
.btn {
  margin-top: 30px;
  padding: 14px 34px;

  border-radius: 14px;
  border: 1px solid var(--border);

  background: var(--glass);
  backdrop-filter: var(--blur);

  color: var(--text);
  letter-spacing: .2em;
  text-transform: uppercase;

  cursor: pointer;
  transition: .3s;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 0 25px var(--purple-glow);
  border-color: var(--purple);
}

/* 🧊 GLASS CARDS GRID */
.section {
  padding: 100px 40px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.card {
  padding: 24px;

  background: var(--glass);
  backdrop-filter: var(--blur);

  border: 1px solid var(--border);
  border-radius: 20px;

  transition: .4s;
  position: relative;
  overflow: hidden;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 60px rgba(139,92,246,.15);
  border-color: var(--purple);
}

.card::before {
  content: "";
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at top left, var(--purple-soft), transparent 60%);
  opacity: 0;
  transition: .4s;
}

.card:hover::before {
  opacity: 1;
}

.card h3 {
  font-family: var(--font-display);
  font-size: 1.5rem;
}

.card p {
  opacity: .7;
  margin-top: 10px;
  line-height: 1.6;
}

/* 🌫️ FLOATING GLASS ORBS */
.orb {
  position: absolute;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, var(--purple-glow), transparent 60%);
  filter: blur(60px);
  opacity: .4;
}

.orb.one { top: 10%; left: 10%; }
.orb.two { bottom: 10%; right: 10%; }

/* 📱 MOBILE */
@media (max-width: 900px) {
  .grid {
    grid-template-columns: 1fr;
  }

  .hero-card {
    padding: 40px 24px;
  }
}
</style>
</head>

<body>

<!-- floating glow -->
<div class="orb one"></div>
<div class="orb two"></div>

<!-- NAV -->
<nav>
  <div class="logo-icon">
    <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#8B5CF6">
      <path d="M12 2C8 2 5 5 5 9c0 5 7 13 7 13s7-8 7-13c0-4-3-7-7-7z"/>
    </svg>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-card">
    <div class="hero-eyebrow">Premium Glass Beauty Studio</div>

    <h1 class="hero-title">
      Where <em>Beauty</em><br>Feels Digital Luxury
    </h1>

    <p class="hero-sub">
      A modern beauty experience built with glass, light, and precision.
    </p>

    <button class="btn">Book Appointment</button>
  </div>
</section>

<!-- SERVICES -->
<section class="section">
  <div class="grid">

    <div class="card">
      <h3>Hair Styling</h3>
      <p>Soft, elegant styling crafted for modern beauty expression.</p>
    </div>

    <div class="card">
      <h3>Makeup</h3>
      <p>Flawless glam with premium glass-light finish aesthetics.</p>
    </div>

    <div class="card">
      <h3>Lash Extensions</h3>
      <p>Lightweight volume lashes designed for soft luxury looks.</p>
    </div>

  </div>
</section>

</body>
</html>
