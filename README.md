<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>CAFÉ CAMINO — уютная кофейня</title>
  <meta name="description" content="Camino — уютная кофейня для мам с детьми, фрилансеров и соседних офисов. Кофе, матча, авторские напитки и выпечка." />

  <!-- Базовые стили, переменные для быстрой настройки бренда -->
  <style>
    :root{
      --bg: #262626;
      --accent: #b8583а; /* основной цвет */
      --accent-dark: #8a3923;
      --muted: #6b6b6b;
      --card: #ffffff;
      --radius: 12px;
      --max-width: 1100px;
      --shadow: 0 6px 18px rgba(15,15,15,0.08);
      --glass: rgba(255,255,255,0.6);
      --font-sans: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:var(--font-sans);
      background:linear-gradient(180deg,var(--bg),#fff);
      color:#222;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding-bottom:64px;
    }

    .wrap{max-width:var(--max-width);margin:0 auto;padding:28px;}
    header{display:flex;align-items:center;justify-content:space-between;padding:12px 0;}
    .brand{display:flex;gap:14px;align-items:center}
    .logo{
      width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--accent),var(--accent-dark));
      display:flex;align-items:center;justify-content:center;color:#fff;font-weight:700;font-size:20px;box-shadow:var(--shadow);
    }
    h1{margin:0;font-size:20px}
    .tag{color:var(--muted);font-size:13px}

    /* Hero */
    .hero{
      display:grid;
      grid-template-columns:1fr 420px;
      gap:22px;
      align-items:center;
      margin:18px 0 28px;
    }
    .hero-card{
      background:var(--card);
      padding:22px;border-radius:var(--radius);box-shadow:var(--shadow);
    }
    .hero h2{margin:0 0 8px;font-size:28px}
    .hero p{margin:0;color:var(--muted)}
    .cta-row{display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .btn{
      display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:10px;border:0;cursor:pointer;font-weight:600;
      background:var(--accent);color:#fff;box-shadow:0 6px 14px rgba(176,75,44,0.18)
    }
    .btn.secondary{background:transparent;color:var(--accent);border:1px solid rgba(170,80,50,0.12);font-weight:600}

    /* Info small cards */
    .cards{display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .small-card{background:var(--card);padding:12px;border-radius:10px;box-shadow:var(--shadow);min-width:140px;flex:1}

    /* Right column image / cozy scene */
    .hero-image{
      height:320px;border-radius:var(--radius);background-image:linear-gradient(135deg,rgba(0,0,0,0.08),transparent), url('https://images.unsplash.com/photo-1509042239860-f550ce710b93?auto=format&fit=crop&w=1000&q=60');
      background-size:cover;background-position:center;box-shadow:var(--shadow);display:flex;align-items:flex-end;padding:18px;color:#fff;
    }
    .hero-image .meta{background:linear-gradient(180deg,rgba(0,0,0,0.35),rgba(0,0,0,0.12));padding:10px;border-radius:8px}

    /* Menu */
    .menu{margin:26px 0}
    .menu-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
    .menu-card{background:var(--card);border-radius:12px;padding:14px;box-shadow:var(--shadow)}
    .menu-card h3{margin:4px 0 10px}
    .menu-item{display:flex;justify-content:space-between;padding:8px 0;border-top:1px dashed rgba(10,10,10,0.03)}
    .menu-item:first-of-type{border-top:0}
    .item-left{display:flex;gap:12px;align-items:center}
    .item-thumb{width:54px;height:54;border-radius:10px;background:#f3f3f3;flex:0 0 54px;overflow:hidden}
    .item-thumb img{width:100%;height:100%;object-fit:cover;display:block}
    .item-meta{min-width:0}
    .item-name{font-weight:700}
    .item-desc{font-size:13px;color:var(--muted);margin-top:4px}
    .item-price{font-weight:700;color:var(--accent);min-width:70px;text-align:right}

    /* Gallery */
    .gallery{display:flex;gap:10px;flex-wrap:wrap;margin-top:18px}
    .gallery img{width:calc(33.333% - 6.6px);border-radius:10px;height:120px;object-fit:cover;box-shadow:var(--shadow)}

    /* Contact */
    .contact{display:grid;grid-template-columns:1fr 320px;gap:20px;margin-top:26px}
    .contact-card{background:var(--card);padding:14px;border-radius:12px;box-shadow:var(--shadow)}
    .map-placeholder{background:linear-gradient(135deg,#eee,#f7f7f7);height:220px;border-radius:12px;display:flex;align-items:center;justify-content:center;color:var(--muted)}

    footer{margin-top:28px;padding:18px 0;text-align:center;color:var(--muted);font-size:13px}

    /* Responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr}
      .menu-grid{grid-template-columns:1fr}
      .contact{grid-template-columns:1fr}
      .gallery img{width:calc(50% - 7px);height:110px}
    }
    @media (max-width:540px){
      .gallery img{width:100%;height:160px}
      .logo{width:46px;height:46px}
    }

    /* simple accessible focus */
    .btn:focus{outline:3px solid rgba(176,75,44,0.18);outline-offset:3px}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo">C</div>
        <div>
          <h1>CAFÉ CAMINO</h1>
          <div class="tag">уютно • кофе • для мам и тех, кто работает рядом</div>
        </div>
      </div>
      <nav aria-label="Навигация">
        <button class="btn" onclick="scrollToSection('menu')">Меню</button>
        <button class="btn secondary" onclick="scrollToSection('contact')">Контакты</button>
      </nav>
    </header>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-card">
        <h2>Кофейня Camino — место, где тепло и вкусно</h2>
        <p>Мы создали пространство для мам с детьми, фрилансеров и соседних офисов: удобная детская зона, стабильный интернет, мягкие кресла и заботливое меню.</p>

        <div class="cta-row">
          <button class="btn" onclick="scrollToSection('menu')">Посмотреть меню</button>
          <button class="btn secondary" onclick="openOrder()">Заказать/Забронировать стол</button>
        </div>

        <div class="cards" aria-hidden="false">
          <div class="small-card">
            <strong>Детская зона</strong>
            <div style="font-size:13px;color:var(--muted);margin-top:6px">Мягкие игрушки, игровая полка и удобные стульчики</div>
          </div>
          <div class="small-card">
            <strong>Wi‑Fi & розетки</strong>
            <div style="font-size:13px;color:var(--muted);margin-top:6px">Удобно для работы и звонков</div>
          </div>
          <div class="small-card">
            <strong>Гибкие часы</strong>
            <div style="font-size:13px;color:var(--muted);margin-top:6px">Открыты с 8:00 до 20:00</div>
          </div>
        </div>
      </div>

      <aside class="hero-image" aria-hidden="true">
        <div class="meta">
          <div style="font-weight:700">Уют и атмосфера</div>
          <div style="font-size:13px">Тёплый свет, дерево и удобные места для работы</div>
        </div>
      </aside>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="hero-card" style="margin-bottom:18px">
        <h3>Немного о нас</h3>
        <p style="color:var(--muted);margin-top:8px">Camino — кофейня с вниманием к деталям: от свежей обжарки до комфортной детской зоны. Наше меню сочетает классические напитки и авторские рецепты, а выпечка готовится ежедневно собственными руками.</p>
      </div>
    </section>

    <!-- MENU -->
    <section id="menu" class="menu" aria-labelledby="menu-heading">
      <h3 id="menu-heading">Меню</h3>
      <div class="menu-grid" id="menu-grid">
        <!-- Здесь скрипт подставит карточки категорий и позиции -->
      </div>
    </section>

    <!-- GALLERY -->
    <section id="gallery" style="margin-top:6px">
      <h3>Интерьер и выпечка</h3>
      <div class="gallery" id="gallery-grid">
        <img src="https://images.unsplash.com/photo-1506784983877-45594efa4cbe?auto=format&fit=crop&w=800&q=60" alt="Кофейня уют">
        <img src="https://images.unsplash.com/photo-1541542684-5b6e0b1f4f36?auto=format&fit=crop&w=800&q=60" alt="Выпечка">
        <img src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=800&q=60" alt="Кофе">
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="contact" aria-label="Контакты">
      <div class="contact-card contact-card-left">
        <h3>Контакты</h3>
        <p style="color:var(--muted)">Адрес: ул. Примерная, 12 — центр района. Телефон: +375 XX XXX-XX-XX</p>

        <div style="display:flex;gap:12px;margin-top:12px;flex-wrap:wrap">
          <div style="min-width:160px">
            <strong>Часы работы</strong>
            <div style="color:var(--muted);margin-top:6px">Ежедневно 08:00 — 20:00</div>
          </div>
          <div style="min-width:160px">
            <strong>Зона для детей</strong>
            <div style="color:var(--muted);margin-top:6px">Маленькая игровая площадка и комфортные кресла</div>
          </div>
        </div>

        <div style="margin-top:14px">
          <button class="btn" onclick="openOrder()">Забронировать стол</button>
        </div>
      </div>

      <div class="contact-card">
        <h4>Карта</h4>
        <div class="map-placeholder">Здесь можно вставить iframe Google/Яндекс карты</div>
        <div style="margin-top:10px;color:var(--muted);font-size:13px">Если нужно, заменю placeholder на iframe карты — вставьте ваш embed code.</div>
      </div>
    </section>

    <footer>
      © CAFÉ CAMINO — уютная кофейня; создано для мам, тех, кто работает рядом, и всех любителей хорошего кофе.
    </footer>
  </div>

  <!-- Скрипт подставляет меню из удобного JS-объекта -->
  <script>
    // Пример данных меню. Редактируйте, добавляйте категории и пункты.
    // Каждая категория: { id, title, description, items: [{name, desc, price, image}] }
    const MENU = [
      {
        id: 'classic',
        title: 'Классические напитки',
        description: 'Эспрессо, американо, капучино и латте — классика в специальной обжарке.',
        items: [
          { name: 'Эспрессо', desc: '25 мл, насыщенно', price: '3.00', image:'' },
          { name: 'Американо', desc: 'Эспрессо + горячая вода', price: '3.50', image:'' },
          { name: 'Капучино', desc: 'Пенка из молока, лёгкая карамель', price: '4.50', image:'' },
          { name: 'Латте', desc: 'Мягкое, сливочное', price: '4.80', image:'' }
        ]
      },
      {
        id: 'hot',
        title: 'Горячие напитки',
        description: 'Чай, матча-латте, горячий шоколад — согреем в любой день.',
        items: [
          { name: 'Матча латте', desc: 'Японская матча с нежным молоком', price: '5.50', image:'' },
          { name: 'Чёрный чай', desc: 'Ассортимент: Эрл Грей, Английский завтрак', price: '2.80', image:'' },
          { name: 'Горячий шоколад', desc: 'Традиционный, с тёмным шоколадом', price: '4.70', image:'' }
        ]
      },
      {
        id: 'signature',
        title: 'Авторское меню',
        description: 'Наши фирменные рецепты — хорошие варианты для подарка себе.',
        items: [
          { name: 'Camino Spiced Latte', desc: 'Коричная нота, мягкая сливочная пена', price: '6.00', image:'' },
          { name: 'Citrus Cold Brew', desc: 'Охлаждённый колд брю с апельсином', price: '6.20', image:'' }
        ]
      },
      {
        id: 'bakery',
        title: 'Выпечка и еда',
        description: 'Круассаны, сырники, блинчики и сэндвичи — готовим каждый день.',
        items: [
          { name: 'Круассан с лососем', desc: 'Сливочный сыр и маринованный лосось', price: '7.50', image:'' },
          { name: 'Блинчики', desc: 'Подаются с разными начинками', price: '5.00', image:'' },
          { name: 'Сырники', desc: 'Нежные, с ягодным соусом', price: '5.50', image:'' }
        ]
      }
    ];

    // Рендер меню в DOM
    const menuGrid = document.getElementById('menu-grid');

    function renderMenu(){
      menuGrid.innerHTML = '';
      MENU.forEach(cat => {
        const card = document.createElement('div');
        card.className = 'menu-card';
        const title = document.createElement('h3');
        title.textContent = cat.title;
        const desc = document.createElement('div');
        desc.style.color = 'var(--muted)';
        desc.style.fontSize = '13px';
        desc.style.marginBottom = '8px';
        desc.textContent = cat.description || '';
        card.appendChild(title);
        card.appendChild(desc);

        cat.items.forEach(it => {
          const item = document.createElement('div');
          item.className = 'menu-item';

          const left = document.createElement('div');
          left.className = 'item-left';

          const thumb = document.createElement('div');
          thumb.className = 'item-thumb';
          if (it.image){
            const img = document.createElement('img');
            img.src = it.image;
            img.alt = it.name;
            thumb.appendChild(img);
          } else {
            thumb.style.display = 'none';
          }

          const meta = document.createElement('div');
          meta.className = 'item-meta';
          const name = document.createElement('div');
          name.className = 'item-name';
          name.textContent = it.name;
          const ide = document.createElement('div');
          ide.className = 'item-desc';
          ide.textContent = it.desc || '';
          meta.appendChild(name);
          meta.appendChild(ide);

          left.appendChild(thumb);
          left.appendChild(meta);

          const price = document.createElement('div');
          price.className = 'item-price';
          price.textContent = it.price ? it.price + ' BYN' : '';

          item.appendChild(left);
          item.appendChild(price);

          card.appendChild(item);
        });

        menuGrid.appendChild(card);
      });
    }

    renderMenu();

    // Простые утилиты пользовательского взаимодействия
    function scrollToSection(id){
      const el = document.getElementById(id);
      if (!el) return;
      el.scrollIntoView({behavior:'smooth',block:'start'});
    }

    function openOrder(){
      // Здесь вы можете подцепить форму брони или мессенджер
      const phone = 'пожалуйста, позвоните нам по телефону указанному в контактах';
      alert('Чтобы забронировать стол или заказать — ' + phone);
    }

    // Позволяет динамически добавлять позицию в меню из консоли браузера:
    // addMenuItem('bakery', {name:'Новый', desc:'Описание', price:'4.00'});
    function addMenuItem(categoryId, item){
      const cat = MENU.find(c => c.id === categoryId);
      if (!cat) return console.warn('Категория не найдена', categoryId);
      cat.items.push(item);
      renderMenu();
    }

    // Экспорт меню в JSON (можно сохранить/редактировать отдельно)
    function exportMenuJSON(){
      const s = JSON.stringify(MENU, null, 2);
      console.log(s);
      return s;
    }
  </script>
</body>
</html>
