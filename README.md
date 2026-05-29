
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ogen & Anastasia — 19.06.2026</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@300;400&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #f5efe6;
    --parchment: #ede3d6;
    --dark: #2a2118;
    --brown: #4a3728;
    --light-brown: #8c6e57;
    --gold: #c9a96e;
    --line: #c4b09a;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }

  body {
    background: var(--cream);
    color: var(--dark);
    font-family: 'Cormorant Garamond', serif;
    overflow-x: hidden;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 1000;
    opacity: 0.5;
  }

  /* ─── HERO ─── */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    padding: 60px 24px 80px;
    text-align: center;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse at 50% 30%, #e8d9c5 0%, var(--cream) 70%);
  }

  .hero > * { position: relative; z-index: 1; }

  .chandelier {
    width: 140px;
    margin-bottom: 28px;
    opacity: 0;
    animation: fadeDown 1.2s ease forwards 0.3s;
  }

  .garland {
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 220px;
    pointer-events: none;
    opacity: 0;
    animation: fadeIn 1.6s ease forwards 0.6s;
  }

  .hero-pre {
    font-family: 'Montserrat', sans-serif;
    font-size: 11px;
    font-weight: 300;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--light-brown);
    margin-bottom: 18px;
    opacity: 0;
    animation: fadeUp 1s ease forwards 0.8s;
  }

  .names {
    font-family: 'Playfair Display', serif;
    font-size: clamp(56px, 14vw, 96px);
    font-weight: 700;
    line-height: 0.9;
    color: var(--dark);
    letter-spacing: -1px;
    opacity: 0;
    animation: fadeUp 1s ease forwards 1s;
  }

  .names .italic {
    font-style: italic;
    font-weight: 400;
    color: var(--brown);
  }

  .names .script {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 0.55em;
    color: var(--light-brown);
    display: block;
    margin: 4px 0;
  }

  .divider-ornament {
    width: 200px;
    height: 1px;
    background: linear-gradient(to right, transparent, var(--gold), transparent);
    margin: 32px auto;
    opacity: 0;
    animation: fadeIn 1s ease forwards 1.2s;
    position: relative;
  }

  .divider-ornament::before, .divider-ornament::after {
    content: '◆';
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 8px;
    color: var(--gold);
  }
  .divider-ornament::before { left: 30px; }
  .divider-ornament::after { right: 30px; }

  .save-the-date {
    font-family: 'Montserrat', sans-serif;
    font-size: 11px;
    font-weight: 300;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--light-brown);
    margin-bottom: 12px;
    opacity: 0;
    animation: fadeUp 1s ease forwards 1.3s;
  }

  .date-display {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(36px, 10vw, 64px);
    font-weight: 300;
    color: var(--dark);
    letter-spacing: 6px;
    opacity: 0;
    animation: fadeUp 1s ease forwards 1.4s;
  }

  .date-display span {
    color: var(--light-brown);
    font-weight: 300;
    margin: 0 8px;
  }

  .tagline {
    font-style: italic;
    font-size: 18px;
    color: var(--light-brown);
    margin-top: 14px;
    letter-spacing: 1px;
    opacity: 0;
    animation: fadeUp 1s ease forwards 1.6s;
  }

  .scroll-hint {
    position: absolute;
    bottom: 32px;
    left: 50%;
    transform: translateX(-50%);
    text-align: center;
    opacity: 0;
    animation: fadeIn 1s ease forwards 2.2s;
  }

  .scroll-hint p {
    font-family: 'Montserrat', sans-serif;
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--light-brown);
    margin-bottom: 8px;
  }

  .scroll-arrow {
    width: 1px;
    height: 40px;
    background: linear-gradient(to bottom, var(--gold), transparent);
    margin: 0 auto;
    animation: scrollPulse 2s ease-in-out infinite;
  }

  /* ─── SECTION COMMON ─── */
  section {
    padding: 80px 24px;
    max-width: 680px;
    margin: 0 auto;
    position: relative;
  }

  .section-label {
    font-family: 'Montserrat', sans-serif;
    font-size: 9px;
    font-weight: 400;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 20px;
    display: block;
    text-align: center;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(30px, 7vw, 46px);
    font-weight: 400;
    font-style: italic;
    color: var(--dark);
    text-align: center;
    margin-bottom: 48px;
    line-height: 1.2;
  }

  /* ─── SCHEDULE ─── */
  .schedule-section {
    background: var(--parchment);
    max-width: 100%;
    padding: 80px 24px;
  }

  .schedule-section .inner {
    max-width: 620px;
    margin: 0 auto;
  }

  .schedule-frame {
    border: 1px solid var(--line);
    padding: 48px 32px;
    position: relative;
  }

  .corner-tl { position:absolute; top:-1px; left:-1px; width:20px; height:20px; border-top:2px solid var(--gold); border-left:2px solid var(--gold); }
  .corner-tr { position:absolute; top:-1px; right:-1px; width:20px; height:20px; border-top:2px solid var(--gold); border-right:2px solid var(--gold); }
  .corner-bl { position:absolute; bottom:-1px; left:-1px; width:20px; height:20px; border-bottom:2px solid var(--gold); border-left:2px solid var(--gold); }
  .corner-br { position:absolute; bottom:-1px; right:-1px; width:20px; height:20px; border-bottom:2px solid var(--gold); border-right:2px solid var(--gold); }

  .timeline { list-style: none; position: relative; }

  .timeline::before {
    content: '';
    position: absolute;
    left: 70px;
    top: 6px; bottom: 6px;
    width: 1px;
    background: linear-gradient(to bottom, transparent, var(--line) 10%, var(--line) 90%, transparent);
  }

  .timeline li {
    display: flex;
    align-items: flex-start;
    gap: 28px;
    margin-bottom: 36px;
    position: relative;
  }
  .timeline li:last-child { margin-bottom: 0; }

  .t-time {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    font-weight: 300;
    color: var(--brown);
    min-width: 70px;
    text-align: right;
    padding-top: 2px;
    letter-spacing: 1px;
  }

  .t-dot { position: relative; flex-shrink: 0; margin-top: 10px; }
  .t-dot::before {
    content: '';
    display: block;
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--gold);
    border: 1px solid var(--light-brown);
    margin-left: -3.5px;
  }

  .t-info { padding-top: 2px; }

  .t-title {
    font-family: 'Playfair Display', serif;
    font-size: 20px;
    font-weight: 400;
    color: var(--dark);
    margin-bottom: 4px;
    line-height: 1.2;
  }

  .t-detail {
    font-family: 'Montserrat', sans-serif;
    font-size: 11px;
    font-weight: 300;
    letter-spacing: 1.5px;
    color: var(--light-brown);
    line-height: 1.5;
  }

  /* ─── MAP BUTTON ─── */
  .map-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    margin-top: 8px;
    padding: 7px 16px 7px 12px;
    border: 1px solid var(--line);
    background: transparent;
    color: var(--brown);
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    font-weight: 400;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }

  .map-btn::before {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--dark);
    transform: translateX(-101%);
    transition: transform 0.3s ease;
  }

  .map-btn:hover::before { transform: translateX(0); }
  .map-btn:hover { color: var(--cream); border-color: var(--dark); }
  .map-btn span, .map-btn svg { position: relative; z-index: 1; }

  /* ─── VENUE ─── */
  .venue-section { text-align: center; }

  .venue-card {
    border: 1px solid var(--line);
    padding: 48px 32px;
    position: relative;
    margin-top: 32px;
  }

  .venue-name {
    font-family: 'Playfair Display', serif;
    font-size: 32px;
    font-style: italic;
    color: var(--dark);
    margin-bottom: 8px;
  }

  .venue-sub {
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 20px;
  }

  .venue-address {
    font-family: 'Cormorant Garamond', serif;
    font-size: 17px;
    font-weight: 300;
    color: var(--brown);
    line-height: 1.6;
    margin-bottom: 28px;
  }

  .venue-map-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 12px 28px;
    background: var(--dark);
    color: var(--cream);
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    font-weight: 400;
    letter-spacing: 3px;
    text-transform: uppercase;
    text-decoration: none;
    border: 1px solid var(--dark);
    transition: all 0.3s ease;
  }
  .venue-map-btn:hover { background: transparent; color: var(--dark); }

  /* ─── COUNTDOWN ─── */
  .countdown-section {
    background: var(--dark);
    max-width: 100%;
    padding: 72px 24px;
    text-align: center;
  }

  .countdown-section .section-label { color: var(--gold); }
  .countdown-section .section-title { color: var(--cream); }

  .countdown-grid {
    display: flex;
    justify-content: center;
    gap: clamp(16px, 4vw, 48px);
    flex-wrap: wrap;
    max-width: 560px;
    margin: 0 auto;
  }

  .c-unit { text-align: center; min-width: 80px; }

  .c-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(48px, 12vw, 80px);
    font-weight: 300;
    color: var(--cream);
    line-height: 1;
    letter-spacing: -2px;
  }

  .c-label {
    font-family: 'Montserrat', sans-serif;
    font-size: 9px;
    font-weight: 300;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gold);
    margin-top: 6px;
  }

  .c-sep {
    font-family: 'Cormorant Garamond', serif;
    font-size: 60px;
    font-weight: 300;
    color: var(--light-brown);
    line-height: 1;
    margin-top: 4px;
    opacity: 0.4;
  }

  /* ─── FOOTER ─── */
  footer {
    background: var(--parchment);
    text-align: center;
    padding: 56px 24px;
    border-top: 1px solid var(--line);
  }

  .footer-names {
    font-family: 'Playfair Display', serif;
    font-size: 28px;
    font-style: italic;
    color: var(--dark);
    margin-bottom: 12px;
  }

  .footer-date {
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--light-brown);
  }

  .footer-initials {
    font-family: 'Playfair Display', serif;
    font-size: clamp(72px, 18vw, 120px);
    font-style: italic;
    font-weight: 400;
    color: transparent;
    -webkit-text-stroke: 1px var(--line);
    letter-spacing: 16px;
    margin-top: 32px;
    line-height: 1;
    user-select: none;
  }

  /* ─── ANIMATIONS ─── */
  @keyframes fadeDown {
    from { opacity:0; transform: translateY(-20px); }
    to   { opacity:1; transform: translateY(0); }
  }
  @keyframes fadeUp {
    from { opacity:0; transform: translateY(24px); }
    to   { opacity:1; transform: translateY(0); }
  }
  @keyframes fadeIn {
    from { opacity:0; }
    to   { opacity:1; }
  }
  @keyframes scrollPulse {
    0%,100% { transform: scaleY(1); opacity:1; }
    50%      { transform: scaleY(0.6); opacity:.5; }
  }

  .reveal {
    opacity: 0;
    transform: translateY(32px);
    transition: opacity .8s ease, transform .8s ease;
  }
  .reveal.visible { opacity:1; transform: translateY(0); }

  @media (max-width:480px) {
    .timeline::before { left:60px; }
    .t-time { min-width:60px; font-size:18px; }
    .schedule-frame { padding:32px 16px; }
    .c-sep { display:none; }
  }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <svg class="garland" viewBox="0 0 800 220" fill="none" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid meet">
    <path d="M0,40 Q100,100 200,60 Q300,20 400,70 Q500,120 600,60 Q700,20 800,50" stroke="#c4b09a" stroke-width="1" fill="none"/>
    <path d="M0,30 Q150,90 300,50 Q450,10 600,50 Q700,80 800,40" stroke="#c4b09a" stroke-width="0.7" fill="none" opacity="0.5"/>
    <circle cx="100" cy="72" r="3" fill="#c9a96e" opacity="0.6"/>
    <circle cx="230" cy="52" r="3" fill="#c9a96e" opacity="0.6"/>
    <circle cx="400" cy="70" r="4" fill="#c9a96e" opacity="0.7"/>
    <circle cx="560" cy="52" r="3" fill="#c9a96e" opacity="0.6"/>
    <circle cx="700" cy="30" r="3" fill="#c9a96e" opacity="0.6"/>
  </svg>

  <svg class="chandelier" viewBox="0 0 140 160" fill="none" xmlns="http://www.w3.org/2000/svg">
    <line x1="70" y1="0" x2="70" y2="28" stroke="#8c6e57" stroke-width="1"/>
    <ellipse cx="70" cy="38" rx="10" ry="6" stroke="#4a3728" stroke-width="1.2" fill="none"/>
    <line x1="70" y1="44" x2="70" y2="62" stroke="#4a3728" stroke-width="1"/>
    <circle cx="70" cy="64" r="4" stroke="#4a3728" stroke-width="1" fill="none"/>
    <path d="M70,48 Q45,52 38,70" stroke="#4a3728" stroke-width="1.2" fill="none"/>
    <path d="M70,48 Q95,52 102,70" stroke="#4a3728" stroke-width="1.2" fill="none"/>
    <path d="M70,50 Q55,54 50,70" stroke="#4a3728" stroke-width="1" fill="none"/>
    <path d="M70,50 Q85,54 90,70" stroke="#4a3728" stroke-width="1" fill="none"/>
    <rect x="34" y="68" width="7" height="16" rx="1" stroke="#4a3728" stroke-width="1" fill="none"/>
    <line x1="37.5" y1="66" x2="37.5" y2="68" stroke="#4a3728" stroke-width="1"/>
    <ellipse cx="37.5" cy="65" rx="2" ry="2.5" fill="#c9a96e" opacity="0.7"/>
    <rect x="98" y="68" width="7" height="16" rx="1" stroke="#4a3728" stroke-width="1" fill="none"/>
    <line x1="101.5" y1="66" x2="101.5" y2="68" stroke="#4a3728" stroke-width="1"/>
    <ellipse cx="101.5" cy="65" rx="2" ry="2.5" fill="#c9a96e" opacity="0.7"/>
    <rect x="46" y="68" width="7" height="14" rx="1" stroke="#4a3728" stroke-width="1" fill="none"/>
    <line x1="49.5" y1="66" x2="49.5" y2="68" stroke="#4a3728" stroke-width="1"/>
    <ellipse cx="49.5" cy="65" rx="2" ry="2.5" fill="#c9a96e" opacity="0.7"/>
    <rect x="86" y="68" width="7" height="14" rx="1" stroke="#4a3728" stroke-width="1" fill="none"/>
    <line x1="89.5" y1="66" x2="89.5" y2="68" stroke="#4a3728" stroke-width="1"/>
    <ellipse cx="89.5" cy="65" rx="2" ry="2.5" fill="#c9a96e" opacity="0.7"/>
    <line x1="37.5" y1="84" x2="37.5" y2="96" stroke="#8c6e57" stroke-width="0.8" opacity="0.6"/>
    <ellipse cx="37.5" cy="99" rx="3" ry="4" stroke="#8c6e57" stroke-width="0.8" fill="none" opacity="0.6"/>
    <line x1="70" y1="68" x2="70" y2="80" stroke="#8c6e57" stroke-width="0.8" opacity="0.6"/>
    <ellipse cx="70" cy="83" rx="3" ry="4" stroke="#8c6e57" stroke-width="0.8" fill="none" opacity="0.6"/>
    <line x1="101.5" y1="84" x2="101.5" y2="96" stroke="#8c6e57" stroke-width="0.8" opacity="0.6"/>
    <ellipse cx="101.5" cy="99" rx="3" ry="4" stroke="#8c6e57" stroke-width="0.8" fill="none" opacity="0.6"/>
  </svg>

  <p class="hero-pre">приглашение на свадьбу</p>

  <div class="names">
    <span>Ogen</span>
    <span class="script">&amp; Wedding day &amp;</span>
    <span class="italic">Anastasia</span>
  </div>

  <div class="divider-ornament"></div>

  <p class="save-the-date">Save the date</p>
  <div class="date-display">19<span>|</span>06<span>|</span>2026</div>
  <p class="tagline">До скорой встречи</p>

  <div class="scroll-hint">
    <p>Листайте вниз</p>
    <div class="scroll-arrow"></div>
  </div>
</section>


<!-- SCHEDULE -->
<div class="schedule-section">
  <div class="inner">
    <span class="section-label reveal">Программа дня</span>
    <h2 class="section-title reveal">Расписание торжества</h2>

    <div class="schedule-frame reveal">
      <div class="corner-tl"></div>
      <div class="corner-tr"></div>
      <div class="corner-bl"></div>
      <div class="corner-br"></div>

      <ul class="timeline">
        <li>
          <span class="t-time">13:45</span>
          <div class="t-dot"></div>
          <div class="t-info">
            <div class="t-title">Сбор гостей в церкви</div>
            <div class="t-detail">
              Фотосессия &amp; Церемония венчания<br>
              <a class="map-btn" href="https://yandex.ru/maps/?text=Олимпийский+проспект+9+Москва" target="_blank" rel="noopener">
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7z"/><circle cx="12" cy="9" r="2.5"/></svg>
                <span>Олимпийский проспект, 9</span>
              </a>
            </div>
          </div>
        </li>

        <li>
          <span class="t-time">16:30</span>
          <div class="t-dot"></div>
          <div class="t-info">
            <div class="t-title">Фуршет в ресторане</div>
            <div class="t-detail">La Delizia · Домодедово</div>
          </div>
        </li>

        <li>
          <span class="t-time">17:00</span>
          <div class="t-dot"></div>
          <div class="t-info">
            <div class="t-title">Начало банкета</div>
            <div class="t-detail">Торжественный вечер с семьёй и близкими</div>
          </div>
        </li>

        <li>
          <span class="t-time">00:30</span>
          <div class="t-dot"></div>
          <div class="t-info">
            <div class="t-title">Окончание вечера</div>
            <div class="t-detail">Спасибо, что были с нами ✦</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</div>


<!-- VENUE -->
<section class="venue-section">
  <span class="section-label reveal">Место проведения</span>
  <h2 class="section-title reveal">Ресторан</h2>

  <div class="venue-card reveal">
    <div class="corner-tl"></div>
    <div class="corner-tr"></div>
    <div class="corner-bl"></div>
    <div class="corner-br"></div>

    <div class="venue-name">La Delizia</div>
    <div class="venue-sub">Ресторан · Домодедово</div>
    <div class="venue-address">
      г. Домодедово<br>
      Объездное шоссе, с7
    </div>

    <a class="venue-map-btn" href="https://yandex.ru/maps/?text=La+Delizia+Домодедово+Объездное+шоссе+с7" target="_blank" rel="noopener">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7z"/><circle cx="12" cy="9" r="2.5"/></svg>
      Открыть на Яндекс Картах
    </a>
  </div>
</section>


<!-- COUNTDOWN -->
<div class="countdown-section">
  <span class="section-label reveal">До свадьбы осталось</span>
  <h2 class="section-title reveal">Обратный отсчёт</h2>

  <div class="countdown-grid">
    <div class="c-unit"><div class="c-num" id="cd-days">—</div><div class="c-label">Дней</div></div>
    <div class="c-sep">·</div>
    <div class="c-unit"><div class="c-num" id="cd-hours">—</div><div class="c-label">Часов</div></div>
    <div class="c-sep">·</div>
    <div class="c-unit"><div class="c-num" id="cd-min">—</div><div class="c-label">Минут</div></div>
    <div class="c-sep">·</div>
    <div class="c-unit"><div class="c-num" id="cd-sec">—</div><div class="c-label">Секунд</div></div>
  </div>
</div>


<!-- FOOTER -->
<footer>
  <svg width="300" height="70" viewBox="0 0 300 70" fill="none" xmlns="http://www.w3.org/2000/svg" style="margin-bottom:32px;opacity:.45;">
    <rect x="20" y="15" width="8" height="30" rx="1" stroke="#4a3728" stroke-width="1"/>
    <line x1="24" y1="13" x2="24" y2="15" stroke="#4a3728" stroke-width="1"/>
    <ellipse cx="24" cy="12" rx="2" ry="2.5" fill="#c9a96e"/>
    <path d="M55,50 L50,20 L60,20 L55,50" stroke="#4a3728" stroke-width="1" fill="none"/>
    <line x1="55" y1="50" x2="55" y2="58" stroke="#4a3728" stroke-width="1"/>
    <line x1="50" y1="58" x2="60" y2="58" stroke="#4a3728" stroke-width="1"/>
    <ellipse cx="150" cy="50" rx="38" ry="10" stroke="#4a3728" stroke-width="1" fill="none"/>
    <ellipse cx="150" cy="48" rx="28" ry="7" stroke="#4a3728" stroke-width="0.7" fill="none"/>
    <line x1="120" y1="20" x2="120" y2="45" stroke="#4a3728" stroke-width="1"/>
    <line x1="117" y1="20" x2="117" y2="30" stroke="#4a3728" stroke-width="0.8"/>
    <line x1="120" y1="20" x2="120" y2="30" stroke="#4a3728" stroke-width="0.8"/>
    <line x1="123" y1="20" x2="123" y2="30" stroke="#4a3728" stroke-width="0.8"/>
    <line x1="180" y1="20" x2="180" y2="45" stroke="#4a3728" stroke-width="1"/>
    <path d="M180,20 Q185,25 180,32" stroke="#4a3728" stroke-width="0.8" fill="none"/>
    <path d="M245,50 L240,20 L250,20 L245,50" stroke="#4a3728" stroke-width="1" fill="none"/>
    <line x1="245" y1="50" x2="245" y2="58" stroke="#4a3728" stroke-width="1"/>
    <line x1="240" y1="58" x2="250" y2="58" stroke="#4a3728" stroke-width="1"/>
    <rect x="272" y="15" width="8" height="30" rx="1" stroke="#4a3728" stroke-width="1"/>
    <line x1="276" y1="13" x2="276" y2="15" stroke="#4a3728" stroke-width="1"/>
    <ellipse cx="276" cy="12" rx="2" ry="2.5" fill="#c9a96e"/>
  </svg>

  <div class="footer-names">Ogen &amp; Anastasia</div>
  <div class="footer-date">19 · 06 · 2026</div>
  <div class="footer-initials">O &amp; A</div>
</footer>


<script>
  const wedding = new Date('2026-06-19T13:45:00');
  function tick() {
    const diff = wedding - new Date();
    if (diff <= 0) return;
    const pad = n => String(Math.floor(n)).padStart(2,'0');
    document.getElementById('cd-days').textContent  = pad(diff/86400000);
    document.getElementById('cd-hours').textContent = pad((diff%86400000)/3600000);
    document.getElementById('cd-min').textContent   = pad((diff%3600000)/60000);
    document.getElementById('cd-sec').textContent   = pad((diff%60000)/1000);
  }
  tick(); setInterval(tick, 1000);

  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); observer.unobserve(e.target); } });
  }, { threshold: 0.12 });
  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
