# proverka1
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
<title>Интернет-магазин</title>
<style>
  /* Reset and base styles */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #f9f9f9;
    color: #333;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
  a {
    text-decoration: none;
    color: inherit;
  }
  /* Header */
  header {
    background: #2a70d4;
    padding: 1rem 1.5rem;
    color: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  header h1 {
    font-size: 1.5rem;
    user-select: none;
  }
  nav ul {
    list-style: none;
    display: flex;
    gap: 1rem;
  }
  nav ul li a {
    font-weight: 600;
    padding: 0.25rem 0.5rem;
    border-radius: 4px;
    transition: background-color 0.3s ease;
  }
  nav ul li a:hover,
  nav ul li a:focus {
    background-color: rgba(255,255,255,0.2);
    outline: none;
  }
  /* Main content */
  main {
    flex: 1;
    padding: 1rem 1rem 2rem 1rem;
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
  }
  .product-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
  }
  .product-card {
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 6px 15px rgb(0 0 0 / 0.1);
    display: flex;
    flex-direction: column;
    overflow: hidden;
    transition: box-shadow 0.3s ease;
  }
  .product-card:hover,
  .product-card:focus-within {
    box-shadow: 0 10px 25px rgba(42,112,212,0.4);
  }
  .product-image {
    width: 100%;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    transition: transform 0.3s ease;
  }
  .product-card:hover .product-image,
  .product-card:focus-within .product-image {
    transform: scale(1.05);
  }
  .product-info {
    padding: 0.75rem 1rem 1.25rem 1rem;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }
  .product-title {
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 0.25rem;
  }
  .product-description {
    flex-grow: 1;
    font-size: 0.9rem;
    color: #555;
    margin-bottom: 0.75rem;
  }
  .product-price {
    font-size: 1.1rem;
    font-weight: 700;
    color: #2a70d4;
    margin-bottom: 1rem;
  }
  .add-to-cart-btn {
    background-color: #2a70d4;
    color: #fff;
    border: none;
    padding: 0.6rem 1rem;
    border-radius: 6px;
    font-weight: 600;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  .add-to-cart-btn:hover,
  .add-to-cart-btn:focus {
    background-color: #1f52b9;
  }
  /* Footer */
  footer {
    background: #2a70d4;
    color: #fff;
    text-align: center;
    padding: 1rem;
    font-size: 0.9rem;
    user-select: none;
  }
  /* Responsive adjustments */
  @media (max-width: 480px) {
    header h1 {
      font-size: 1.25rem;
    }
    nav ul {
      gap: 0.5rem;
    }
    .product-info {
      padding: 0.5rem 0.75rem 1rem 0.75rem;
    }
    .product-title {
      font-size: 1rem;
    }
    .product-description {
      font-size: 0.85rem;
    }
    .product-price {
      font-size: 1rem;
    }
  }
</style>
</head>
<body>
<header>
  <h1>Мой Интернет-Магазин</h1>
  <nav aria-label="Главное меню">
    <ul>
      <li><a href="#" tabindex="0">Главная</a></li>
      <li><a href="#" tabindex="0">Каталог</a></li>
      <li><a href="#" tabindex="0">О нас</a></li>
      <li><a href="#" tabindex="0">Контакты</a></li>
      <li><a href="#" tabindex="0">Корзина (<span id="cart-count">0</span>)</a></li>
    </ul>
  </nav>
</header>
<main>
  <section class="product-list" aria-label="Список товаров">
    <!-- Example product -->
    <article class="product-card" tabindex="0">
      <img src="https://images.pexels.com/photos/298863/pexels-photo-298863.jpeg?auto=compress&cs=tinysrgb&h=400" alt="Смартфон" class="product-image" />
      <div class="product-info">
        <h2 class="product-title">Современный смартфон</h2>
        <p class="product-description">Мощный смартфон с высоким качеством камеры и длительной работой аккумулятора.</p>
        <p class="product-price">25 000 ₽</p>
        <button class="add-to-cart-btn" aria-label="Добавить Современный смартфон в корзину" data-product="Современный смартфон" data-price="25000">В корзину</button>
      </div>
    </article>
    <article class="product-card" tabindex="0">
      <img src="https://images.pexels.com/photos/264636/pexels-photo-264636.jpeg?auto=compress&cs=tinysrgb&h=400" alt="Наушники" class="product-image" />
      <div class="product-info">
        <h2 class="product-title">Беспроводные наушники</h2>
        <p class="product-description">Комфортные наушники с отличным звуком и шумоподавлением.</p>
        <p class="product-price">8 500 ₽</p>
        <button class="add-to-cart-btn" aria-label="Добавить Беспроводные наушники в корзину" data-product="Беспроводные наушники" data-price="8500">В корзину</button>
      </div>
    </article>
    <article class="product-card" tabindex="0">
      <img src="https://images.pexels.com/photos/267350/pexels-photo-267350.jpeg?auto=compress&cs=tinysrgb&h=400" alt="Умные часы" class="product-image" />
      <div class="product-info">
        <h2 class="product-title">Умные часы</h2>
        <p class="product-description">Станьте на шаг ближе к здоровому образу жизни с помощью умных часов.</p>
        <p class="product-price">12 700 ₽</p>
        <button class="add-to-cart-btn" aria-label="Добавить Умные часы в корзину" data-product="Умные часы" data-price="12700">В корзину</button>
      </div>
    </article>
  </section>
</main>
<footer>
  &copy; 2024 Мой Интернет-Магазин — Все права защищены
</footer>
<script>
  // Simple cart functionality using localStorage
  const cartCountEl = document.getElementById('cart-count');
  const buttons = document.querySelectorAll('.add-to-cart-btn');
  
  function getCart() {
    return JSON.parse(localStorage.getItem('cart')) || [];
  }
  function setCart(cart) {
    localStorage.setItem('cart', JSON.stringify(cart));
    cartCountEl.textContent = cart.length;
  }
  function addToCart(product) {
    const cart = getCart();
    cart.push(product);
    setCart(cart);
  }
  // Initialize cart count on page load
  document.addEventListener('DOMContentLoaded', () => {
    setCart(getCart());
  });
  buttons.forEach(button => {
    button.addEventListener('click', () => {
      const product = {
        name: button.dataset.product,
        price: parseFloat(button.dataset.price)
      };
      addToCart(product);
      button.textContent = 'Добавлено';
      button.disabled = true;
      setTimeout(() => {
        button.textContent = 'В корзину';
        button.disabled = false;
      }, 1500);
    });
  });
</script>
</body>
</html>
