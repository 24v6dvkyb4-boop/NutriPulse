<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NutriPulse — Coach Sport & Nutrition Intelligent</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    font-family: 'Segoe UI', Arial, sans-serif;
    background: #0d0d0d;
    color: #fff;
    line-height: 1.6;
  }
  a { text-decoration: none; }

  /* NAVBAR */
  nav {
    display: flex; justify-content: space-between; align-items: center;
    padding: 18px 40px; background: #0d0d0d; position: sticky; top: 0; z-index: 10;
    border-bottom: 1px solid #1f3d1f;
  }
  .nav-brand { display: flex; align-items: center; gap: 10px; }
  .nav-brand svg { width: 32px; height: 32px; filter: drop-shadow(0 0 6px #39ff14); }
  .logo {
    font-size: 24px; font-weight: 800; color: #39ff14;
    letter-spacing: 1px; text-shadow: 0 0 12px #39ff14;
  }
  nav ul { display: flex; gap: 28px; list-style: none; }
  nav ul li a { color: #cfd8cf; font-weight: 600; font-size: 15px; transition: color 0.2s; }
  nav ul li a:hover { color: #39ff14; }
  .btn-nav {
    background: #39ff14; color: #0d0d0d; padding: 10px 22px;
    border-radius: 30px; font-weight: 800; font-size: 14px;
    box-shadow: 0 0 15px rgba(57,255,20,0.4);
  }

  /* HERO */
  .hero {
    display: flex; align-items: center; justify-content: space-between; gap: 40px;
    padding: 90px 40px; flex-wrap: wrap; text-align: left;
    background: radial-gradient(circle at 80% 20%, #122512 0%, #0d0d0d 60%);
  }
  .hero-text { flex: 1; min-width: 280px; }
  .hero-text h1 {
    font-size: 54px; line-height: 1.1; margin-bottom: 20px;
    color: #39ff14; text-shadow: 0 0 25px rgba(57,255,20,0.6);
  }
  .hero-text p { font-size: 18px; color: #b8c9bf; margin-bottom: 30px; max-width: 480px; }
  .hero-buttons { display: flex; gap: 15px; flex-wrap: wrap; }
  .btn-primary {
    background: #39ff14; color: #0d0d0d; padding: 15px 32px;
    border-radius: 40px; font-weight: 800; font-size: 16px;
    box-shadow: 0 0 20px rgba(57,255,20,0.4);
  }
  .btn-secondary {
    background: transparent; color: #39ff14; border: 2px solid #39ff14;
    padding: 13px 30px; border-radius: 40px; font-weight: 700; font-size: 16px;
  }
  .hero-img { flex: 1; min-width: 260px; display: flex; justify-content: center; }
  .hero-circle {
    width: 320px; height: 320px; border-radius: 50%;
    border: 2px solid #39ff14;
    box-shadow: 0 0 40px rgba(57,255,20,0.4), inset 0 0 40px rgba(57,255,20,0.15);
    display: flex; align-items: center; justify-content: center;
    background: radial-gradient(circle, rgba(57,255,20,0.08) 0%, transparent 70%);
  }
  .hero-circle svg { width: 170px; height: 170px; filter: drop-shadow(0 0 15px #39ff14); }

  /* STATS */
  .stats {
    display: flex; justify-content: space-around; flex-wrap: wrap;
    padding: 50px 40px; background: #111; gap: 20px;
    border-top: 1px solid #1f3d1f; border-bottom: 1px solid #1f3d1f;
  }
  .stat { text-align: center; }
  .stat h3 { font-size: 38px; color: #39ff14; text-shadow: 0 0 15px rgba(57,255,20,0.5); }
  .stat p { color: #8fa394; font-weight: 600; }

  /* SECTIONS */
  section { padding: 80px 40px; }
  .section-title { text-align: center; margin-bottom: 50px; }
  .section-title h2 { font-size: 38px; color: #39ff14; margin-bottom: 10px; text-shadow: 0 0 15px rgba(57,255,20,0.4); }
  .section-title p { color: #8fa394; font-size: 17px; }

  /* CARDS */
  .cards { display: flex; gap: 25px; justify-content: center; flex-wrap: wrap; }
  .card {
    background: #141414; border: 1px solid #2a5c2a; border-radius: 18px;
    padding: 35px 25px; width: 280px; text-align: center;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .card:hover {
    transform: translateY(-6px);
    box-shadow: 0 0 25px rgba(57,255,20,0.25);
    border-color: #39ff14;
  }
  .card .icon { font-size: 50px; margin-bottom: 15px; }
  .card h3 { font-size: 22px; margin-bottom: 10px; color: #fff; }
  .card p { color: #8fa394; font-size: 15px; }
  .card .tag {
    display: inline-block; margin-top: 15px;
    background: rgba(57,255,20,0.12); color: #39ff14;
    padding: 6px 16px; border-radius: 20px; font-size: 13px; font-weight: 700;
    border: 1px solid #39ff14;
  }

  /* NUTRITION */
  .nutrition { background: #0a1a0a; }

  /* TÉMOIGNAGES */
  .testimonials { background: #111; }
  .testi {
    background: #141414; border: 1px solid #2a5c2a; border-radius: 16px;
    padding: 30px; width: 300px;
  }
  .testi p { font-style: italic; color: #b8c9bf; margin-bottom: 15px; }
  .testi strong { color: #39ff14; }

  /* CTA */
  .cta {
    text-align: center; background: linear-gradient(135deg, #0a1a0a, #142b14);
    border: 1px solid #39ff14; border-radius: 20px;
    margin: 0 40px 80px; padding: 60px 30px;
    box-shadow: 0 0 40px rgba(57,255,20,0.15);
  }
  .cta h2 { font-size: 36px; margin-bottom: 15px; color: #39ff14; text-shadow: 0 0 15px rgba(57,255,20,0.4); }
  .cta p { font-size: 17px; margin-bottom: 25px; color: #b8c9bf; }
  .cta a {
    background: #39ff14; color: #0d0d0d; padding: 15px 40px;
    border-radius: 40px; font-weight: 800; font-size: 16px;
    box-shadow: 0 0 20px rgba(57,255,20,0.4);
  }

  /* FOOTER */
  footer { background: #050505; color: #8fa394; padding: 50px 40px 25px; border-top: 1px solid #1f3d1f; }
  .footer-grid { display: flex; justify-content: space-between; flex-wrap: wrap; gap: 30px; margin-bottom: 30px; text-align: left; }
  .footer-grid h4 { color: #fff; margin-bottom: 12px; font-size: 16px; }
  .footer-grid a { display: block; color: #8fa394; font-size: 14px; margin-bottom: 6px; }
  .footer-grid a:hover { color: #39ff14; }
  .footer-bottom { text-align: center; border-top: 1px solid #1f3d1f; padding-top: 20px; font-size: 13px; }

  @media (max-width: 700px) {
    nav ul { display: none; }
    .hero { text-align: center; }
    .hero-text h1 { font-size: 36px; }
    .hero-buttons { justify-content: center; }
    .hero-circle { width: 240px; height: 240px; }
    .hero-circle svg { width: 130px; height: 130px; }
  }
</style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <div class="nav-brand">
    <!-- LOGO SVG : haltère néon -->
    <svg viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">
      <rect x="4" y="26" width="8" height="12" rx="2" stroke="#39ff14" stroke-width="3"/>
      <rect x="52" y="26" width="8" height="12" rx="2" stroke="#39ff14" stroke-width="3"/>
      <rect x="14" y="22" width="10" height="20" rx="3" stroke="#39ff14" stroke-width="3"/>
      <rect x="40" y="22" width="10" height="20" rx="3" stroke="#39ff14" stroke-width="3"/>
      <line x1="24" y1="32" x2="40" y2="32" stroke="#39ff14" stroke-width="3" stroke-linecap="round"/>
    </svg>
    <div class="logo">NutriPulse</div>
  </div>
  <ul>
    <li><a href="#">Accueil</a></li>
    <li><a href="#">Exercices</a></li>
    <li><a href="#">Nutrition</a></li>
    <li><a href="#">Témoignages</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
  <a href="#" class="btn-nav">Commencer</a>
</nav>

<!-- HERO -->
<header class="hero">
  <div class="hero-text">
    <h1>Ton coach sport & nutrition intelligent</h1>
    <p>NutriPulse t'accompagne chaque jour avec des programmes d'exercices adaptés et des conseils nutrition pour un équilibre sain et durable.</p>
    <div class="hero-buttons">
      <a href="#" class="btn-primary">Commencer gratuitement</a>
      <a href="#" class="btn-secondary">Voir les programmes</a>
    </div>
  </div>
  <div class="hero-img">
    <div class="hero-circle">
      <!-- Même logo haltère, en plus grand -->
      <svg viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="4" y="26" width="8" height="12" rx="2" stroke="#39ff14" stroke-width="3"/>
        <rect x="52" y="26" width="8" height="12" rx="2" stroke="#39ff14" stroke-width="3"/>
        <rect x="14" y="22" width="10" height="20" rx="3" stroke="#39ff14" stroke-width="3"/>
        <rect x="40" y="22" width="10" height="20" rx="3" stroke="#39ff14" stroke-width="3"/>
        <line x1="24" y1="32" x2="40" y2="32" stroke="#39ff14" stroke-width="3" stroke-linecap="round"/>
      </svg>
    </div>
  </div>
</header>

<!-- STATS -->
<div class="stats">
  <div class="stat"><h3>10k+</h3><p>Membres actifs</p></div>
  <div class="stat"><h3>250+</h3><p>Programmes sport</p></div>
  <div class="stat"><h3>500+</h3><p>Recettes saines</p></div>
  <div class="stat"><h3>4.9★</h3><p>Note moyenne</p></div>
</div>

<!-- EXERCICES -->
<section>
  <div class="section-title">
    <h2>Nos programmes d'exercices</h2>
    <p>Des séances adaptées à ton niveau et à tes objectifs</p>
  </div>
  <div class="cards">
    <div class="card">
      <div class="icon">💪</div>
      <h3>Renforcement</h3>
      <p>Gagne en force et en muscles avec des séances progressives.</p>
      <span class="tag">Débutant → Avancé</span>
    </div>
    <div class="card">
      <div class="icon">🏃</div>
      <h3>Cardio</h3>
      <p>Améliore ton endurance et brûle des calories efficacement.</p>
      <span class="tag">20-40 min</span>
    </div>
    <div class="card">
      <div class="icon">🧘</div>
      <h3>Bien-être</h3>
      <p>Yoga, stretching et récupération pour un corps équilibré.</p>
      <span class="tag">Doux & relaxant</span>
    </div>
  </div>
</section>

<!-- NUTRITION -->
<section class="nutrition">
  <div class="section-title">
    <h2>Mange sain, mange équilibré</h2>
    <p>Des repas simples et savoureux pour soutenir tes efforts</p>
  </div>
  <div class="cards">
    <div class="card">
      <div class="icon">🥗</div>
      <h3>Repas équilibrés</h3>
      <p>Des recettes riches en protéines, fibres et bons nutriments.</p>
      <span class="tag">500+ recettes</span>
    </div>
    <div class="card">
      <div class="icon">📊</div>
      <h3>Suivi nutrition</h3>
      <p>Suis tes calories et macros facilement au quotidien.</p>
      <span class="tag">Macros & calories</span>
    </div>
    <div class="card">
      <div class="icon">🍎</div>
      <h3>Conseils healthy</h3>
      <p>Des astuces pour mieux manger sans te priver.</p>
      <span class="tag">Astuces du jour</span>
    </div>
  </div>
</section>

<!-- TÉMOIGNAGES -->
<section class="testimonials">
  <div class="section-title">
    <h2>Ils ont changé leur quotidien</h2>
    <p>Des résultats concrets, une vraie motivation</p>
  </div>
  <div class="cards">
    <div class="testi">
      <p>"Grâce à NutriPulse, j'ai enfin trouvé un équilibre entre sport et alimentation. Je me sens mieux dans mon corps."</p>
      <strong>— Sarah, 28 ans</strong>
    </div>
    <div class="testi">
      <p>"Les programmes sont clairs et les recettes délicieuses. J'ai perdu 5 kg sans me priver."</p>
      <strong>— Thomas, 34 ans</strong>
    </div>
    <div class="testi">
      <p>"Le suivi nutrition m'aide à comprendre ce que je mange. C'est devenu un réflexe quotidien."</p>
      <strong>— Léa, 22 ans</strong>
    </div>
  </div>
</section>

<!-- CTA -->
<div class="cta">
  <h2>Prêt à commencer ton équilibre ?</h2>
  <p>Rejoins des milliers de personnes qui prennent soin d'elles avec NutriPulse.</p>
  <a href="#">Créer mon compte gratuit</a>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div>
      <div class="nav-brand" style="margin-bottom:10px;">
        <svg viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg" style="width:28px;height:28px;filter:drop-shadow(0 0 6px #39ff14);">
          <rect x="4" y="26" width="8" height="12" rx="2" stroke="#39ff14" stroke-width="3"/>
          <rect x="52" y="26" width="8" height="12" rx="2" stroke="#39ff14" stroke-width="3"/>
          <rect x="14" y="22" width="10" height="20" rx="3" stroke="#39ff14" stroke-width="3"/>
          <rect x="40" y="22" width="10" height="20" rx="3" stroke="#39ff14" stroke-width="3"/>
          <line x1="24" y1="32" x2="40" y2="32" stroke="#39ff14" stroke-width="3" stroke-linecap="round"/>
        </svg>
        <div class="logo" style="font-size:20px;">NutriPulse</div>
      </div>
      <p style="font-size:14px; max-width:250px;">Ton coach sport & nutrition intelligent, chaque jour.</p>
    </div>
    <div>
      <h4>Navigation</h4>
      <a href="#">Accueil</a>
      <a href="#">Exercices</a>
      <a href="#">Nutrition</a>
      <a href="#">Témoignages</a>
    </div>
    <div>
      <h4>Ressources</h4>
      <a href="#">Blog</a>
      <a href="#">Recettes</a>
      <a href="#">FAQ</a>
      <a href="#">Contact</a>
    </div>
    <div>
      <h4>Suis-nous</h4>
      <a href="#">Instagram</a>
      <a href="#">TikTok</a>
      <a href="#">YouTube</a>
    </div>
  </div>
  <div class="footer-bottom">© 2025 NutriPulse. Tous droits réservés.</div>
</footer>

</body>
</html># NutriPulse
