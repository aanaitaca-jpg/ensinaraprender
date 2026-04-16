
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ensinar &amp; Aprender Matemática</title>
  <meta name="description" content="Aprenda matemática com as coisas do seu dia a dia: mercado, cozinha, dinheiro, casa e muito mais." />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,400;0,600;0,700;1,400;1,600&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --green-dark: #1a3a2a;
      --green-mid: #3a6a4a;
      --green-light: #7ecfa0;
      --green-bg: #eaf7ee;
      --green-border: #c0e8cc;
      --amber-bg: #fff8e6;
      --amber-text: #7a5000;
      --blue-bg: #e8f0ff;
      --blue-text: #1a3a80;
      --blue-light: #eef5ff;
      --blue-light-text: #1a3070;
      --red-bg: #fdeef0;
      --red-text: #7a1a2a;
      --purple-bg: #f2eeff;
      --purple-text: #3a1a80;
      --bg: #f8f7f4;
      --surface: #ffffff;
      --surface-secondary: #f1efe8;
      --text-primary: #1c1c1a;
      --text-secondary: #5f5e5a;
      --text-hint: #888780;
      --border: rgba(0,0,0,0.12);
      --border-hover: rgba(0,0,0,0.22);
      --radius-md: 8px;
      --radius-lg: 14px;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text-primary);
      min-height: 100vh;
      line-height: 1.6;
    }

    /* ── NAV ── */
    nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(248,247,244,0.92);
      backdrop-filter: blur(10px);
      border-bottom: 0.5px solid var(--border);
      padding: 0 2rem;
    }

    .nav-inner {
      max-width: 900px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 60px;
    }

    .nav-logo {
      font-family: 'Fraunces', serif;
      font-weight: 700;
      font-size: 1.1rem;
      color: var(--green-dark);
      text-decoration: none;
    }

    .nav-logo span { color: var(--green-mid); font-style: italic; }

    .nav-links {
      display: flex;
      gap: 1.5rem;
      list-style: none;
    }

    .nav-links a {
      font-size: 14px;
      color: var(--text-secondary);
      text-decoration: none;
      transition: color 0.15s;
    }
    .nav-links a:hover { color: var(--text-primary); }

    .nav-cta {
      background: var(--green-dark);
      color: var(--green-light) !important;
      padding: 8px 18px;
      border-radius: 100px;
      font-weight: 500;
    }
    .nav-cta:hover { opacity: 0.88; }

    @media (max-width: 600px) {
      .nav-links { display: none; }
    }

    /* ── LAYOUT ── */
    .page {
      max-width: 900px;
      margin: 0 auto;
      padding: 2.5rem 1.5rem 4rem;
    }

    /* ── HERO ── */
    .hero {
      background: var(--green-dark);
      border-radius: var(--radius-lg);
      padding: 3rem 2.5rem 2.5rem;
      position: relative;
      overflow: hidden;
      margin-bottom: 2rem;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: -70px; right: -70px;
      width: 240px; height: 240px;
      border-radius: 50%;
      background: rgba(255,255,255,0.04);
    }

    .hero::after {
      content: '';
      position: absolute;
      bottom: -50px; left: 35%;
      width: 180px; height: 180px;
      border-radius: 50%;
      background: rgba(255,255,255,0.03);
    }

    .hero-tag {
      display: inline-block;
      background: rgba(255,255,255,0.12);
      color: #a8d8b0;
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.09em;
      text-transform: uppercase;
      padding: 5px 14px;
      border-radius: 100px;
      margin-bottom: 1.25rem;
    }

    .hero h1 {
      font-family: 'Fraunces', serif;
      font-size: clamp(2rem, 5vw, 3.2rem);
      font-weight: 700;
      color: #fff;
      line-height: 1.15;
      margin-bottom: 1rem;
      max-width: 560px;
    }

    .hero h1 em {
      font-style: italic;
      color: #7ecfa0;
    }

    .hero p {
      font-size: 16px;
      color: rgba(255,255,255,0.72);
      line-height: 1.7;
      max-width: 480px;
      margin-bottom: 1.75rem;
    }

    .hero-btns {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    .btn-primary {
      background: var(--green-light);
      color: var(--green-dark);
      border: none;
      padding: 12px 26px;
      border-radius: 100px;
      font-size: 14px;
      font-weight: 500;
      font-family: 'DM Sans', sans-serif;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
      transition: opacity 0.15s, transform 0.12s;
    }
    .btn-primary:hover { opacity: 0.88; transform: translateY(-1px); }

    .btn-secondary {
      background: transparent;
      color: rgba(255,255,255,0.82);
      border: 0.5px solid rgba(255,255,255,0.32);
      padding: 12px 26px;
      border-radius: 100px;
      font-size: 14px;
      font-family: 'DM Sans', sans-serif;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
      transition: border-color 0.15s;
    }
    .btn-secondary:hover { border-color: rgba(255,255,255,0.6); }

    .hero-stats {
      display: flex;
      gap: 2.5rem;
      margin-top: 2.5rem;
      padding-top: 2rem;
      border-top: 0.5px solid rgba(255,255,255,0.12);
      flex-wrap: wrap;
    }

    .stat { display: flex; flex-direction: column; gap: 2px; }
    .stat-num { font-family: 'Fraunces', serif; font-size: 1.9rem; font-weight: 600; color: #fff; }
    .stat-label { font-size: 12px; color: rgba(255,255,255,0.48); }

    /* ── CHALLENGE BANNER ── */
    .challenge-banner {
      border-radius: var(--radius-lg);
      padding: 1.5rem 2rem;
      background: var(--green-bg);
      border: 0.5px solid var(--green-border);
      margin-bottom: 2.5rem;
      display: flex;
      align-items: center;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .challenge-icon { font-size: 2.4rem; flex-shrink: 0; }

    .challenge-content h3 {
      font-family: 'Fraunces', serif;
      font-size: 1.05rem;
      font-weight: 600;
      color: var(--green-dark);
      margin-bottom: 4px;
    }

    .challenge-content p {
      font-size: 13px;
      color: var(--green-mid);
      line-height: 1.5;
    }

    .challenge-btn {
      margin-left: auto;
      background: var(--green-dark);
      color: var(--green-light);
      border: none;
      padding: 11px 22px;
      border-radius: 100px;
      font-size: 13px;
      font-weight: 500;
      font-family: 'DM Sans', sans-serif;
      cursor: pointer;
      white-space: nowrap;
      text-decoration: none;
      transition: opacity 0.15s;
    }
    .challenge-btn:hover { opacity: 0.85; }

    /* ── SECTION HEADERS ── */
    .section-label {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.09em;
      text-transform: uppercase;
      color: var(--text-hint);
      margin-bottom: 0.6rem;
    }

    .section-title {
      font-family: 'Fraunces', serif;
      font-size: 1.65rem;
      font-weight: 600;
      color: var(--text-primary);
      margin-bottom: 0.5rem;
    }

    .section-sub {
      font-size: 15px;
      color: var(--text-secondary);
      margin-bottom: 1.75rem;
      line-height: 1.65;
      max-width: 560px;
    }

    /* ── TOPICS GRID ── */
    .topics-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 16px;
      margin-bottom: 2.75rem;
    }

    .topic-card {
      background: var(--surface);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 1.25rem;
      cursor: pointer;
      text-decoration: none;
      display: block;
      transition: border-color 0.15s, transform 0.12s, box-shadow 0.12s;
      color: inherit;
    }
    .topic-card:hover {
      border-color: var(--border-hover);
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(0,0,0,0.07);
    }

    .topic-icon {
      width: 42px; height: 42px;
      border-radius: var(--radius-md);
      display: flex; align-items: center; justify-content: center;
      margin-bottom: 0.85rem;
      font-size: 20px;
    }

    .topic-card h3 {
      font-size: 14px;
      font-weight: 500;
      color: var(--text-primary);
      margin-bottom: 6px;
    }

    .topic-card p {
      font-size: 13px;
      color: var(--text-secondary);
      line-height: 1.55;
    }

    .topic-tag {
      display: inline-block;
      font-size: 11px;
      padding: 3px 11px;
      border-radius: 100px;
      margin-top: 12px;
      font-weight: 500;
    }

    /* ── ACTIVITIES ── */
    .featured-section {
      background: var(--surface-secondary);
      border-radius: var(--radius-lg);
      padding: 2rem 2rem 2.25rem;
      margin-bottom: 2.5rem;
    }

    .activities { display: flex; flex-direction: column; gap: 12px; }

    .activity-row {
      display: flex;
      align-items: flex-start;
      gap: 14px;
      background: var(--surface);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-md);
      padding: 1rem 1.1rem;
      cursor: pointer;
      text-decoration: none;
      color: inherit;
      transition: border-color 0.15s, transform 0.1s;
    }
    .activity-row:hover {
      border-color: var(--border-hover);
      transform: translateX(3px);
    }

    .activity-num {
      width: 34px; height: 34px;
      border-radius: 50%;
      background: var(--green-dark);
      color: var(--green-light);
      font-size: 13px;
      font-weight: 500;
      display: flex; align-items: center; justify-content: center;
      flex-shrink: 0;
      font-family: 'Fraunces', serif;
    }

    .activity-body { flex: 1; }
    .activity-body h4 { font-size: 14px; font-weight: 500; color: var(--text-primary); margin-bottom: 4px; }
    .activity-body p { font-size: 13px; color: var(--text-secondary); line-height: 1.5; }

    .activity-level {
      font-size: 11px;
      font-weight: 500;
      padding: 4px 11px;
      border-radius: 100px;
      flex-shrink: 0;
      align-self: flex-start;
      white-space: nowrap;
    }

    /* ── TWO COLS ── */
    .two-col {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
      margin-bottom: 2.5rem;
    }

    @media (max-width: 600px) {
      .two-col { grid-template-columns: 1fr; }
      .hero { padding: 2rem 1.5rem; }
      .hero-stats { gap: 1.5rem; }
      .challenge-banner { flex-direction: column; align-items: flex-start; }
      .challenge-btn { margin-left: 0; }
    }

    /* ── QUOTE ── */
    .quote-card {
      background: var(--green-dark);
      border-radius: var(--radius-lg);
      padding: 1.75rem;
      color: #fff;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .quote-card blockquote {
      font-family: 'Fraunces', serif;
      font-size: 1.05rem;
      font-style: italic;
      line-height: 1.65;
      color: rgba(255,255,255,0.88);
      margin-bottom: 1.5rem;
    }

    .quote-attr { font-size: 12px; color: rgba(255,255,255,0.42); }

    /* ── CTA CARD ── */
    .cta-card {
      background: var(--surface);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 1.75rem;
      display: flex;
      flex-direction: column;
      gap: 14px;
    }

    .cta-card h3 {
      font-family: 'Fraunces', serif;
      font-size: 1.1rem;
      font-weight: 600;
      color: var(--text-primary);
    }

    .cta-card p {
      font-size: 13px;
      color: var(--text-secondary);
      line-height: 1.55;
    }

    .cta-input { display: flex; gap: 8px; flex-wrap: wrap; }

    .cta-input input {
      flex: 1;
      min-width: 160px;
      font-size: 13px;
      padding: 10px 14px;
      border: 0.5px solid var(--border);
      border-radius: var(--radius-md);
      background: var(--surface);
      color: var(--text-primary);
      font-family: 'DM Sans', sans-serif;
      outline: none;
      transition: border-color 0.15s;
    }
    .cta-input input:focus { border-color: var(--border-hover); }
    .cta-input input::placeholder { color: var(--text-hint); }

    .cta-input button {
      background: var(--green-dark);
      color: var(--green-light);
      border: none;
      padding: 10px 20px;
      border-radius: var(--radius-md);
      font-size: 13px;
      font-weight: 500;
      font-family: 'DM Sans', sans-serif;
      cursor: pointer;
      transition: opacity 0.15s;
    }
    .cta-input button:hover { opacity: 0.85; }

    /* ── FOOTER ── */
    footer {
      border-top: 0.5px solid var(--border);
      padding: 2rem 1.5rem;
      text-align: center;
    }

    .footer-inner {
      max-width: 900px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
    }

    .footer-logo {
      font-family: 'Fraunces', serif;
      font-weight: 700;
      font-size: 1.05rem;
      color: var(--green-dark);
    }

    .footer-logo span { font-style: italic; color: var(--green-mid); }

    footer p {
      font-size: 12px;
      color: var(--text-hint);
    }

    footer a {
      color: var(--green-mid);
      text-decoration: none;
      font-size: 12px;
    }
    footer a:hover { text-decoration: underline; }

    /* ── TOAST ── */
    #toast {
      position: fixed;
      bottom: 1.5rem;
      left: 50%;
      transform: translateX(-50%) translateY(80px);
      background: var(--green-dark);
      color: var(--green-light);
      padding: 10px 22px;
      border-radius: 100px;
      font-size: 13px;
      font-weight: 500;
      opacity: 0;
      transition: transform 0.3s ease, opacity 0.3s ease;
      pointer-events: none;
      z-index: 999;
      white-space: nowrap;
    }
    #toast.show {
      transform: translateX(-50%) translateY(0);
      opacity: 1;
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#" class="nav-logo">Ensinar &amp; <span>Aprender</span></a>
    <ul class="nav-links">
      <li><a href="#temas">Temas</a></li>
      <li><a href="#atividades">Atividades</a></li>
      <li><a href="#desafio">Desafio</a></li>
      <li><a href="#contato" class="nav-cta">Inscreva-se</a></li>
    </ul>
  </div>
</nav>

<!-- PAGE -->
<main class="page">

  <!-- HERO -->
  <section class="hero" id="inicio">
    <div class="hero-tag">Projeto Educacional</div>
    <h1>Ensinar &amp; <em>Aprender</em> Matemática</h1>
    <p>Matemática está em todo lugar — no mercado, na cozinha, no troco, na receita. Aqui você aprende de verdade, com as coisas do seu dia a dia.</p>
    <div class="hero-btns">
      <a href="#temas" class="btn-primary">Começar agora →</a>
      <a href="#atividades" class="btn-secondary">Ver atividades</a>
    </div>
    <div class="hero-stats">
      <div class="stat"><span class="stat-num">6</span><span class="stat-label">Temas do cotidiano</span></div>
      <div class="stat"><span class="stat-num">30+</span><span class="stat-label">Atividades práticas</span></div>
      <div class="stat"><span class="stat-num">100%</span><span class="stat-label">Gratuito e acessível</span></div>
    </div>
  </section>

  <!-- CHALLENGE BANNER -->
  <section class="challenge-banner" id="desafio">
    <span class="challenge-icon">🧮</span>
    <div class="challenge-content">
      <h3>Desafio da semana: O troco certo</h3>
      <p>Você comprou R$47,50 em produtos e pagou com R$50,00. Quanto deve receber de troco? Descubra o raciocínio por trás!</p>
    </div>
    <a href="#contato" class="challenge-btn">Participar →</a>
  </section>

  <!-- TOPICS -->
  <section id="temas">
    <p class="section-label">Temas principais</p>
    <h2 class="section-title">Matemática em todo lugar</h2>
    <p class="section-sub">Cada tema usa situações reais para você entender os conceitos de forma natural e duradoura.</p>
    <div class="topics-grid">

      <a href="#" class="topic-card" onclick="showToast('Abrindo Mercado e Feira Livre…'); return false;">
        <div class="topic-icon" style="background:#eaf7ee;">🛒</div>
        <h3>Mercado e Feira Livre</h3>
        <p>Preços, peso, volume, comparação de produtos e calcular o troco na hora.</p>
        <span class="topic-tag" style="background:#eaf7ee; color:#1a5c2a;">Números e operações</span>
      </a>

      <a href="#" class="topic-card" onclick="showToast('Abrindo Cozinha e Receitas…'); return false;">
        <div class="topic-icon" style="background:#fff8e6;">🍳</div>
        <h3>Cozinha e Receitas</h3>
        <p>Frações na hora de dobrar receitas, medidas de colher e xícara, proporção.</p>
        <span class="topic-tag" style="background:#fff8e6; color:#7a5000;">Frações e proporção</span>
      </a>

      <a href="#" class="topic-card" onclick="showToast('Abrindo Dinheiro e Finanças…'); return false;">
        <div class="topic-icon" style="background:#e8f0ff;">💰</div>
        <h3>Dinheiro e Finanças</h3>
        <p>Porcentagem de desconto, juros do cartão e como planejar gastos do mês.</p>
        <span class="topic-tag" style="background:#e8f0ff; color:#1a3a80;">Porcentagem e juros</span>
      </a>

      <a href="#" class="topic-card" onclick="showToast('Abrindo Casa e Construção…'); return false;">
        <div class="topic-icon" style="background:#fdeef0;">🏠</div>
        <h3>Casa e Construção</h3>
        <p>Área do quarto, quantidade de piso, pintura de paredes e medições práticas.</p>
        <span class="topic-tag" style="background:#fdeef0; color:#7a1a2a;">Geometria e medidas</span>
      </a>

      <a href="#" class="topic-card" onclick="showToast('Abrindo Viagens e Transporte…'); return false;">
        <div class="topic-icon" style="background:#eef5ff;">🚌</div>
        <h3>Viagens e Transporte</h3>
        <p>Velocidade média, tempo de viagem e consumo de combustível na estrada.</p>
        <span class="topic-tag" style="background:#eef5ff; color:#1a3070;">Velocidade e tempo</span>
      </a>

      <a href="#" class="topic-card" onclick="showToast('Abrindo Dados do Cotidiano…'); return false;">
        <div class="topic-icon" style="background:#f2eeff;">📊</div>
        <h3>Dados do Cotidiano</h3>
        <p>Leitura de gráficos, médias e estatísticas em notícias e pesquisas do dia a dia.</p>
        <span class="topic-tag" style="background:#f2eeff; color:#3a1a80;">Estatística básica</span>
      </a>

    </div>
  </section>

  <!-- ACTIVITIES -->
  <section class="featured-section" id="atividades">
    <p class="section-label">Atividades práticas</p>
    <h2 class="section-title">Aprenda fazendo</h2>
    <p class="section-sub">Situações reais para praticar em casa ou na sala de aula, do básico ao avançado.</p>
    <div class="activities">

      <a href="#" class="activity-row" onclick="showToast('Carregando atividade 1…'); return false;">
        <div class="activity-num">1</div>
        <div class="activity-body">
          <h4>Compare preços no mercado</h4>
          <p>Calcule o preço por quilo e descubra qual produto é mais barato de verdade.</p>
        </div>
        <span class="activity-level" style="background:#eaf7ee; color:#1a5c2a;">Iniciante</span>
      </a>

      <a href="#" class="activity-row" onclick="showToast('Carregando atividade 2…'); return false;">
        <div class="activity-num">2</div>
        <div class="activity-body">
          <h4>Dobre a receita para mais convidados</h4>
          <p>Uma receita para 4 virou festa para 10. Como ajustar as medidas com proporção?</p>
        </div>
        <span class="activity-level" style="background:#fff8e6; color:#7a5000;">Médio</span>
      </a>

      <a href="#" class="activity-row" onclick="showToast('Carregando atividade 3…'); return false;">
        <div class="activity-num">3</div>
        <div class="activity-body">
          <h4>Calcule o desconto real de uma promoção</h4>
          <p>O produto estava R$120 e agora é R$84. Qual o percentual de desconto real?</p>
        </div>
        <span class="activity-level" style="background:#eef5ff; color:#1a3070;">Médio</span>
      </a>

      <a href="#" class="activity-row" onclick="showToast('Carregando atividade 4…'); return false;">
        <div class="activity-num">4</div>
        <div class="activity-body">
          <h4>Quanto piso preciso para meu quarto?</h4>
          <p>Meça o quarto, calcule a área e descubra quantas caixas de piso comprar.</p>
        </div>
        <span class="activity-level" style="background:#fdeef0; color:#7a1a2a;">Avançado</span>
      </a>

      <a href="#" class="activity-row" onclick="showToast('Carregando atividade 5…'); return false;">
        <div class="activity-num">5</div>
        <div class="activity-body">
          <h4>Entenda a fatura do cartão de crédito</h4>
          <p>Aprenda a ler os juros rotativos e calcular o custo real de parcelar compras.</p>
        </div>
        <span class="activity-level" style="background:#fdeef0; color:#7a1a2a;">Avançado</span>
      </a>

    </div>
  </section>

  <!-- QUOTE + CTA -->
  <div class="two-col" id="contato">
    <div class="quote-card">
      <blockquote>"A matemática está presente em cada compra que fazemos, em cada receita que preparamos, em cada viagem que planejamos."</blockquote>
      <span class="quote-attr">Projeto Ensinar &amp; Aprender</span>
    </div>
    <div class="cta-card">
      <h3>Fique por dentro das novidades</h3>
      <p>Receba atividades, desafios e dicas semanais de matemática no cotidiano direto no seu e-mail.</p>
      <div class="cta-input">
        <input type="email" placeholder="seu@email.com" id="emailInput" />
        <button onclick="handleSubscribe()">Entrar →</button>
      </div>
    </div>
  </div>

</main>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo">Ensinar &amp; <span>Aprender</span></div>
    <p>Projeto de educação matemática contextualizada para professores e alunos.</p>
    <a href="https://www.facebook.com/ensinaraprenderprofessores" target="_blank" rel="noopener">
      Siga no Facebook →
    </a>
    <p style="margin-top: 6px;">© 2025 Projeto Ensinar e Aprender. Todos os direitos reservados.</p>
  </div>
</footer>

<!-- TOAST -->
<div id="toast"></div>

<script>
  function showToast(msg) {
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 2400);
  }

  function handleSubscribe() {
    const input = document.getElementById('emailInput');
    const email = input.value.trim();
    if (!email || !email.includes('@')) {
      showToast('Por favor, insira um e-mail válido.');
      return;
    }
    input.value = '';
    showToast('Inscrição realizada com sucesso! ✓');
  }

  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      const href = this.getAttribute('href');
      if (href === '#' || this.getAttribute('onclick')) return;
      e.preventDefault();
      const target = document.querySelector(href);
      if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });
</script>

</body>
</html>
