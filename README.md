<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anti Virus Lion - Total Protection</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', sans-serif;
            color: #1a1a2e;
            background: #fff;
            overflow-x: hidden;
        }

        .top-banner {
            background: linear-gradient(90deg, #c40233, #ff1744);
            color: #fff;
            text-align: center;
            padding: 10px 20px;
            font-size: 0.85rem;
            font-weight: 500;
            letter-spacing: 0.3px;
        }

        .top-banner span {
            font-weight: 700;
            text-decoration: underline;
            cursor: pointer;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 60px;
            background: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-logo-icon {
            width: 42px;
            height: 42px;
            background: linear-gradient(135deg, #c40233, #ff1744);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.4rem;
            box-shadow: 0 4px 15px rgba(196, 2, 51, 0.3);
        }

        .nav-logo-text {
            font-size: 1.3rem;
            font-weight: 800;
            color: #1a1a2e;
            letter-spacing: -0.5px;
        }

        .nav-logo-text .red { color: #c40233; }

        nav ul {
            display: flex;
            list-style: none;
            gap: 32px;
            align-items: center;
        }

        nav ul li a {
            color: #444;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: color 0.2s;
            position: relative;
        }

        nav ul li a:hover { color: #c40233; }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: #c40233;
            transition: width 0.3s;
        }

        nav ul li a:hover::after { width: 100%; }

        .nav-btn {
            background: #c40233;
            color: #fff !important;
            padding: 10px 24px;
            border-radius: 25px;
            font-weight: 600;
            font-size: 0.85rem;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(196, 2, 51, 0.3);
            cursor: pointer;
        }

        .nav-btn::after { display: none !important; }

        .nav-btn:hover {
            background: #a30029 !important;
            transform: translateY(-1px);
            box-shadow: 0 6px 20px rgba(196, 2, 51, 0.4);
        }

        .hero {
            display: flex;
            align-items: center;
            justify-content: space-between;
            max-width: 1200px;
            margin: 0 auto;
            padding: 80px 60px;
            gap: 60px;
        }

        .hero-left {
            flex: 1;
            max-width: 550px;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #fff3f3;
            color: #c40233;
            padding: 8px 18px;
            border-radius: 25px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 25px;
            border: 1px solid rgba(196, 2, 51, 0.15);
        }

        .hero-badge-dot {
            width: 8px;
            height: 8px;
            background: #c40233;
            border-radius: 50%;
            animation: blink 1.5s ease-in-out infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.3; }
        }

        .hero h1 {
            font-size: 3.2rem;
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 20px;
            letter-spacing: -1px;
            color: #0d0d2b;
        }

        .hero h1 .red { color: #c40233; }
        .hero h1 .gold { color: #d4900a; }

        .hero-desc {
            font-size: 1.1rem;
            color: #666;
            line-height: 1.7;
            margin-bottom: 35px;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            align-items: center;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(135deg, #c40233, #e8053a);
            color: #fff;
            padding: 18px 40px;
            border-radius: 32px;
            font-size: 1.05rem;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s;
            box-shadow: 0 6px 25px rgba(196, 2, 51, 0.35);
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: left 0.5s;
        }

        .btn-primary:hover::before { left: 100%; }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 35px rgba(196, 2, 51, 0.45);
        }

        .btn-secondary {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #1a1a2e;
            padding: 18px 30px;
            border-radius: 32px;
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            border: 2px solid #ddd;
            transition: all 0.3s;
            cursor: pointer;
            background: transparent;
        }

        .btn-secondary:hover {
            border-color: #c40233;
            color: #c40233;
        }

        .hero-meta {
            display: flex;
            gap: 30px;
            font-size: 0.82rem;
            color: #999;
        }

        .hero-meta-item {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .check-green {
            color: #22c55e;
            font-weight: 700;
        }

        .hero-right {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        .shield-visual {
            position: relative;
            width: 380px;
            height: 380px;
        }

        .shield-bg {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(196, 2, 51, 0.08) 0%, transparent 70%);
            border-radius: 50%;
        }

        .shield-circle {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 50%;
            border: 2px dashed rgba(196, 2, 51, 0.15);
        }

        .shield-circle-1 {
            width: 320px;
            height: 320px;
            animation: spin 20s linear infinite;
        }

        .shield-circle-2 {
            width: 360px;
            height: 360px;
            animation: spin 30s linear infinite reverse;
            border-style: dotted;
        }

        @keyframes spin {
            from { transform: translate(-50%, -50%) rotate(0deg); }
            to { transform: translate(-50%, -50%) rotate(360deg); }
        }

        .main-shield {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 200px;
            height: 230px;
            background: linear-gradient(160deg, #c40233, #e8053a, #ff2d55);
            border-radius: 10px 10px 50% 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            box-shadow: 0 20px 60px rgba(196, 2, 51, 0.3);
            animation: shield-float 3s ease-in-out infinite;
        }

        @keyframes shield-float {
            0%, 100% { transform: translate(-50%, -50%) translateY(0px); }
            50% { transform: translate(-50%, -50%) translateY(-10px); }
        }

        .main-shield .lion-emoji {
            font-size: 4rem;
            filter: drop-shadow(0 4px 8px rgba(0,0,0,0.2));
        }

        .main-shield .shield-check {
            font-size: 2rem;
            margin-top: 5px;
        }

        .floating-badge {
            position: absolute;
            background: #fff;
            border-radius: 12px;
            padding: 12px 18px;
            box-shadow: 0 8px 30px rgba(0,0,0,0.12);
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.8rem;
            font-weight: 600;
            animation: badge-float 4s ease-in-out infinite;
            white-space: nowrap;
        }

        .floating-badge-1 { top: 30px; right: 10px; animation-delay: 0s; }
        .floating-badge-2 { bottom: 50px; left: 0px; animation-delay: 1s; }
        .floating-badge-3 { top: 50px; left: 10px; animation-delay: 2s; }

        @keyframes badge-float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-8px); }
        }

        .badge-icon {
            width: 32px;
            height: 32px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
        }

        .badge-icon.green { background: #e8faf0; color: #22c55e; }
        .badge-icon.blue { background: #eef4ff; color: #3b82f6; }
        .badge-icon.red { background: #fff1f1; color: #c40233; }

        .trust-bar {
            background: #f8f9fb;
            padding: 30px 60px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 50px;
            flex-wrap: wrap;
            border-top: 1px solid #eee;
            border-bottom: 1px solid #eee;
        }

        .trust-label {
            font-size: 0.8rem;
            color: #999;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .trust-logos {
            display: flex;
            gap: 40px;
            align-items: center;
            flex-wrap: wrap;
        }

        .trust-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            font-weight: 700;
            color: #bbb;
        }

        .trust-item span { font-size: 1.5rem; }

        .stats-section {
            background: linear-gradient(135deg, #0d0d2b, #1a1a40);
            padding: 70px 60px;
            color: #fff;
        }

        .stats-grid {
            max-width: 1100px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px;
            text-align: center;
        }

        .stat-item { padding: 20px; }

        .stat-number {
            font-size: 3rem;
            font-weight: 900;
            color: #fff;
            margin-bottom: 8px;
            letter-spacing: -1px;
        }

        .stat-number .red-num { color: #ff4466; }

        .stat-desc {
            font-size: 0.9rem;
            color: #8888aa;
        }

        .features-section {
            padding: 80px 60px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-label {
            display: inline-block;
            background: #fff1f1;
            color: #c40233;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .section-header h2 {
            font-size: 2.5rem;
            font-weight: 800;
            color: #0d0d2b;
            margin-bottom: 15px;
        }

        .section-header p {
            font-size: 1.05rem;
            color: #888;
            max-width: 550px;
            margin: 0 auto;
            line-height: 1.6;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .feature-card {
            background: #fff;
            border: 1px solid #f0f0f0;
            border-radius: 16px;
            padding: 35px 30px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #c40233, #ff4466);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s;
        }

        .feature-card:hover::before { transform: scaleX(1); }

        .feature-card:hover {
            box-shadow: 0 15px 40px rgba(0,0,0,0.1);
            transform: translateY(-5px);
        }

        .feature-card-icon {
            width: 56px;
            height: 56px;
            background: linear-gradient(135deg, #fff1f1, #ffe8e8);
            border-radius: 14px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.6rem;
            margin-bottom: 20px;
        }

        .feature-card h3 {
            font-size: 1.15rem;
            font-weight: 700;
            color: #0d0d2b;
            margin-bottom: 12px;
        }

        .feature-card p {
            font-size: 0.9rem;
            color: #888;
            line-height: 1.7;
        }

        .plan-section {
            background: linear-gradient(135deg, #fafafa, #f5f5f5);
            padding: 80px 60px;
        }

        .plan-card {
            max-width: 900px;
            margin: 0 auto;
            background: #fff;
            border-radius: 24px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.08);
            display: flex;
        }

        .plan-left {
            flex: 1;
            padding: 50px 40px;
        }

        .plan-popular {
            display: inline-block;
            background: linear-gradient(135deg, #c40233, #ff4466);
            color: #fff;
            padding: 5px 14px;
            border-radius: 15px;
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 18px;
        }

        .plan-left h3 {
            font-size: 1.8rem;
            font-weight: 800;
            color: #0d0d2b;
            margin-bottom: 8px;
        }

        .plan-left .plan-sub {
            color: #999;
            font-size: 0.95rem;
            margin-bottom: 25px;
        }

        .plan-features {
            list-style: none;
            margin-bottom: 30px;
        }

        .plan-features li {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 10px 0;
            font-size: 0.95rem;
            color: #555;
            border-bottom: 1px solid #f5f5f5;
        }

        .plan-features li:last-child { border: none; }

        .plan-check {
            width: 22px;
            height: 22px;
            background: #e8faf0;
            color: #22c55e;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.75rem;
            font-weight: 800;
            flex-shrink: 0;
        }

        .plan-right {
            width: 280px;
            background: linear-gradient(160deg, #0d0d2b, #1a1a40);
            padding: 50px 35px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: #fff;
        }

        .plan-price-label {
            font-size: 0.85rem;
            color: #8888aa;
            margin-bottom: 8px;
        }

        .plan-price {
            font-size: 3.5rem;
            font-weight: 900;
            margin-bottom: 5px;
        }

        .plan-price-sub {
            font-size: 0.85rem;
            color: #8888aa;
            margin-bottom: 30px;
        }

        .plan-price .small { font-size: 1.5rem; }

        .plan-download-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: linear-gradient(135deg, #c40233, #e8053a);
            color: #fff;
            padding: 16px 35px;
            border-radius: 30px;
            font-size: 1rem;
            font-weight: 700;
            text-decoration: none;
            border: none;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 6px 20px rgba(196, 2, 51, 0.4);
            margin-bottom: 15px;
            width: 100%;
            justify-content: center;
        }

        .plan-download-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(196, 2, 51, 0.5);
        }

        .plan-guarantee {
            font-size: 0.75rem;
            color: #6666aa;
        }

        .devices-section {
            padding: 60px;
            text-align: center;
        }

        .devices-section h3 {
            font-size: 1.1rem;
            font-weight: 600;
            color: #999;
            margin-bottom: 30px;
        }

        .devices-row {
            display: flex;
            justify-content: center;
            gap: 50px;
            flex-wrap: wrap;
        }

        .device-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            font-size: 0.85rem;
            color: #888;
            font-weight: 500;
        }

        .device-icon {
            width: 60px;
            height: 60px;
            background: #f8f8f8;
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            border: 1px solid #eee;
            transition: all 0.3s;
        }

        .device-item:hover .device-icon {
            border-color: #c40233;
            background: #fff1f1;
        }

        .cta-section {
            background: linear-gradient(135deg, #c40233, #e8053a, #ff2d55);
            padding: 70px 60px;
            text-align: center;
            color: #fff;
            position: relative;
            overflow: hidden;
        }

        .cta-section::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 500px;
            height: 500px;
            background: rgba(255,255,255,0.05);
            border-radius: 50%;
        }

        .cta-section h2 {
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 15px;
            position: relative;
            z-index: 1;
        }

        .cta-section p {
            font-size: 1.1rem;
            opacity: 0.85;
            margin-bottom: 30px;
            position: relative;
            z-index: 1;
        }

        .btn-white {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: #fff;
            color: #c40233;
            padding: 18px 45px;
            border-radius: 32px;
            font-size: 1.05rem;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s;
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
            position: relative;
            z-index: 1;
            border: none;
            cursor: pointer;
        }

        .btn-white:hover {
            transform: translateY(-2px) scale(1.02);
            box-shadow: 0 12px 35px rgba(0,0,0,0.2);
        }

        footer {
            background: #0d0d2b;
            color: #666;
            padding: 50px 60px 30px;
        }

        .footer-top {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            max-width: 1100px;
            margin: 0 auto 40px;
        }

        .footer-brand .footer-logo {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }

        .footer-logo-icon {
            width: 36px;
            height: 36px;
            background: linear-gradient(135deg, #c40233, #ff4466);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
        }

        .footer-logo-text {
            font-size: 1.1rem;
            font-weight: 700;
            color: #fff;
        }

        .footer-brand p {
            font-size: 0.85rem;
            color: #555;
            line-height: 1.7;
        }

        .footer-col h4 {
            color: #fff;
            font-size: 0.9rem;
            font-weight: 700;
            margin-bottom: 18px;
        }

        .footer-col ul { list-style: none; }
        .footer-col ul li { margin-bottom: 10px; }

        .footer-col ul li a {
            color: #555;
            text-decoration: none;
            font-size: 0.85rem;
            transition: color 0.2s;
        }

        .footer-col ul li a:hover { color: #ff4466; }

        .footer-bottom {
            max-width: 1100px;
            margin: 0 auto;
            padding-top: 25px;
            border-top: 1px solid #1a1a40;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.8rem;
            color: #444;
            flex-wrap: wrap;
            gap: 10px;
        }

        @media (max-width: 968px) {
            .hero { flex-direction: column; text-align: center; padding: 50px 30px; }
            .hero-left { max-width: 100%; }
            .hero-buttons { justify-content: center; }
            .hero-meta { justify-content: center; }
            .shield-visual { width: 300px; height: 300px; }
            .main-shield { width: 150px; height: 175px; }
            .main-shield .lion-emoji { font-size: 3rem; }
            .shield-circle-1 { width: 240px; height: 240px; }
            .shield-circle-2 { width: 280px; height: 280px; }
            .floating-badge { display: none; }
            .features-grid { grid-template-columns: 1fr; }
            .stats-grid { grid-template-columns: repeat(2, 1fr); }
            .plan-card { flex-direction: column; }
            .plan-right { width: 100%; }
            nav { padding: 15px 20px; }
            nav ul { display: none; }
            .hero h1 { font-size: 2.2rem; }
            .footer-top { grid-template-columns: 1fr 1fr; }
            .section-header h2 { font-size: 1.8rem; }
            .cta-section h2 { font-size: 1.8rem; }
        }
    </style>
</head>
<body>

    <div class="top-banner">
        🔥 Begränsat erbjudande: Få 60% rabatt på Anti Virus Lion Total Protection. <span onclick="downloadApp()">Hämta nu →</span>
    </div>

    <nav>
        <div class="nav-logo">
            <div class="nav-logo-icon">🦁</div>
            <div class="nav-logo-text">Anti Virus <span class="red">Lion</span></div>
        </div>
        <ul>
            <li><a href="#">Produkter</a></li>
            <li><a href="#features">Funktioner</a></li>
            <li><a href="#pricing">Priser</a></li>
            <li><a href="#">Support</a></li>
            <li><a href="#">Om oss</a></li>
            <li><a href="#" onclick="downloadApp(); return false;" class="nav-btn">Ladda ner</a></li>
        </ul>
    </nav>

    <section class="hero">
        <div class="hero-left">
            <div class="hero-badge">
                <div class="hero-badge-dot"></div>
                Uppdaterad 2025 — Ny AI-motor
            </div>
            <h1>Download<br><span class="red">Anti Virus</span> <span class="gold">Lion</span></h1>
            <p class="hero-desc">Skydda alla dina enheter med prisbelönt säkerhet. Avancerat skydd mot virus, ransomware, phishing och cyberhot — dygnet runt.</p>
            <div class="hero-buttons">
                <button class="btn-primary" onclick="downloadApp()">
                    ⬇️ Download Anti Virus Lion
                </button>
                <a href="#features" class="btn-secondary">
                    📋 Se alla funktioner
                </a>
            </div>
            <div class="hero-meta">
                <div class="hero-meta-item"><span class="check-green">✔</span> Gratis i 30 dagar</div>
                <div class="hero-meta-item"><span class="check-green">✔</span> Ingen kreditkort krävs</div>
                <div class="hero-meta-item"><span class="check-green">✔</span> 85 MB</div>
            </div>
        </div>
        <div class="hero-right">
            <div class="shield-visual">
                <div class="shield-bg"></div>
                <div class="shield-circle shield-circle-1"></div>
                <div class="shield-circle shield-circle-2"></div>
                <div class="main-shield">
                    <div class="lion-emoji">🦁</div>
                    <div class="shield-check">✓</div>
                </div>
                <div class="floating-badge floating-badge-1">
                    <div class="badge-icon green">✓</div>
                    <span>Skyddat</span>
                </div>
                <div class="floating-badge floating-badge-2">
                    <div class="badge-icon blue">🔒</div>
                    <span>Krypterat</span>
                </div>
                <div class="floating-badge floating-badge-3">
                    <div class="badge-icon red">🛡️</div>
                    <span>Realtid</span>
                </div>
            </div>
        </div>
    </section>

    <div class="trust-bar">
        <div class="trust-label">Testat & godkänt av</div>
        <div class="trust-logos">
            <div class="trust-item"><span>🏆</span> AV-TEST</div>
            <div class="trust-item"><span>⭐</span> PCMag</div>
            <div class="trust-item"><span>🥇</span> AV-Comparatives</div>
            <div class="trust-item"><span>🔬</span> SE Labs</div>
            <div class="trust-item"><span>📰</span> TechRadar</div>
        </div>
    </div>

    <section class="stats-section">
        <div class="stats-grid">
            <div class="stat-item">
                <div class="stat-number" id="stat1">0</div>
                <div class="stat-desc">Aktiva användare världen över</div>
            </div>
            <div class="stat-item">
                <div class="stat-number"><span class="red-num">99.9</span>%</div>
                <div class="stat-desc">Virus detektionsgrad</div>
            </div>
            <div class="stat-item">
                <div class="stat-number" id="stat2">0</div>
                <div class="stat-desc">Hot blockerade varje dag</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">24/7</div>
                <div class="stat-desc">Realtidsövervakning & support</div>
            </div>
        </div>
    </section>

    <section class="features-section" id="features">
        <div class="section-header">
            <div class="section-label">Funktioner</div>
            <h2>Komplett skydd för din digitala värld</h2>
            <p>Anti Virus Lion ger dig allt du behöver för att hålla dig säker online.</p>
        </div>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-card-icon">🛡️</div>
                <h3>Realtidsskydd</h3>
                <p>Kontinuerlig övervakning som stoppar hot direkt — innan de hinner orsaka skada.</p>
            </div>
            <div class="feature-card">
                <div class="feature-card-icon">🤖</div>
                <h3>Lion AI Engine</h3>
                <p>Vår AI-drivna motor analyserar beteendemönster och identifierar okända hot.</p>
            </div>
            <div class="feature-card">
                <div class="feature-card-icon">🌐</div>
                <h3>Webbskydd</h3>
                <p>Säker surfning med automatisk blockering av farliga webbsidor och phishing.</p>
            </div>
            <div class="feature-card">
                <div class="feature-card-icon">🔥</div>
                <h3>Brandvägg</h3>
                <p>Avancerad brandvägg som övervakar nätverkstrafik och blockerar obehörig åtkomst.</p>
            </div>
            <div class="feature-card">
                <div class="feature-card-icon">📧</div>
                <h3>E-postskydd</h3>
                <p>Skannar bilagor och länkar i e-post för att förhindra malware-attacker.</p>
            </div>
            <div class="feature-card">
                <div class="feature-card-icon">⚡</div>
                <h3>Prestanda-optimering</h3>
                <p>Rensar skräpfiler och optimerar systemet utan att sakta ner din dator.</p>
            </div>
        </div>
    </section>

    <section class="plan-section" id="pricing">
        <div class="section-header">
            <div class="section-label">Populärast</div>
            <h2>Total Protection</h2>
            <p>Allt-i-ett säkerhetslösning för hela familjen.</p>
        </div>
        <div class="plan-card">
            <div class="plan-left">
                <div class="plan-popular">🦁 Mest populär</div>
                <h3>Anti Virus Lion Total Protection</h3>
                <p class="plan-sub">Skydd för upp till 5 enheter</p>
                <ul class="plan-features">
                    <li><div class="plan-check">✓</div> Realtidsskydd mot virus & malware</li>
                    <li><div class="plan-check">✓</div> AI-driven hotdetektering</li>
                    <li><div class="plan-check">✓</div> Säker VPN (obegränsad data)</li>
                    <li><div class="plan-check">✓</div> Lösenordshanterare</li>
                    <li><div class="plan-check">✓</div> Identitetsskydd & övervakning</li>
                    <li><div class="plan-check">✓</div> Brandvägg & webbskydd</li>
                    <li><div class="plan-check">✓</div> Föräldrakontroll</li>
                    <li><div class="plan-check">✓</div> 24/7 kundsupport</li>
                </ul>
            </div>
            <div class="plan-right">
                <div class="plan-price-label">Från</div>
                <div class="plan-price"><span class="small">kr</span>29<span class="small">/mån</span></div>
                <div class="plan-price-sub">Faktureras årsvis. Spara 60%</div>
                <button class="plan-download-btn" onclick="downloadApp()">
                    ⬇️ Download Nu
                </button>
                <div class="plan-guarantee">🔒 30 dagars pengarna-tillbaka-garanti</div>
            </div>
        </div>
    </section>

    <section class="devices-section">
        <h3>Fungerar på alla dina enheter</h3>
        <div class="devices-row">
            <div class="device-item"><div class="device-icon">🖥️</div>Windows</div>
            <div class="device-item"><div class="device-icon">🍎</div>macOS</div>
            <div class="device-item"><div class="device-icon">📱</div>Android</div>
            <div class="device-item"><div class="device-icon">📲</div>iOS</div>
            <div class="device-item"><div class="device-icon">🐧</div>Linux</div>
        </div>
    </section>

    <section class="cta-section">
        <h2>🦁 Skydda dig idag med Anti Virus Lion</h2>
        <p>Gå med över 10 miljoner användare som litar på Lion för sin digitala säkerhet.</p>
        <button class="btn-white" onclick="downloadApp()">
            ⬇️ Download Anti Virus Lion — Gratis
        </button>
    </section>

    <footer>
        <div class="footer-top">
            <div class="footer-brand">
                <div class="footer-logo">
                    <div class="footer-logo-icon">🦁</div>
                    <div class="footer-logo-text">Anti Virus Lion</div>
                </div>
                <p>Anti Virus Lion ger dig förstklassigt skydd mot alla typer av digitala hot.</p>
            </div>
            <div class="footer-col">
                <h4>Produkter</h4>
                <ul>
                    <li><a href="#">Total Protection</a></li>
                    <li><a href="#">Internet Security</a></li>
                    <li><a href="#">VPN</a></li>
                    <li><a href="#">Identitetsskydd</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Resurser</h4>
                <ul>
                    <li><a href="#">Blogg</a></li>
                    <li><a href="#">Säkerhetstips</a></li>
                    <li><a href="#">FAQ</a></li>
                    <li><a href="#">Kontakta oss</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Företag</h4>
                <ul>
                    <li><a href="#">Om oss</a></li>
                    <li><a href="#">Karriär</a></li>
                    <li><a href="#">Integritetspolicy</a></li>
                    <li><a href="#">Villkor</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <span>© 2025 Anti Virus Lion. Alla rättigheter förbehållna.</span>
            <span>Gjord med 🦁 för din säkerhet</span>
        </div>
    </footer>

    <script>
        // DOWNLOAD FUNCTION - skapar filen och laddar ner den direkt
        function downloadApp() {
            const appCode = `<!DOCTYPE html>
<html lang="sv">
<head>
<meta charset="UTF-8">
<title>Anti Virus Lion - Scanner</title>
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Segoe UI',sans-serif;background:#0d0d2b;color:#fff;min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center}
.container{text-align:center;max-width:500px;padding:20px;width:100%}
.logo{font-size:5rem;margin-bottom:20px}
h1{font-size:2rem;margin-bottom:5px}
h1 .red{color:#c40233}
h1 .gold{color:#d4900a}
.version{color:#666;margin-bottom:30px;font-size:0.9rem}
.progress-container{background:#1a1a40;border-radius:12px;padding:30px;margin-bottom:25px}
.progress-text{margin-bottom:15px;font-size:0.95rem;color:#aaa}
.progress-bar{width:100%;height:12px;background:#2a2a50;border-radius:6px;overflow:hidden;margin-bottom:10px}
.progress-fill{height:100%;width:0%;background:linear-gradient(90deg,#c40233,#ff4466);border-radius:6px;transition:width 0.3s}
.percent{color:#ff4466;font-weight:700;font-size:1.2rem}
.status{background:#1a1a40;border-radius:12px;padding:20px;margin-bottom:20px}
.status-item{display:flex;align-items:center;gap:10px;padding:8px 0;font-size:0.9rem;color:#888;text-align:left}
.status-item.done{color:#22c55e}
.status-item.active{color:#ff4466}
.shield-status{margin-top:20px;padding:15px;border-radius:10px;font-weight:700;font-size:1.1rem}
.shield-protected{background:rgba(34,197,94,0.1);border:1px solid rgba(34,197,94,0.3);color:#22c55e}
.footer-text{color:#444;font-size:0.75rem;margin-top:20px}
.scan-btn{background:linear-gradient(135deg,#c40233,#e8053a);color:#fff;border:none;padding:14px 35px;border-radius:25px;font-size:1rem;font-weight:700;cursor:pointer;margin-top:15px;transition:all 0.3s}
.scan-btn:hover{transform:scale(1.05);box-shadow:0 5px 20px rgba(196,2,51,0.4)}
.hidden{display:none}
.threat-found{background:rgba(196,2,51,0.1);border:1px solid rgba(196,2,51,0.3);color:#ff4466;padding:10px;border-radius:8px;margin-top:10px;font-size:0.85rem;text-align:left}
.threat-clean{background:rgba(34,197,94,0.1);border:1px solid rgba(34,197,94,0.3);color:#22c55e;padding:10px;border-radius:8px;margin-top:10px;font-size:0.85rem}
.info-box{background:#1a1a40;border-radius:12px;padding:20px;margin-top:15px;text-align:left}
.info-row{display:flex;justify-content:space-between;padding:6px 0;font-size:0.85rem;border-bottom:1px solid #2a2a50}
.info-row:last-child{border:none}
.info-label{color:#666}
.info-value{color:#fff;font-weight:600}
.rescan-btn{background:transparent;border:2px solid #c40233;color:#c40233;padding:12px 30px;border-radius:25px;font-size:0.9rem;font-weight:600;cursor:pointer;margin-top:15px;transition:all 0.3s}
.rescan-btn:hover{background:#c40233;color:#fff}
</style>
</head>
<body>
<div class="container">
<div class="logo">🦁</div>
<h1><span class="red">Anti Virus</span> <span class="gold">Lion</span></h1>
<div class="version">Version 2025.1 — Total Protection</div>
<div class="progress-container">
<div class="progress-text" id="progressText">Klicka för att starta skanning...</div>
<div class="progress-bar"><div class="progress-fill" id="progressFill"></div></div>
<div class="percent" id="percent">0%</div>
</div>
<button class="scan-btn" id="scanBtn" onclick="startScan()">🔍 Starta Skanning</button>
<div class="status hidden" id="statusBox">
<div class="status-item" id="s1">⏳ Kontrollerar systemfiler...</div>
<div class="status-item" id="s2">⏳ Skannar nedladdningar...</div>
<div class="status-item" id="s3">⏳ Kontrollerar webbläsare...</div>
<div class="status-item" id="s4">⏳ Skannar register...</div>
<div class="status-item" id="s5">⏳ Letar efter malware...</div>
<div class="status-item" id="s6">⏳ Kontrollerar nätverk...</div>
</div>
<div class="hidden" id="result"></div>
<div class="hidden" id="infoBox"></div>
<div class="footer-text">Anti Virus Lion © 2025 — Skyddar din digitala värld 🦁</div>
</div>
<script>
function startScan(){
var btn=document.getElementById('scanBtn');
var statusBox=document.getElementById('statusBox');
var fill=document.getElementById('progressFill');
var percent=document.getElementById('percent');
var text=document.getElementById('progressText');
var result=document.getElementById('result');
var infoBox=document.getElementById('infoBox');
btn.classList.add('hidden');
statusBox.classList.remove('hidden');
text.textContent='Skannar ditt system...';
var progress=0;
var steps=[{id:'s1',at:10},{id:'s2',at:25},{id:'s3',at:42},{id:'s4',at:58},{id:'s5',at:75},{id:'s6',at:90}];
var filesScanned=0;
var interval=setInterval(function(){
progress+=1;
filesScanned+=Math.floor(Math.random()*847)+100;
fill.style.width=progress+'%';
percent.textContent=progress+'%';
text.textContent='Skannar... '+filesScanned.toLocaleString()+' filer kontrollerade';
steps.forEach(function(step){
var el=document.getElementById(step.id);
if(progress>=step.at+12){
if(!el.classList.contains('done')){el.className='status-item done';el.innerHTML='✅'+el.innerHTML.substring(1)}
}else if(progress>=step.at){
if(!el.classList.contains('active')){el.className='status-item active';el.innerHTML='🔍'+el.innerHTML.substring(1)}
}
});
if(progress>=100){
clearInterval(interval);
text.textContent='Skanning klar! '+filesScanned.toLocaleString()+' filer kontrollerade';
fill.style.background='linear-gradient(90deg,#22c55e,#4ade80)';
percent.style.color='#22c55e';
result.classList.remove('hidden');
result.innerHTML='<div class="shield-status shield-protected">🛡️ Ditt system är skyddat! Inga hot hittades.</div><div class="threat-clean">✅ 0 virus hittade<br>✅ 0 malware hittade<br>✅ 0 spyware hittade<br>✅ Brandvägg aktiv<br>✅ Webbskydd aktivt</div>';
infoBox.classList.remove('hidden');
infoBox.innerHTML='<div class="info-box"><div class="info-row"><span class="info-label">Filer skannade</span><span class="info-value">'+filesScanned.toLocaleString()+'</span></div><div class="info-row"><span class="info-label">Hot hittade</span><span class="info-value" style="color:#22c55e">0</span></div><div class="info-row"><span class="info-label">Skyddsnivå</span><span class="info-value" style="color:#22c55e">Utmärkt</span></div><div class="info-row"><span class="info-label">Senaste uppdatering</span><span class="info-value">Idag</span></div><div class="info-row"><span class="info-label">Licens</span><span class="info-value">Total Protection</span></div></div><button class="rescan-btn" onclick="location.reload()">🔄 Skanna igen</button>';
}
},80);
}
</script>
</body>
</html>`;

            var blob = new Blob([appCode], {type: 'text/html'});
            var url = URL.createObjectURL(blob);
            var a = document.createElement('a');
            a.href = url;
            a.download = 'AntiVirusLion_Setup.html';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
        }

        // Animate counters
        function animateCounter(id, target) {
            var el = document.getElementById(id);
            var current = 0;
            var increment = target / 60;
            var timer = setInterval(function() {
                current += increment;
                if (current >= target) { current = target; clearInterval(timer); }
                if (target >= 1000000) { el.textContent = (current / 1000000).toFixed(1) + 'M+'; }
                else if (target >= 1000) { el.textContent = Math.floor(current / 1000) + 'K+'; }
            }, 30);
        }

        var statsSection = document.querySelector('.stats-section');
        var statsCounted = false;
        var observer = new IntersectionObserver(function(entries) {
            if (entries[0].isIntersecting && !statsCounted) {
                statsCounted = true;
                animateCounter('stat1', 10000000);
                animateCounter('stat2', 850000);
            }
        }, { threshold: 0.3 });
        observer.observe(statsSection);

        var cards = document.querySelectorAll('.feature-card');
        var cardObserver = new IntersectionObserver(function(entries) {
            entries.forEach(function(entry, index) {
                if (entry.isIntersecting) {
                    setTimeout(function() {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }, index * 100);
                }
            });
        }, { threshold: 0.1 });

        cards.forEach(function(card) {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.transition = 'all 0.6s ease';
            cardObserver.observe(card);
        });
    </script>
</body>
</html>
