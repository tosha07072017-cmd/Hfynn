<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Электрик Челябинск — Профессиональный электромонтаж</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #f59e0b;
            --primary-dark: #d97706;
            --primary-glow: rgba(245, 158, 11, 0.3);
            --bg-dark: #0a0a0f;
            --bg-card: rgba(255, 255, 255, 0.03);
            --bg-glass: rgba(255, 255, 255, 0.05);
            --border: rgba(255, 255, 255, 0.08);
            --text: #f8fafc;
            --text-muted: #94a3b8;
            --accent-gradient: linear-gradient(135deg, #f59e0b 0%, #f97316 100%);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: 'Inter', sans-serif;
            background: var(--bg-dark);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .bg-mesh {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1;
            background: 
                radial-gradient(circle at 20% 50%, rgba(245, 158, 11, 0.08) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(249, 115, 22, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 50% 10%, rgba(245, 158, 11, 0.03) 0%, transparent 50%);
            pointer-events: none;
        }

        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: var(--bg-dark); }
        ::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 4px; }

        nav {
            position: fixed; top: 0; width: 100%; z-index: 1000; padding: 20px 0;
            transition: all 0.4s ease;
        }
        nav.scrolled {
            background: rgba(10, 10, 15, 0.85);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid var(--border);
            padding: 15px 0;
        }
        .nav-container {
            max-width: 1200px; margin: 0 auto; padding: 0 24px;
            display: flex; justify-content: space-between; align-items: center;
        }
        .logo {
            display: flex; align-items: center; gap: 12px;
            font-size: 1.4rem; font-weight: 800; color: var(--text);
            text-decoration: none; letter-spacing: -0.5px;
        }
        .logo-icon {
            width: 40px; height: 40px;
            background: var(--accent-gradient); border-radius: 12px;
            display: flex; align-items: center; justify-content: center;
            font-size: 1.2rem;
            box-shadow: 0 0 20px var(--primary-glow);
        }
        .nav-links { display: flex; gap: 40px; align-items: center; }
        .nav-links a {
            color: var(--text-muted); text-decoration: none; font-weight: 500;
            font-size: 0.95rem; transition: color 0.3s; position: relative;
        }
        .nav-links a::after {
            content: ''; position: absolute; bottom: -6px; left: 0;
            width: 0; height: 2px; background: var(--accent-gradient);
            transition: width 0.3s; border-radius: 2px;
        }
        .nav-links a:hover { color: var(--text); }
        .nav-links a:hover::after { width: 100%; }
        .phone-nav {
            display: flex; align-items: center; gap: 8px;
            padding: 10px 24px; background: var(--bg-glass);
            border: 1px solid var(--border); border-radius: 50px;
            color: var(--primary); text-decoration: none;
            font-weight: 600; font-size: 0.95rem;
            transition: all 0.3s; backdrop-filter: blur(10px);
        }
        .phone-nav:hover {
            background: var(--primary); color: var(--bg-dark);
            border-color: var(--primary);
            box-shadow: 0 0 30px var(--primary-glow);
        }
        .mobile-menu-btn {
            display: none; background: none; border: none;
            color: var(--text); font-size: 1.5rem; cursor: pointer;
        }

        .hero {
            min-height: 100vh; display: flex; align-items: center; justify-content: center;
            text-align: center; padding: 120px 24px 80px; position: relative;
        }
        .hero-content { max-width: 900px; position: relative; z-index: 1; }
        .hero-badge {
            display: inline-flex; align-items: center; gap: 8px;
            padding: 8px 20px; background: var(--bg-glass);
            border: 1px solid var(--border); border-radius: 50px;
            font-size: 0.85rem; color: var(--primary); margin-bottom: 32px;
            backdrop-filter: blur(10px); animation: fadeInUp 0.8s ease;
        }
        .hero-badge::before {
            content: ''; width: 8px; height: 8px;
            background: #22c55e; border-radius: 50%;
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0%, 100% { opacity: 1; } 50% { opacity: 0.5; }
        }
        .hero h1 {
            font-size: clamp(2.5rem, 6vw, 4.5rem); font-weight: 800;
            line-height: 1.1; margin-bottom: 24px; letter-spacing: -2px;
            animation: fadeInUp 0.8s ease 0.1s both;
        }
        .hero h1 span {
            background: var(--accent-gradient);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .hero p {
            font-size: 1.25rem; color: var(--text-muted);
            max-width: 600px; margin: 0 auto 40px; line-height: 1.7;
            animation: fadeInUp 0.8s ease 0.2s both;
        }
        .hero-buttons {
            display: flex; gap: 16px; justify-content: center; flex-wrap: wrap;
            animation: fadeInUp 0.8s ease 0.3s both;
        }
        .btn-primary {
            padding: 16px 40px; background: var(--accent-gradient); color: white;
            text-decoration: none; border-radius: 14px; font-weight: 600;
            font-size: 1.05rem; transition: all 0.3s;
            display: inline-flex; align-items: center; gap: 8px;
            border: none; cursor: pointer;
            box-shadow: 0 4px 20px rgba(245, 158, 11, 0.3);
        }
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(245, 158, 11, 0.5);
        }
        .btn-secondary {
            padding: 16px 40px; background: var(--bg-glass); color: var(--text);
            text-decoration: none; border-radius: 14px; font-weight: 600;
            font-size: 1.05rem; transition: all 0.3s;
            display: inline-flex; align-items: center; gap: 8px;
            border: 1px solid var(--border); backdrop-filter: blur(10px);
        }
        .btn-secondary:hover {
            background: rgba(255,255,255,0.1); border-color: var(--primary);
        }

        .floating-card {
            position: absolute; background: var(--bg-glass);
            backdrop-filter: blur(20px); border: 1px solid var(--border);
            border-radius: 20px; padding: 20px;
            display: flex; align-items: center; gap: 12px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            animation: float 6s ease-in-out infinite;
        }
        .floating-card-1 { top: 20%; right: 5%; animation-delay: 0s; }
        .floating-card-2 { bottom: 20%; left: 5%; animation-delay: 3s; }
        @keyframes float {
            0%, 100% { transform: translateY(0); } 50% { transform: translateY(-20px); }
        }
        .floating-icon {
            width: 48px; height: 48px;
            background: var(--accent-gradient); border-radius: 12px;
            display: flex; align-items: center; justify-content: center;
            font-size: 1.5rem;
        }

        section { padding: 100px 24px; position: relative; }
        .section-header {
            text-align: center; max-width: 600px; margin: 0 auto 64px;
        }
        .section-label {
            display: inline-block; padding: 6px 16px;
            background: var(--primary-glow); border: 1px solid var(--primary);
            border-radius: 50px; color: var(--primary);
            font-size: 0.85rem; font-weight: 600; margin-bottom: 16px;
            text-transform: uppercase; letter-spacing: 1px;
        }
        .section-title {
            font-size: clamp(2rem, 4vw, 3rem); font-weight: 800;
            margin-bottom: 16px; letter-spacing: -1px;
        }
        .section-desc { color: var(--text-muted); font-size: 1.1rem; }

        .stats {
            background: linear-gradient(135deg, rgba(245, 158, 11, 0.05) 0%, rgba(249, 115, 22, 0.05) 100%);
            border-top: 1px solid var(--border); border-bottom: 1px solid var(--border);
        }
        .stats-grid {
            max-width: 1000px; margin: 0 auto;
            display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px; text-align: center;
        }
        .stat-item h3 {
            font-size: 3rem; font-weight: 800;
            background: var(--accent-gradient);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            background-clip: text; margin-bottom: 8px;
        }
        .stat-item p { color: var(--text-muted); font-size: 0.95rem; }

        .services-grid {
            max-width: 1200px; margin: 0 auto;
            display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 24px;
        }
        .service-card {
            background: var(--bg-card); border: 1px solid var(--border);
            border-radius: 24px; padding: 40px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative; overflow: hidden; cursor: pointer;
        }
        .service-card::before {
            content: ''; position: absolute; top: 0; left: 0;
            width: 100%; height: 100%;
            background: radial-gradient(circle at var(--mouse-x, 50%) var(--mouse-y, 50%), rgba(245, 158, 11, 0.1), transparent 50%);
            opacity: 0; transition: opacity 0.3s; pointer-events: none;
        }
        .service-card:hover::before { opacity: 1; }
        .service-card:hover {
            transform: translateY(-8px); border-color: var(--primary);
            box-shadow: 0 20px 40px rgba(0,0,0,0.4), 0 0 60px rgba(245, 158, 11, 0.1);
        }
        .service-icon {
            width: 64px; height: 64px;
            background: var(--accent-gradient); border-radius: 16px;
            display: flex; align-items: center; justify-content: center;
            font-size: 1.8rem; margin-bottom: 24px;
            box-shadow: 0 8px 20px rgba(245, 158, 11, 0.3);
        }
        .service-card h3 { font-size: 1.3rem; font-weight: 700; margin-bottom: 12px; }
        .service-card p { color: var(--text-muted); font-size: 0.95rem; line-height: 1.7; }

        .pricing-grid {
            max-width: 1000px; margin: 0 auto;
            display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 24px; align-items: start;
        }
        .pricing-card {
            background: var(--bg-card); border: 1px solid var(--border);
            border-radius: 24px; padding: 48px 32px;
            text-align: center; transition: all 0.4s; position: relative;
        }
        .pricing-card.featured {
            background: linear-gradient(135deg, rgba(245, 158, 11, 0.1) 0%, rgba(249, 115, 22, 0.05) 100%);
            border-color: var(--primary); transform: scale(1.05);
            box-shadow: 0 0 60px rgba(245, 158, 11, 0.15);
        }
        .pricing-card.featured::before {
            content: 'Популярный'; position: absolute;
            top: -12px; left: 50%; transform: translateX(-50%);
            background: var(--accent-gradient); color: white;
            padding: 6px 20px; border-radius: 50px;
            font-size: 0.8rem; font-weight: 600;
        }
        .pricing-card:hover { transform: translateY(-8px); border-color: var(--primary); }
        .pricing-card.featured:hover { transform: scale(1.05) translateY(-8px); }
        .pricing-card h3 { font-size: 1.3rem; font-weight: 700; margin-bottom: 8px; }
        .price {
            font-size: 3rem; font-weight: 800;
            background: var(--accent-gradient);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            background-clip: text; margin: 16px 0;
        }
        .pricing-card ul { list-style: none; margin: 32px 0; text-align: left; }
        .pricing-card ul li {
            padding: 12px 0; color: var(--text-muted);
            border-bottom: 1px solid var(--border);
            display: flex; align-items: center; gap: 10px;
        }
        .pricing-card ul li::before { content: '✓'; color: var(--primary); font-weight: bold; }

        .cta { text-align: center; background: linear-gradient(135deg, rgba(245, 158, 11, 0.08) 0%, transparent 100%); }
        .cta-phone {
            display: inline-flex; align-items: center; gap: 16px;
            margin: 32px 0; padding: 24px 48px;
            background: var(--bg-glass); border: 1px solid var(--border);
            border-radius: 24px; text-decoration: none; color: var(--text);
            transition: all 0.3s; backdrop-filter: blur(20px);
        }
        .cta-phone:hover {
            border-color: var(--primary);
            box-shadow: 0 0 40px var(--primary-glow);
            transform: scale(1.05);
        }
        .cta-phone .phone-icon {
            width: 64px; height: 64px;
            background: var(--accent-gradient); border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-size: 1.5rem;
            animation: pulse-ring 2s infinite;
        }
        @keyframes pulse-ring {
            0% { box-shadow: 0 0 0 0 rgba(245, 158, 11, 0.4); }
            70% { box-shadow: 0 0 0 20px rgba(245, 158, 11, 0); }
            100% { box-shadow: 0 0 0 0 rgba(245, 158, 11, 0); }
        }
        .cta-phone .phone-text { text-align: left; }
        .cta-phone .phone-label { font-size: 0.9rem; color: var(--text-muted); margin-bottom: 4px; }
        .cta-phone .phone-number { font-size: 2rem; font-weight: 800; color: var(--primary); }

        .form-container { max-width: 600px; margin: 0 auto; }
        .form-card {
            background: var(--bg-card); border: 1px solid var(--border);
            border-radius: 24px; padding: 48px; backdrop-filter: blur(20px);
        }
        .form-group { margin-bottom: 24px; }
        .form-group label {
            display: block; margin-bottom: 8px;
            font-weight: 500; font-size: 0.9rem; color: var(--text-muted);
        }
        .form-group input, .form-group textarea {
            width: 100%; padding: 16px 20px;
            background: var(--bg-glass); border: 1px solid var(--border);
            border-radius: 14px; color: var(--text); font-size: 1rem;
            font-family: inherit; transition: all 0.3s;
        }
        .form-group input:focus, .form-group textarea:focus {
            outline: none; border-color: var(--primary);
            box-shadow: 0 0 0 3px var(--primary-glow);
        }
        .form-group textarea { resize: vertical; min-height: 120px; }
        .btn-submit {
            width: 100%; padding: 18px;
            background: var(--accent-gradient); color: white;
            border: none; border-radius: 14px; font-size: 1.1rem;
            font-weight: 600; cursor: pointer; transition: all 0.3s;
            font-family: inherit;
        }
        .btn-submit:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(245, 158, 11, 0.4);
        }

        footer {
            background: rgba(0,0,0,0.3); border-top: 1px solid var(--border);
            padding: 60px 24px 30px; text-align: center;
        }
        .footer-content { max-width: 800px; margin: 0 auto; }
        .footer-logo {
            font-size: 1.5rem; font-weight: 800; margin-bottom: 16px;
            display: flex; align-items: center; justify-content: center; gap: 12px;
        }
        .footer-phone {
            display: inline-block; margin: 16px 0; padding: 12px 32px;
            background: var(--bg-glass); border: 1px solid var(--border);
            border-radius: 50px; color: var(--primary);
            text-decoration: none; font-weight: 600; font-size: 1.1rem;
            transition: all 0.3s;
        }
        .footer-phone:hover { background: var(--primary); color: var(--bg-dark); }
        .footer-copy {
            margin-top: 32px; padding-top: 24px;
            border-top: 1px solid var(--border);
            color: var(--text-muted); font-size: 0.9rem;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .reveal {
            opacity: 0; transform: translateY(40px);
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .reveal.visible { opacity: 1; transform: translateY(0); }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .mobile-menu-btn { display: block; }
            .floating-card { display: none; }
            .hero h1 { font-size: 2.2rem; }
            .hero-buttons { flex-direction: column; align-items: center; }
            .btn-primary, .btn-secondary { width: 100%; justify-content: center; }
            .pricing-card.featured { transform: none; }
            .pricing-card.featured:hover { transform: translateY(-8px); }
            .form-card { padding: 32px 24px; }
            .cta-phone { flex-direction: column; padding: 24px; }
            .cta-phone .phone-number { font-size: 1.5rem; }
            section { padding: 60px 20px; }
        }
    </style>
</head>
<body>

    <div class="bg-mesh"></div>

    <nav id="navbar">
        <div class="nav-container">
            <a href="#" class="logo">
                <div class="logo-icon">⚡</div>
                ЭЛЕКТРИК74
            </a>
            <div class="nav-links">
                <a href="#services">Услуги</a>
                <a href="#pricing">Цены</a>
                <a href="#contact">Контакты</a>
                <a href="tel:+79227331802" class="phone-nav">📞 +7 (922) 733-18-02</a>
            </div>
            <button class="mobile-menu-btn">☰</button>
        </div>
    </nav>

    <section class="hero">
        <div class="floating-card floating-card-1">
            <div class="floating-icon">⚡</div>
            <div>
                <div style="font-weight:700;">Выезд 24/7</div>
                <div style="font-size:0.85rem;color:var(--text-muted);">В любой район</div>
            </div>
        </div>
        <div class="floating-card floating-card-2">
            <div class="floating-icon">🛡️</div>
            <div>
                <div style="font-weight:700;">Гарантия 3 года</div>
                <div style="font-size:0.85rem;color:var(--text-muted);">На все работы</div>
            </div>
        </div>

        <div class="hero-content">
            <div class="hero-badge">Электрик в Челябинске</div>
            <h1>Профессиональный <span>электромонтаж</span> в Челябинске</h1>
            <p>Качественные электротехнические работы любой сложности. Выезд на объект в день обращения. Честные цены без скрытых платежей.</p>
            <div class="hero-buttons">
                <a href="tel:+79227331802" class="btn-primary">📞 Позвонить сейчас</a>
                <a href="#contact" class="btn-secondary">✉️ Оставить заявку</a>
            </div>
        </div>
    </section>

    <section class="stats">
        <div class="stats-grid reveal">
            <div class="stat-item"><h3>10+</h3><p>Лет опыта работы</p></div>
            <div class="stat-item"><h3>500+</h3><p>Выполненных объектов</p></div>
            <div class="stat-item"><h3>30 мин</h3><p>Среднее время приезда</p></div>
            <div class="stat-item"><h3>100%</h3><p>Гарантия качества</p></div>
        </div>
    </section>

    <section id="services">
        <div class="section-header reveal">
            <div class="section-label">Услуги</div>
            <h2 class="section-title">Что мы делаем</h2>
            <p class="section-desc">Полный спектр электромонтажных работ для квартир, домов и коммерческих помещений</p>
        </div>
        <div class="services-grid">
            <div class="service-card reveal">
                <div class="service-icon">🏠</div>
                <h3>Квартирная электрика</h3>
                <p>Полная или частичная замена проводки, установка розеток и выключателей, монтаж освещения и подсветки</p>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">🏢</div>
                <h3>Офисы и магазины</h3>
                <p>Проектирование и монтаж электросетей для коммерческих помещений, установка щитового оборудования</p>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">🏭</div>
                <h3>Промышленный монтаж</h3>
                <p>Электромонтаж на производствах, складах и промышленных объектах любой сложности</p>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">🔧</div>
                <h3>Щиты и автоматы</h3>
                <p>Монтаж и сборка распределительных щитов, установка автоматов, УЗО и дифавтоматов</p>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">💡</div>
                <h3>Освещение</h3>
                <p>Монтаж люстр, светильников, точечного освещения, LED-подсветки, диммеров и умного света</p>
            </div>
            <div class="service-card reveal">
                <div class="service-icon">🔌</div>
                <h3>Розетки и выключатели</h3>
                <p>Установка, перенос и замена розеток, выключателей, диммеров, таймеров и датчиков движения</p>
            </div>
        </div>
    </section>

    <section id="pricing">
        <div class="section-header reveal">
            <div class="section-label">Стоимость</div>
            <h2 class="section-title">Прозрачные цены</h2>
            <p class="section-desc">Фиксированная стоимость работ. Никаких скрытых платежей</p>
        </div>
        <div class="pricing-grid">
            <div class="pricing-card reveal">
                <h3>Минимальный</h3>
                <div class="price">1 500 ₽</div>
                <ul>
                    <li>Замена розетки / выключателя</li>
                    <li>Установка люстры</li>
                    <li>Диагностика неисправности</li>
                    <li>Консультация электрика</li>
                </ul>
                <a href="tel:+79227331802" class="btn-primary" style="width:100%;justify-content:center;">Заказать</a>
            </div>
            <div class="pricing-card featured reveal">
                <h3>Стандартный</h3>
                <div class="price">5 000 ₽</div>
                <ul>
                    <li>Замена проводки в комнате</li>
                    <li>Монтаж распаечной коробки</li>
                    <li>Установка щитка с автоматами</li>
                    <li>Прокладка кабеля до 10 м</li>
                </ul>
                <a href="tel:+79227331802" class="btn-primary" style="width:100%;justify-content:center;">Заказать</a>
            </div>
            <div class="pricing-card reveal">
                <h3>Полный</h3>
                <div class="price">15 000 ₽</div>
                <ul>
                    <li>Полная замена проводки</li>
                    <li>Монтаж электрощита</li>
                    <li>Установка освещения</li>
                    <li>Сборка и подключение</li>
                </ul>
                <a href="tel:+79227331802" class="btn-primary" style="width:100%;justify-content:center;">Заказать</a>
            </div>
        </div>
    </section>

    <section id="contact" class="cta">
        <div class="section-header reveal">
            <div class="section-label">Контакты</div>
            <h2 class="section-title">Готовы начать?</h2>
            <p class="section-desc">Звоните прямо сейчас — работаем без выходных с 8:00 до 22:00</p>
        </div>
        <div class="reveal">
            <a href="tel:+79227331802" class="cta-phone">
                <div class="phone-icon">📞</div>
                <div class="phone-text">
                    <div class="phone-label">Позвоните нам</div>
                    <div class="phone-number">+7 (922) 733-18-02</div>
                </div>
            </a>
            <div style="margin-top: 40px; display: flex; justify-content: center; gap: 40px; flex-wrap: wrap; color: var(--text-muted);">
                <div>📍 Челябинск и область</div>
                <div>🚗 Бесплатный выезд</div>
                <div>⏰ Ежедневно 8:00 — 22:00</div>
            </div>
        </div>
    </section>

    <section>
        <div class="section-header reveal">
            <div class="section-label">Заявка</div>
            <h2 class="section-title">Оставить заявку</h2>
            <p class="section-desc">Опишите задачу — мы перезвоним в течение 15 минут</p>
        </div>
        <div class="form-container reveal">
            <div class="form-card">
                <form id="contactForm">
                    <div class="form-group">
                        <label>Ваше имя</label>
                        <input type="text" id="formName" placeholder="Иван Иванов" required>
                    </div>
                    <div class="form-group">
                        <label>Телефон</label>
                        <input type="tel" id="formPhone" placeholder="+7 (___) ___-__-__" required>
                    </div>
                    <div class="form-group">
                        <label>Описание задачи</label>
                        <textarea id="formMessage" placeholder="Например: нужно заменить проводку в двухкомнатной квартире..."></textarea>
                    </div>
                    <button type="submit" class="btn-submit">Отправить заявку</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-content">
            <div class="footer-logo">
                <div class="logo-icon" style="width:36px;height:36px;font-size:1rem;">⚡</div>
                ЭЛЕКТРИК74
            </div>
            <p style="color: var(--text-muted); margin-bottom: 16px;">Профессиональный электромонтаж в Челябинске</p>
            <a href="tel:+79227331802" class="footer-phone">+7 (922) 733-18-02</a>
            <div class="footer-copy">
                © 2026 Электрик Челябинск. Все права защищены.
            </div>
        </div>
    </footer>

    <script>
        // ═══════════════════════════════════════════════════════════════
        // КОНФИГУРАЦИЯ TELEGRAM-БОТА — ЗАПОЛНИТЕ ЭТИ ДАННЫЕ!
        // ═══════════════════════════════════════════════════════════════
        
        // 1. Создайте бота у @BotFather в Telegram
        // 2. Получите токен вида: 123456789:ABCdefGHIjklMNOpqrSTUvwxyz
        const BOT_TOKEN = 'ВАШ_ТОКЕН_БОТА';  // ← ЗАМЕНИТЕ!
        
        // 3. Узнайте свой chat_id через @userinfobot или @getmyid_bot
        const CHAT_ID = 'ВАШ_CHAT_ID';  // ← ЗАМЕНИТЕ!
        
        // 4. Для отправки через прокси (если прямой запрос не работает):
        // Можно использовать сервисы типа https://api.allorigins.win/raw?url=
        // или https://corsproxy.io/? — но лучше настроить серверную часть
        
        // ═══════════════════════════════════════════════════════════════

        // Получение информации о посетителе
        async function getVisitorInfo() {
            let ip = 'неизвестно';
            let city = 'Челябинск (предположительно)';
            let country = 'RU';
            
            try {
                const response = await fetch('https://ipapi.co/json/');
                const data = await response.json();
                ip = data.ip;
                city = data.city || city;
                country = data.country_name || country;
            } catch (e) {
                console.log('Не удалось получить IP');
            }

            const now = new Date();
            const timeString = now.toLocaleString('ru-RU', {
                day: '2-digit', month: '2-digit', year: 'numeric',
                hour: '2-digit', minute: '2-digit', second: '2-digit'
            });

            const ua = navigator.userAgent;
            let device = '💻 Компьютер';
            if (/Mobile|Android|iPhone|iPad|iPod/.test(ua)) {
                device = /iPad/.test(ua) ? '📱 Планшет' : '📱 Телефон';
            }

            let browser = 'Неизвестный';
            if (ua.includes('Chrome')) browser = 'Chrome';
            else if (ua.includes('Firefox')) browser = 'Firefox';
            else if (ua.includes('Safari')) browser = 'Safari';
            else if (ua.includes('Edge')) browser = 'Edge';

            let os = 'Неизвестная';
            if (ua.includes('Windows')) os = 'Windows';
            else if (ua.includes('Mac')) os = 'macOS';
            else if (ua.includes('Linux')) os = 'Linux';
            else if (ua.includes('Android')) os = 'Android';
            else if (ua.includes('iPhone') || ua.includes('iPad')) os = 'iOS';

            const referrer = document.referrer || 'Прямой заход';
            const page = window.location.href;

            return {
                ip, city, country, time: timeString, device, browser, os, referrer, page
            };
        }

        // Форматирование сообщения для Telegram
        function formatVisitorMessage(info) {
            return `🔔 <b>Новый посетитель сайта!</b>

📍 <b>IP:</b> <code>${info.ip}</code>
🏙 <b>Город:</b> ${info.city}, ${info.country}
⏰ <b>Время:</b> ${info.time}
📱 <b>Устройство:</b> ${info.device}
🌐 <b>Браузер:</b> ${info.browser}
💻 <b>ОС:</b> ${info.os}
🔗 <b>Источник:</b> ${info.referrer}
📄 <b>Страница:</b> ${info.page}`;
        }

        // Отправка в Telegram
        async function sendToTelegram(text) {
            if (BOT_TOKEN === 'ВАШ_ТОКЕН_БОТА' || CHAT_ID === 'ВАШ_CHAT_ID') {
                console.log('⚠️ Не настроен Telegram-бот. Сообщение не отправлено.');
                console.log('Данные посетителя:', text);
                return;
            }

            const url = `https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`;
            
            try {
                // Пробуем прямой запрос
                const response = await fetch(url, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        chat_id: CHAT_ID,
                        text: text,
                        parse_mode: 'HTML'
                    })
                });
                
                if (!response.ok) throw new Error('Прямой запрос не удался');
                console.log('✅ Уведомление отправлено в Telegram');
            } catch (e) {
                // Если прямой запрос не работает (CORS), пробуем через прокси
                try {
                    const proxyUrl = `https://api.allorigins.win/raw?url=${encodeURIComponent(url)}`;
                    await fetch(proxyUrl, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify({
                            chat_id: CHAT_ID,
                            text: text,
                            parse_mode: 'HTML'
                        })
                    });
                    console.log('✅ Уведомление отправлено через прокси');
                } catch (e2) {
                    console.error('❌ Не удалось отправить в Telegram:', e2);
                }
            }
        }

        // Отслеживание посетителя при загрузке
        let visitorNotified = false;
        async function trackVisitor() {
            if (visitorNotified) return;
            visitorNotified = true;
            
            const info = await getVisitorInfo();
            const message = formatVisitorMessage(info);
            await sendToTelegram(message);
        }

        // Отслеживание кликов по телефону
        document.querySelectorAll('a[href^="tel:"]').forEach(link => {
            link.addEventListener('click', async () => {
                const info = await getVisitorInfo();
                const message = `📞 <b>КЛИК ПО ТЕЛЕФОНУ!</b>

👤 Пользователь нажал на номер телефона
${formatVisitorMessage(info).split('\n').slice(1).join('\n')}`;
                await sendToTelegram(message);
            });
        });

        // Отслеживание отправки формы
        document.getElementById('contactForm').addEventListener('submit', async (e) => {
            e.preventDefault();
            
            const name = document.getElementById('formName').value;
            const phone = document.getElementById('formPhone').value;
            const message = document.getElementById('formMessage').value;
            
            const info = await getVisitorInfo();
            const telegramMessage = `📝 <b>НОВАЯ ЗАЯВКА С САЙТА!</b>

👤 <b>Имя:</b> ${name}
📱 <b>Телефон:</b> <code>${phone}</code>
💬 <b>Сообщение:</b> ${message || 'Не указано'}

📍 <b>IP:</b> <code>${info.ip}</code>
🏙 <b>Город:</b> ${info.city}, ${info.country}
⏰ <b>Время:</b> ${info.time}
📱 <b>Устройство:</b> ${info.device}`;

            await sendToTelegram(telegramMessage);
            
            // Показываем успешную отправку
            const btn = e.target.querySelector('.btn-submit');
            const originalText = btn.textContent;
            btn.textContent = '✓ Заявка отправлена!';
            btn.style.background = '#22c55e';
            setTimeout(() => {
                btn.textContent = originalText;
                btn.style.background = '';
                e.target.reset();
            }, 3000);
        });

        // Запускаем отслеживание через 2 секунды после загрузки
        setTimeout(trackVisitor, 2000);

        // Также отслеживаем при возвращении на вкладку
        document.addEventListener('visibilitychange', () => {
            if (document.visibilityState === 'visible') {
                setTimeout(trackVisitor, 1000);
            }
        });

        // ═══════════════════════════════════════════════════════════════
        // ОСТАЛЬНЫЕ СКРИПТЫ САЙТА
        // ═══════════════════════════════════════════════════════════════

        // Navbar scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            navbar.classList.toggle('scrolled', window.scrollY > 50);
        });

        // Mouse tracking for cards
        document.querySelectorAll('.service-card').forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                card.style.setProperty('--mouse-x', ((e.clientX - rect.left) / rect.width) * 100 + '%');
                card.style.setProperty('--mouse-y', ((e.clientY - rect.top) / rect.height) * 100 + '%');
            });
        });

        // Reveal on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.classList.add('visible');
            });
        }, { threshold: 0.1, rootMargin: '0px 0px -50px 0px' });

        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
            });
        });
    </script>

</body>
</html>
