# team-site
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bean & Brew — кофейня</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header class="header">
    <div class="container header-inner">
      <a href="#" class="logo">☕ Bean &amp; Brew</a>
      <nav class="nav">
        <a href="#menu">Меню</a>
        <a href="#about">О нас</a>
        <a href="#contacts">Контакты</a>
      </nav>
      <button class="burger" id="burger" aria-label="Меню">☰</button>
    </div>
  </header>

  <section class="hero">
    <div class="container">
      <h1>Свежий кофе <span class="accent">каждое утро</span></h1>
      <p>Обжариваем зёрна сами, варим с любовью, подаём с улыбкой.</p>
      <a href="#menu" class="btn">Смотреть меню</a>
    </div>
  </section>

  <section class="features">
    <div class="container features-grid">
      <div class="feature-card">
        <div class="feature-icon">🌱</div>
        <h3>Своё обжаривание</h3>
        <p>Зёрна приезжают к нам зелёными — обжариваем по 15 кг в день.</p>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🥐</div>
        <h3>Свежая выпечка</h3>
        <p>Круассаны и слойки из печи — к 8 утра каждые будни.</p>
      </div>
      <div class="feature-card">
        <div class="feature-icon">📶</div>
        <h3>Работать можно</h3>
        <p>Быстрый Wi-Fi, розетки у каждого стола и никаких «садитесь на полчаса».</p>
      </div>
    </div>
  </section>

  <section id="menu" class="menu">
    <div class="container">
      <h2>Меню</h2>
      <ul class="menu-list" id="menuList"></ul>
    </div>
  </section>

  <section id="about" class="about">
    <div class="container">
      <h2>О нас</h2>
      <p>Bean &amp; Brew открылась в 2019 году и с тех пор варит кофе для всего района.
         Мы верим, что хороший эспрессо — это ремесло: 9 бар, 25 секунд, 18 граммов зерна.</p>
    </div>
  </section>

  <section id="contacts" class="contacts">
    <div class="container">
      <h2>Контакты</h2>
      <form id="contactForm" class="contact-form">
        <input type="text" name="name" placeholder="Ваше имя" required>
        <input type="email" name="email" placeholder="Email" required>
        <textarea name="message" placeholder="Сообщение" required></textarea>
        <button type="submit" class="btn">Отправить</button>
      </form>
      <p class="form-msg" id="formMsg"></p>
    </div>
  </section>

  <footer class="footer">
    <div class="container">
      <p>© 2026 Bean &amp; Brew. Сделано с ☕ и ♥</p>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>
style.css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --brown: #6f4e37;
  --dark: #2b1d14;
  --cream: #f5efe6;
  --accent: #c98b52;
}

body {
  font-family: "Segoe UI", Arial, sans-serif;
  color: var(--dark);
  background: var(--cream);
  line-height: 1.6;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Шапка */
.header {
  position: sticky;
  top: 0;
  background: var(--dark);
  color: #fff;
  z-index: 100;
}

.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 14px 20px;
}

.logo {
  color: #fff;
  text-decoration: none;
  font-weight: 700;
  font-size: 1.3rem;
}

.nav a {
  color: #fff;
  text-decoration: none;
  margin-left: 24px;
  opacity: 0.85;
}

.nav a:hover {
  opacity: 1;
  color: var(--accent);
}

.burger {
  display: none;
  background: none;
  border: none;
  color: #fff;
  font-size: 1.4rem;
  cursor: pointer;
}

/* Хиро */
.hero {
  background: linear-gradient(135deg, var(--dark), var(--brown));
  color: #fff;
  text-align: center;
  padding: 110px 20px;
}

.hero h1 {
  font-size: 2.6rem;
  margin-bottom: 12px;
}

.accent {
  color: var(--accent);
}

.hero p {
  font-size: 1.2rem;
  margin-bottom: 28px;
  opacity: 0.9;
}

.btn {
  display: inline-block;
  background: var(--accent);
  color: #fff;
  padding: 12px 32px;
  border-radius: 30px;
  text-decoration: none;
  border: none;
  font-size: 1rem;
  cursor: pointer;
  transition: transform 0.2s, background 0.2s;
}

.btn:hover {
  background: #b47a3f;
  transform: translateY(-2px);
}

/* Преимущества */
.features {
  padding: 70px 0;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.feature-card {
  background: #fff;
  border-radius: 14px;
  padding: 28px;
  box-shadow: 0 4px 14px rgba(0, 0, 0, 0.06);
}

.feature-icon {
  font-size: 2rem;
  margin-bottom: 10px;
}

.feature-card h3 {
  margin-bottom: 8px;
}

/* Меню */
.menu {
  background: #fff;
  padding: 70px 0;
}

.menu h2, .about h2, .contacts h2 {
  text-align: center;
  margin-bottom: 32px;
  font-size: 2rem;
}

.menu-list {
  list-style: none;
  max-width: 560px;
  margin: 0 auto;
}

.menu-item {
  display: flex;
  justify-content: space-between;
  padding: 14px 8px;
  border-bottom: 1px dashed #ddd;
}

.menu-item .price {
  color: var(--brown);
  font-weight: 700;
}

/* О нас */
.about {
  padding: 70px 0;
  text-align: center;
}

.about p {
  max-width: 640px;
  margin: 0 auto;
  font-size: 1.1rem;
}

/* Контакты */
.contacts {
  padding: 70px 0;
  background: #fff;
}

.contact-form {
  max-width: 480px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.contact-form input,
.contact-form textarea {
  padding: 12px 14px;
  border: 1px solid #ddd;
  border-radius: 8px;
  font: inherit;
  resize: vertical;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: 2px solid var(--accent);
  border-color: transparent;
}

.form-msg {
  text-align: center;
  color: green;
  margin-top: 14px;
}

/* Подвал */
.footer {
  background: var(--dark);
  color: #fff;
  text-align: center;
  padding: 24px 0;
}

/* Адаптив */
@media (max-width: 720px) {
  .features-grid {
    grid-template-columns: 1fr;
  }

  .burger {
    display: block;
  }

  .nav {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: var(--dark);
    flex-direction: column;
    padding: 16px;
  }

  .nav.open {
    display: flex;
  }

  .nav a {
    margin: 8px 0;
  }

  .hero h1 {
    font-size: 2rem;
  }
}
script.js
// Меню кофейни
const menuItems = [
  { name: 'Эспрессо', price: 120 },
  { name: 'Капучино', price: 180 },
  { name: 'Латте', price: 190 },
  { name: 'Флэт уайт', price: 210 },
  { name: 'Раф ванильный', price: 240 },
  { name: 'Круассан', price: 130 },
  { name: 'Чизкейк', price: 220 },
];

const menuList = document.getElementById('menuList');
menuList.innerHTML = menuItems
  .map(item => <li class="menu-item"><span>${item.name}</span><span class="price">${item.price} ₽</span></li>)
  .join('');

// Мобильное меню
const burger = document.getElementById('burger');
const nav = document.querySelector('.nav');
burger.addEventListener('click', () => nav.classList.toggle('open'));
nav.querySelectorAll('a').forEach(link =>
  link.addEventListener('click', () => nav.classList.remove('open'))
);

// Форма
const form = document.getElementById('contactForm');
const formMsg = document.getElementById('formMsg');
form.addEventListener('submit', (e) => {
  e.preventDefault();
  formMsg.textContent = 'Спасибо! Мы ответим вам в течение дня ☕';
  form.reset();
});