<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Gotowe Posiłki – zdrowa dieta i gotowe jadłospisy</title>
<style>
  /* Reset */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #6dd5fa, #2980b9);
    color: #fff;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  header {
    background: rgba(0,0,0,0.4);
    padding: 1.5rem 2rem;
    box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  header h1 {
    font-weight: 700;
    font-size: 2rem;
    color: #f1c40f;
    letter-spacing: 2px;
  }

  nav a {
    color: #f1c40f;
    font-weight: 600;
    margin-left: 1.8rem;
    text-decoration: none;
    font-size: 1.1rem;
    transition: color 0.3s ease;
  }

  nav a:hover {
    color: #ffe066;
  }

  .hero {
    background: url('https://source.unsplash.com/1600x900/?healthy,food') center/cover no-repeat;
    padding: 6rem 2rem 4rem;
    text-align: center;
    position: relative;
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .hero::before {
    content: "";
    position: absolute;
    inset: 0;
    background: rgba(0,0,0,0.5);
    z-index: 1;
    border-radius: 10px;
  }

  .hero-content {
    position: relative;
    z-index: 2;
    max-width: 700px;
    margin: 0 auto;
  }

  .hero h2 {
    font-size: 3rem;
    margin-bottom: 1rem;
    font-weight: 800;
    text-shadow: 0 2px 6px rgba(0,0,0,0.7);
  }

  .hero p {
    font-size: 1.3rem;
    margin-bottom: 2.5rem;
    line-height: 1.5;
    text-shadow: 0 1px 4px rgba(0,0,0,0.6);
  }

  .btn-primary {
    background-color: #f1c40f;
    color: #222;
    font-weight: 700;
    padding: 1.3rem 3rem;
    border-radius: 40px;
    border: none;
    cursor: pointer;
    font-size: 1.3rem;
    box-shadow: 0 6px 15px rgba(241, 196, 15, 0.6);
    text-decoration: none;
    display: inline-block;
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
  }

  .btn-primary:hover {
    background-color: #ffe066;
    box-shadow: 0 8px 20px rgba(255, 224, 102, 0.9);
  }

  section.features {
    background: #fff;
    color: #333;
    padding: 4rem 2rem;
    border-radius: 20px 20px 0 0;
    max-width: 1100px;
    margin: -5rem auto 3rem;
    box-shadow: 0 8px 20px rgba(0,0,0,0.15);
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
  }

  .feature-card {
    background: linear-gradient(135deg, #27ae60, #2ecc71);
    flex: 1 1 280px;
    border-radius: 20px;
    padding: 2rem;
    text-align: center;
    color: white;
    box-shadow: 0 6px 15px rgba(39, 174, 96, 0.5);
    transition: transform 0.3s ease;
    cursor: default;
  }

  .feature-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 12px 30px rgba(39, 174, 96, 0.8);
  }

  .feature-card img {
    width: 90px;
    margin-bottom: 1.5rem;
    border-radius: 50%;
    border: 3px solid rgba(255, 255, 255, 0.6);
    background: rgba(255,255,255,0.15);
  }

  .feature-card h3 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
    font-weight: 700;
  }

  .feature-card p {
    font-size: 1.1rem;
    line-height: 1.4;
  }

  section.cta {
    text-align: center;
    margin: 3rem auto 4rem;
  }

  section.cta h2 {
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
    color: #fff;
    text-shadow: 0 2px 8px rgba(0,0,0,0.7);
  }

  footer {
    text-align: center;
    padding: 1.5rem 1rem;
    color: #eee;
    background: rgba(0,0,0,0.3);
    font-size: 0.9rem;
  }

  /* Responsive */

  @media (max-width: 768px) {
    header {
      flex-direction: column;
      align-items: flex-start;
    }
    nav {
      margin-top: 1rem;
    }
    nav a {
      margin-left: 0;
      margin-right: 1.5rem;
    }
    section.features {
      flex-direction: column;
      margin: -3rem 1rem 2rem;
      border-radius: 15px;
      padding: 3rem 1rem;
    }
  }
</style>
</head>
<body>
  <header>
    <h1>Gotowe Posiłki</h1>
    <nav>
      <a href="#features">Co oferujemy</a>
      <a href="#kup">Kup teraz</a>
      <a href="#kontakt">Kontakt</a>
    </nav>
  </header>

  <section class="hero">
    <div class="hero-content">
      <h2>Zdrowa dieta dopasowana do Ciebie</h2>
      <p>Gotowe jadłospisy z pełną listą zakupów i przepisami — wygoda i smak każdego dnia.</p>
      <a href="#kup" class="btn-primary">Kup teraz – 39 zł</a>
    </div>
  </section>

  <section id="features" class="features">
    <div class="feature-card">
      <img src="https://source.unsplash.com/90x90/?salad,healthy" alt="Zdrowe posiłki" />
      <h3>Zbilansowane jadłospisy</h3>
      <p>Przepisy od 2000 do 3500 kcal, idealne na każdy cel dietetyczny.</p>
    </div>
    <div class="feature-card">
      <img src="https://source.unsplash.com/90x90/?fitness,workout" alt="Trening i dieta" />
      <h3>Dla aktywnych</h3>
      <p>Dieta dostosowana do Twojej aktywności i celu: masa, redukcja lub utrzymanie.</p>
    </div>
    <div class="feature-card">
      <img src="https://source.unsplash.com/90x90/?shopping,list" alt="Lista zakupów" />
      <h3>Lista zakupów</h3>
      <p>Wszystko, co potrzebujesz, w jednym miejscu, gotowe do pobrania i wydruku.</p>
    </div>
  </section>

  <section id="kup" class="cta">
    <h2>Kup swój e-book już dziś!</h2>
    <a href="https://twoj-link-do-sklepu" target="_blank" rel="noopener" class="btn-primary" style="font-size:1.5rem; padding:1rem 4rem;">
      Kup teraz – 39 zł
    </a>
  </section>

  <footer id="kontakt">
    <p>© 2025 Gotowe Posiłki. Wszelkie prawa zastrzeżone.</p>
  </footer>
</body>
</html>
