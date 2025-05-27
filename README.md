<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Gotowe Posiłki i Kalkulator Kalorii</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background: #f9f9f9;
      color: #333;
    }
    h1, h2 {
      text-align: center;
      color: #2c3e50;
    }
    form {
      max-width: 400px;
      margin: 0 auto 40px;
      background: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    label {
      display: block;
      margin: 10px 0 5px;
    }
    input[type="number"], select {
      width: 100%;
      padding: 8px;
      box-sizing: border-box;
      margin-bottom: 15px;
      border-radius: 4px;
      border: 1px solid #ccc;
    }
    .radio-group {
      display: flex;
      justify-content: space-between;
      margin-bottom: 15px;
    }
    .radio-group label {
      flex: 1;
      margin-right: 10px;
      font-weight: normal;
    }
    button {
      background-color: #27ae60;
      color: white;
      border: none;
      padding: 12px;
      border-radius: 4px;
      cursor: pointer;
      width: 100%;
      font-size: 16px;
    }
    button:hover {
      background-color: #219150;
    }
    .ebooks {
      max-width: 1200px;
      margin: 0 auto;
    }
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .product {
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      padding: 15px;
      text-align: center;
    }
    .product img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 6px;
    }
    .product h2 {
      margin: 15px 0 10px;
      font-size: 20px;
      color: #34495e;
    }
    .product p {
      font-size: 14px;
      color: #666;
      min-height: 60px;
    }
    .product button {
      margin-top: 10px;
      background-color: #2980b9;
      width: auto;
      padding: 10px 20px;
      font-size: 15px;
    }
    .product button:hover {
      background-color: #1f6391;
    }
    footer {
      text-align: center;
      margin: 40px 0 20px;
      color: #999;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <h1>Gotowe Posiłki i Kalkulator Kalorii</h1>
  <p style="text-align:center;">Dopasuj kaloryczność i wybierz idealny e-book</p>

  <form id="calorieForm">
    <label for="age">Wiek:</label>
    <input type="number" id="age" name="age" min="10" max="100" required />

    <label for="height">Wzrost (cm):</label>
    <input type="number" id="height" name="height" min="100" max="250" required />

    <label for="weight">Waga (kg):</label>
    <input type="number" id="weight" name="weight" min="30" max="250" required />

    <label>Płeć:</label>
    <div class="radio-group">
      <label><input type="radio" name="gender" value="male" required /> Mężczyzna</label>
      <label><input type="radio" name="gender" value="female" /> Kobieta</label>
    </div>

    <label>Cel:</label>
    <div class="radio-group">
      <label><input type="radio" name="goal" value="maintain" required /> Utrzymanie wagi</label>
      <label><input type="radio" name="goal" value="reduce" /> Redukcja</label>
      <label><input type="radio" name="goal" value="gain" /> Masa</label>
    </div>

    <label>Aktywność:</label>
    <div class="radio-group" style="flex-wrap: wrap;">
      <label><input type="radio" name="activity" value="none" required /> Brak aktywności</label>
      <label><input type="radio" name="activity" value="light" /> Lekka aktywność</label>
      <label><input type="radio" name="activity" value="moderate" /> Średnia aktywność</label>
      <label><input type="radio" name="activity" value="high" /> Duża aktywność</label>
    </div>

    <button type="submit">Oblicz</button>
  </form>

  <section class="ebooks" id="ebooksSection" style="display:none;">
    <h2>Wybierz e-book z gotowymi posiłkami</h2>
    <div class="product-grid">
      <div class="product" data-kcal="2000">
        <img src="https://source.unsplash.com/400x300/?healthy,meal" alt="2000 kcal" />
        <h2>Gotowe Posiłki – 2000 kcal</h2>
        <p>Idealne na redukcję z pełnym jadłospisem i listą zakupów.</p>
        <button>Kup teraz – 39 zł</button>
      </div>
      <div class="product" data-kcal="2300">
        <img src="https://source.unsplash.com/400x300/?meal,fit" alt="2300 kcal" />
        <h2>Gotowe Posiłki – 2300 kcal</h2>
        <p>Zbilansowane posiłki na utrzymanie formy lub lekki deficyt.</p>
        <button>Kup teraz – 39 zł</button>
      </div>
      <div class="product" data-kcal="2500">
        <img src="https://source.unsplash.com/400x300/?fitness,lunch" alt="2500 kcal" />
        <h2>Gotowe Posiłki – 2500 kcal</h2>
        <p>Codzienne przepisy idealne przy treningach siłowych.</p>
        <button>Kup teraz – 39 zł</button>
      </div>
      <div class="product" data-kcal="2800">
        <img src="https://source.unsplash.com/400x300/?food,meal" alt="2800 kcal" />
        <h2>Gotowe Posiłki – 2800 kcal</h2>
        <p>Dieta dla osób z wysoką aktywnością i potrzebą energii.</p>
        <button>Kup teraz – 39 zł</button>
      </div>
      <div class="product" data-kcal="3000">
        <img src="https://source.unsplash.com/400x300/?chicken,meal" alt="3000 kcal" />
        <h2>Gotowe Posiłki – 3000 kcal</h2>
        <p>Skuteczna dieta masowa – smaczna i łatwa w przygotowaniu.</p>
        <button>Kup teraz – 39 zł</button>
      </div>
      <div class="product" data-kcal="3500">
        <img src="https://source.unsplash.com/400x300/?bulk,meal" alt="3500 kcal" />
        <h2>Gotowe Posiłki – 3500 kcal</h2>
        <p>Wysokoenergetyczna dieta dla zaawansowanych.</p>
        <button>Kup teraz – 39 zł</button>
      </div>
    </div>
  </section>

  <footer>
    © 2025 Gotowe Posiłki. Wszelkie prawa zastrzeżone.
  </footer>

  <script>
    const form = document.getElementById('calorieForm');
    const ebooksSection = document.getElementById('ebooksSection');
    const products = document.querySelectorAll('.product');

    // Funkcja do obliczenia podstawowej przemiany materii (BMR) metodą Mifflin-St Jeor
    function calculateBMR(age, weight, height, gender) {
      if(gender === 'male') {
        return 10 * weight + 6.25 * height - 5 * age + 5;
      } else {
        return 10 * weight + 6.25 * height - 5 * age - 161;
      }
    }

    // Współczynniki aktywności
    const activityFactors = {
      none: 1.2,
      light: 1.375,
      moderate: 1.55,
      high: 1.725
    };

    // Funkcja do kalkulacji dziennego zapotrzebowania kalorycznego
    function calculateCalories(age, weight, height, gender, activity, goal) {
      let bmr = calculateBMR(age, weight, height, gender);
      let maintenanceCalories = bmr * activityFactors[activity];
      switch(goal) {
        case 'reduce': 
          return Math.round(maintenanceCalories * 0.85);
        case 'gain': 
          return Math.round(maintenanceCalories * 1.15);
        default: 
          return Math.round(maintenanceCalories);
      }
    }

    // Obsługa formularza
    form.addEventListener('submit', function(e) {
      e.preventDefault();

      const age = parseInt(form.age.value);
      const height = parseInt(form.height.value);
      const weight = parseInt(form.weight.value);
      const gender = form.gender.value;
      const goal = form.goal.value;
      const activity = form.activity.value;

      const calories = calculateCalories(age, weight, height, gender, activity, goal);

      // Pokaż sekcję z ebookami i zaznacz najlepszy zakres kaloryczny
      ebooksSection.style.display = 'block';

      // Podświetl produkt najbliższy obliczonym kaloriom
      products.forEach(product => {
        const kcal = parseInt(product.getAttribute('data-kcal'));
        if(Math.abs(kcal - calories) <= 200) {
          product.style.border = '3px solid #27ae60';
          product.style.boxShadow = '0 0 15px #27ae60';
        } else {
          product.style.border = 'none';
          product.style.boxShadow = '0 2px 10px rgba(0,0,0,0.1)';
        }
      });

      alert(`Twoje dzienne zapotrzebowanie kaloryczne wynosi około ${calories} kcal.\nPolecamy e-booki z kalorycznością dopasowaną do Twoich potrzeb.`);
    });
  </script>

</body>
</html>
