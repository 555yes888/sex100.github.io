# sex100.github.io
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>NIGHT LIFE｜夜生活娛樂資訊</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family:
        -apple-system,
        BlinkMacSystemFont,
        "Noto Sans TC",
        "Microsoft JhengHei",
        sans-serif;
      background: #0b0b0d;
      color: #fff;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* ===== 導覽列 ===== */

    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(11, 11, 13, 0.95);
      border-bottom: 1px solid #29292d;
      backdrop-filter: blur(10px);
    }

    .nav {
      max-width: 1200px;
      margin: auto;
      height: 72px;
      padding: 0 24px;

      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 24px;
      font-weight: 900;
      letter-spacing: 2px;
      color: #d9a441;
    }

    .menu {
      display: flex;
      gap: 28px;
      list-style: none;
      color: #ccc;
    }

    .menu a:hover {
      color: #d9a441;
    }

    .menu-btn {
      display: none;
      font-size: 26px;
      cursor: pointer;
    }

    /* ===== Hero ===== */

    .hero {
      min-height: 560px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;

      padding: 80px 20px;

      background:
        linear-gradient(
          rgba(0,0,0,.55),
          rgba(0,0,0,.85)
        ),
        url("https://images.unsplash.com/photo-1514525253161-7a46d19cd819?auto=format&fit=crop&w=1800&q=80")
        center / cover;
    }

    .hero-content {
      width: 100%;
      max-width: 800px;
    }

    .hero h1 {
      font-size: clamp(40px, 7vw, 76px);
      font-weight: 900;
      letter-spacing: 3px;
      margin-bottom: 15px;
    }

    .hero p {
      color: #ddd;
      font-size: 18px;
      margin-bottom: 35px;
    }

    .search-box {
      max-width: 700px;
      margin: auto;
      background: #fff;
      padding: 8px;
      border-radius: 12px;

      display: flex;
      gap: 8px;
    }

    .search-box select,
    .search-box input {
      border: none;
      outline: none;
      padding: 15px;
      font-size: 16px;
      background: #fff;
      color: #222;
    }

    .search-box select {
      width: 150px;
    }

    .search-box input {
      flex: 1;
    }

    .search-btn {
      border: none;
      padding: 0 25px;
      border-radius: 8px;

      background: #d9a441;
      color: #111;

      font-size: 16px;
      font-weight: 700;
      cursor: pointer;
    }

    .search-btn:hover {
      background: #f0c15d;
    }

    /* ===== 共用區塊 ===== */

    section {
      max-width: 1200px;
      margin: auto;
      padding: 70px 24px;
    }

    .section-title {
      margin-bottom: 30px;
    }

    .section-title h2 {
      font-size: 30px;
    }

    .section-title p {
      color: #888;
      margin-top: 5px;
    }

    /* ===== 分類 ===== */

    .categories {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
    }

    .category {
      padding: 28px 15px;
      background: #151519;
      border: 1px solid #28282d;
      border-radius: 12px;

      text-align: center;
      transition: .25s;
    }

    .category:hover {
      transform: translateY(-5px);
      border-color: #d9a441;
    }

    .category-icon {
      font-size: 32px;
      margin-bottom: 8px;
    }

    .category span {
      color: #aaa;
      font-size: 14px;
    }

    /* ===== 店家卡片 ===== */

    .shops {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .shop-card {
      overflow: hidden;
      background: #151519;
      border: 1px solid #29292d;
      border-radius: 14px;

      transition: .25s;
    }

    .shop-card:hover {
      transform: translateY(-5px);
      border-color: #d9a441;
    }

    .shop-image {
      height: 220px;
      background-size: cover;
      background-position: center;
    }

    .shop-content {
      padding: 20px;
    }

    .shop-content h3 {
      font-size: 20px;
      margin-bottom: 5px;
    }

    .rating {
      color: #d9a441;
      margin-bottom: 8px;
    }

    .location {
      color: #999;
      font-size: 14px;
    }

    .shop-btn {
      display: inline-block;
      margin-top: 15px;

      padding: 9px 16px;
      border-radius: 7px;

      background: #242429;
      color: #fff;
      font-size: 14px;
    }

    .shop-btn:hover {
      background: #d9a441;
      color: #111;
    }

    /* ===== 排行榜 ===== */

    .ranking {
      background: #111114;
      border-top: 1px solid #222;
      border-bottom: 1px solid #222;
    }

    .ranking-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .rank-item {
      display: flex;
      align-items: center;
      gap: 20px;

      padding: 18px 20px;

      background: #18181c;
      border-radius: 10px;
    }

    .rank-number {
      width: 40px;
      font-size: 24px;
      font-weight: 900;
      color: #d9a441;
    }

    .rank-name {
      flex: 1;
    }

    .rank-score {
      color: #d9a441;
    }

    /* ===== Footer ===== */

    footer {
      background: #070708;
      border-top: 1px solid #222;
      padding: 45px 20px;
      text-align: center;
      color: #777;
    }

    footer .footer-logo {
      color: #d9a441;
      font-size: 22px;
      font-weight: 900;
      margin-bottom: 15px;
    }

    .footer-links {
      display: flex;
      justify-content: center;
      gap: 25px;
      margin-bottom: 20px;
      font-size: 14px;
    }

    /* ===== 手機版 ===== */

    @media (max-width: 768px) {

      .menu {
        display: none;
      }

      .menu-btn {
        display: block;
      }

      .hero {
        min-height: 520px;
      }

      .search-box {
        flex-direction: column;
      }

      .search-box select,
      .search-box input {
        width: 100%;
      }

      .search-btn {
        padding: 15px;
      }

      .categories {
        grid-template-columns: repeat(2, 1fr);
      }

      .shops {
        grid-template-columns: 1fr;
      }

      section {
        padding: 50px 18px;
      }

      .footer-links {
        flex-wrap: wrap;
      }
    }

    @media (max-width: 420px) {

      .hero h1 {
        font-size: 40px;
      }

      .categories {
        grid-template-columns: 1fr 1fr;
      }

      .nav {
        padding: 0 18px;
      }
    }
  </style>
</head>

<body>

  <!-- 導覽列 -->

  <header>
    <nav class="nav">

      <a href="#" class="logo">
        NIGHT LIFE
      </a>

      <ul class="menu">
        <li><a href="#">首頁</a></li>
        <li><a href="#categories">娛樂分類</a></li>
        <li><a href="#shops">熱門店家</a></li>
        <li><a href="#ranking">排行榜</a></li>
        <li><a href="#about">關於我們</a></li>
      </ul>

      <div class="menu-btn">
        ☰
      </div>

    </nav>
  </header>


  <!-- 首頁主視覺 -->

  <div class="hero">

    <div class="hero-content">

      <h1>今晚，去哪裡？</h1>

      <p>
        探索熱門夜生活與娛樂場所
      </p>

      <div class="search-box">

        <select>
          <option>📍 台中市</option>
          <option>📍 台北市</option>
          <option>📍 新竹市</option>
          <option>📍 高雄市</option>
        </select>

        <input
          type="text"
          placeholder="搜尋店家、娛樂類型..."
        >

        <button class="search-btn">
          搜尋
        </button>

      </div>

    </div>

  </div>


  <!-- 分類 -->

  <section id="categories">

    <div class="section-title">
      <h2>🎯 選擇娛樂類型</h2>
      <p>找到適合你的夜生活</p>
    </div>

    <div class="categories">

      <a href="#" class="category">
        <div class="category-icon">🍸</div>
        <strong>酒吧</strong>
        <br>
        <span>Bar</span>
      </a>

      <a href="#" class="category">
        <div class="category-icon">🎤</div>
        <strong>KTV</strong>
        <br>
        <span>Karaoke</span>
      </a>

      <a href="#" class="category">
        <div class="category-icon">🌙</div>
        <strong>夜店</strong>
        <br>
        <span>Night Club</span>
      </a>

      <a href="#" class="category">
        <div class="category-icon">🥂</div>
        <strong>會所</strong>
        <br>
        <span>Lounge</span>
      </a>

    </div>

  </section>


  <!-- 熱門店家 -->

  <section id="shops">

    <div class="section-title">
      <h2>🔥 本週熱門</h2>
      <p>大家最近正在關注的店家</p>
    </div>

    <div class="shops">


      <!-- 店家 1 -->

      <article class="shop-card">

        <div
          class="shop-image"
          style="background-image:url('https://images.unsplash.com/photo-1514933651103-005eec06c04b?auto=format&fit=crop&w=900&q=80')">
        </div>

        <div class="shop-content">

          <h3>Golden Lounge</h3>

          <div class="rating">
            ★★★★★ 4.8
          </div>

          <div class="location">
            📍 台中・西屯區
          </div>

          <a href="#" class="shop-btn">
            查看詳情 →
          </a>

        </div>

      </article>


      <!-- 店家 2 -->

      <article class="shop-card">

        <div
          class="shop-image"
          style="background-image:url('https://images.unsplash.com/photo-1572116469696-31de0f17cc34?auto=format&fit=crop&w=900&q=80')">
        </div>

        <div class="shop-content">

          <h3>Night House</h3>

          <div class="rating">
            ★★★★★ 4.7
          </div>

          <div class="location">
            📍 台中・北區
          </div>

          <a href="#" class="shop-btn">
            查看詳情 →
          </a>

        </div>

      </article>


      <!-- 店家 3 -->

      <article class="shop-card">

        <div
          class="shop-image"
          style="background-image:url('https://images.unsplash.com/photo-1566737236500-c8ac43014a8e?auto=format&fit=crop&w
