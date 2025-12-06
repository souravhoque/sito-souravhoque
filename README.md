<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8" />
  <title>Sourav Hoque – Excel Systems di Livello Superiore</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Excel Systems di Livello Superiore. Piattaforma Excel di nuova generazione per aziende moderne: turni, gestione personale, controllo produttivo e automazione avanzata." />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg-main: #050713;
      --bg-card: rgba(10, 14, 35, 0.85);
      --bg-card-soft: rgba(15, 20, 55, 0.8);
      --accent: #4af2c5;
      --accent2: #7c5cff;
      --text-main: #f5f7ff;
      --text-soft: #a2a8d8;
      --border-glass: rgba(255, 255, 255, 0.08);
      --shadow-soft: 0 24px 80px rgba(0, 0, 0, 0.7);
      --radius-xl: 24px;
      --transition-fast: 0.2s ease-out;
      --transition-slow: 0.5s ease-out;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background: radial-gradient(circle at top, #151b3a 0, #050713 55%, #020309 100%);
      color: var(--text-main);
      min-height: 100vh;
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* ====== BACKGROUND VIDEO ====== */
    .bg-video {
      position: fixed;
      inset: 0;
      overflow: hidden;
      z-index: -2;
    }

    .bg-video video {
      position: absolute;
      min-width: 100%;
      min-height: 100%;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      object-fit: cover;
      filter: saturate(1.3) contrast(1.2) blur(0.3px);
      opacity: 0.45;
    }

    .bg-overlay {
      position: fixed;
      inset: 0;
      background: radial-gradient(circle at top, rgba(76, 255, 209, 0.25), transparent 45%),
                  radial-gradient(circle at bottom, rgba(124, 92, 255, 0.2), transparent 55%),
                  linear-gradient(135deg, rgba(0, 0, 0, 0.9), rgba(3, 7, 25, 0.95));
      z-index: -1;
      pointer-events: none;
    }

    /* ====== LAYOUT ====== */
    .page-wrap {
      max-width: 1240px;
      margin: 0 auto;
      padding: 24px 16px 60px;
    }

    @media (min-width: 992px) {
      .page-wrap {
        padding: 32px 12px 80px;
      }
    }

    /* ====== NAVBAR ====== */
    .nav {
      position: sticky;
      top: 0;
      z-index: 99;
      backdrop-filter: blur(18px);
      background: linear-gradient(90deg, rgba(3, 6, 20, 0.96), rgba(10, 10, 40, 0.92));
      border: 1px solid rgba(255, 255, 255, 0.04);
      box-shadow: 0 18px 45px rgba(0, 0, 0, 0.6);
      border-radius: 999px;
      padding: 10px 18px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      margin-bottom: 28px;
    }

    .logo-wrap {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-mark {
      width: 40px;
      height: 40px;
      border-radius: 16px;
      background: radial-gradient(circle at 30% 0, var(--accent), transparent 60%),
                  radial-gradient(circle at 0 100%, var(--accent2), transparent 55%),
                  radial-gradient(circle at 100% 0, #00ffd1, transparent 55%),
                  #050713;
      box-shadow:
        0 0 18px rgba(74, 242, 197, 0.65),
        0 0 32px rgba(124, 92, 255, 0.7);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      font-size: 16px;
      letter-spacing: 1px;
    }

    .logo-mark span {
      background: linear-gradient(135deg, #eaffff, #a7f6d9);
      -webkit-background-clip: text;
      color: transparent;
    }

    .logo-text-main {
      font-size: 15px;
      font-weight: 600;
      letter-spacing: 0.06em;
      text-transform: uppercase;
    }

    .logo-text-sub {
      font-size: 11px;
      color: var(--text-soft);
      opacity: 0.9;
    }

    .nav-links {
      display: none;
      align-items: center;
      gap: 10px;
      font-size: 13px;
    }

    .nav-links a {
      padding: 6px 12px;
      border-radius: 999px;
      color: var(--text-soft);
      border: 1px solid transparent;
      cursor: pointer;
      transition: var(--transition-fast);
      font-weight: 400;
      white-space: nowrap;
    }

    .nav-links a:hover {
      color: var(--accent);
      border-color: rgba(74, 242, 197, 0.45);
      background: radial-gradient(circle at top, rgba(74, 242, 197, 0.12), transparent 60%);
    }

    .nav-cta {
      display: none;
      align-items: center;
      gap: 10px;
    }

    .btn {
      border-radius: 999px;
      padding: 8px 18px;
      font-size: 13px;
      border: 1px solid transparent;
      cursor: pointer;
      transition: var(--transition-fast);
      font-weight: 500;
      letter-spacing: 0.03em;
      text-transform: uppercase;
    }

    .btn-outline {
      background: transparent;
      border-color: rgba(255, 255, 255, 0.12);
      color: var(--text-soft);
    }

    .btn-outline:hover {
      border-color: rgba(74, 242, 197, 0.7);
      color: var(--accent);
      background: radial-gradient(circle at top, rgba(74, 242, 197, 0.15), transparent 55%);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      color: #050713;
      box-shadow:
        0 10px 30px rgba(74, 242, 197, 0.35),
        0 0 40px rgba(124, 92, 255, 0.55);
    }

    .btn-primary:hover {
      filter: brightness(1.1);
      transform: translateY(-1px);
      box-shadow:
        0 16px 40px rgba(74, 242, 197, 0.55),
        0 0 55px rgba(124, 92, 255, 0.7);
    }

    .nav-burger {
      width: 30px;
      height: 24px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      cursor: pointer;
    }

    .nav-burger span {
      display: block;
      height: 2px;
      border-radius: 999px;
      background: linear-gradient(90deg, var(--accent), var(--accent2));
    }

    .nav-mobile-menu {
      margin-top: 10px;
      padding: 12px 16px;
      border-radius: 18px;
      background: rgba(2, 4, 15, 0.96);
      border: 1px solid rgba(255, 255, 255, 0.05);
      display: none;
      flex-direction: column;
      gap: 8px;
      font-size: 14px;
    }

    .nav-mobile-menu a {
      padding: 6px 4px;
      color: var(--text-soft);
    }

    .nav-mobile-menu a:hover {
      color: var(--accent);
    }

    @media (min-width: 900px) {
      .nav {
        padding: 10px 22px;
      }
      .nav-links {
        display: flex;
      }
      .nav-cta {
        display: flex;
      }
      .nav-burger {
        display: none;
      }
      .nav-mobile-menu {
        display: none !important;
      }
    }

    /* ====== HERO ====== */
    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr);
      gap: 24px;
      margin-top: 8px;
      margin-bottom: 40px;
    }

    @media (min-width: 900px) {
      .hero {
        grid-template-columns: minmax(0, 1.4fr) minmax(0, 1.1fr);
        align-items: stretch;
        margin-bottom: 52px;
      }
    }

    .hero-left {
      padding: 20px 20px 24px;
      border-radius: var(--radius-xl);
      background: linear-gradient(135deg, rgba(12, 20, 65, 0.96), rgba(7, 9, 30, 0.98));
      border: 1px solid rgba(133, 241, 211, 0.18);
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-left::before {
      content: "";
      position: absolute;
      width: 200%;
      height: 200%;
      top: -50%;
      left: -50%;
      background:
        radial-gradient(circle at 20% 0, rgba(74, 242, 197, 0.13), transparent 60%),
        radial-gradient(circle at 80% 100%, rgba(124, 92, 255, 0.16), transparent 60%);
      mix-blend-mode: screen;
      opacity: 0.85;
      pointer-events: none;
    }

    .hero-chip-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 12px;
      position: relative;
      z-index: 1;
    }

    .chip {
      padding: 4px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.09em;
      color: var(--text-soft);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: rgba(8, 11, 30, 0.9);
      backdrop-filter: blur(10px);
    }

    .chip-dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: radial-gradient(circle, var(--accent), transparent);
      box-shadow: 0 0 12px rgba(74, 242, 197, 0.8);
    }

    .hero-title {
      position: relative;
      z-index: 1;
      font-size: clamp(28px, 4vw, 36px);
      line-height: 1.1;
      margin-bottom: 10px;
    }

    .hero-title span.accent {
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      -webkit-background-clip: text;
      color: transparent;
      text-shadow: 0 0 18px rgba(74, 242, 197, 0.8);
    }

    .hero-subtitle {
      position: relative;
      z-index: 1;
      font-size: 14px;
      line-height: 1.5;
      color: var(--text-soft);
      margin-bottom: 18px;
    }

    .hero-subtitle strong {
      color: #e9f5ff;
      font-weight: 500;
    }

    .hero-actions {
      position: relative;
      z-index: 1;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      align-items: center;
      margin-bottom: 16px;
    }

    .hero-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      font-size: 12px;
      color: var(--text-soft);
      position: relative;
      z-index: 1;
      margin-bottom: 4px;
    }

    .hero-meta span {
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .meta-pill {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      box-shadow: 0 0 12px rgba(124, 92, 255, 0.8);
    }

    .hero-footnote {
      font-size: 11px;
      color: var(--text-soft);
      opacity: 0.85;
      position: relative;
      z-index: 1;
    }

    .hero-right {
      border-radius: var(--radius-xl);
      background: var(--bg-card-soft);
      border: 1px solid rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(18px);
      box-shadow: var(--shadow-soft);
      padding: 16px;
      display: grid;
      grid-template-rows: auto auto;
      gap: 12px;
    }

    .hero-dashboard-preview {
      border-radius: 18px;
      border: 1px solid rgba(92, 255, 207, 0.18);
      background: radial-gradient(circle at top, rgba(74, 242, 197, 0.16), transparent 60%),
                  rgba(4, 6, 20, 0.98);
      padding: 12px;
      position: relative;
      overflow: hidden;
    }

    .hero-dashboard-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 8px;
      font-size: 11px;
      color: var(--text-soft);
    }

    .hero-dots {
      display: flex;
      gap: 4px;
    }

    .hero-dots span {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: radial-gradient(circle, rgba(255, 255, 255, 0.9), transparent);
      opacity: 0.7;
    }

    .mini-tabs {
      display: flex;
      gap: 5px;
      font-size: 10px;
    }

    .mini-tab {
      padding: 3px 7px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.14);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .mini-tab.active {
      background: linear-gradient(135deg, rgba(74, 242, 197, 0.23), rgba(124, 92, 255, 0.5));
      border-color: rgba(184, 255, 232, 0.9);
      color: #050713;
      font-weight: 600;
      box-shadow: 0 0 18px rgba(124, 92, 255, 0.85);
    }

    .hero-dashboard-grid {
      display: grid;
      grid-template-columns: 1.1fr 1fr;
      gap: 10px;
      align-items: stretch;
    }

    .hero-chart-card,
    .hero-kpi-card {
      border-radius: 14px;
      background: rgba(3, 7, 25, 0.9);
      border: 1px solid rgba(255, 255, 255, 0.09);
      padding: 8px 9px;
      font-size: 10px;
    }

    .hero-chart-bars {
      margin-top: 8px;
      display: flex;
      gap: 4px;
      align-items: flex-end;
      height: 64px;
    }

    .hero-chart-bar {
      flex: 1;
      border-radius: 999px;
      background: linear-gradient(180deg, rgba(74, 242, 197, 0.95), rgba(10, 15, 40, 0));
      box-shadow: 0 0 14px rgba(74, 242, 197, 0.6);
      transform-origin: bottom;
      animation: chartPulse 2.5s ease-in-out infinite alternate;
    }

    .hero-chart-bar:nth-child(2) {
      height: 70%;
      animation-delay: 0.15s;
    }

    .hero-chart-bar:nth-child(3) {
      height: 100%;
      animation-delay: 0.3s;
    }

    .hero-chart-bar:nth-child(4) {
      height: 52%;
      animation-delay: 0.45s;
    }

    .hero-kpi-row {
      display: flex;
      justify-content: space-between;
      gap: 8px;
      margin-top: 6px;
    }

    .hero-kpi-pill {
      flex: 1;
      padding: 6px 7px;
      border-radius: 10px;
      background: radial-gradient(circle at top, rgba(124, 92, 255, 0.28), transparent 65%);
      border: 1px solid rgba(193, 167, 255, 0.7);
      text-align: left;
    }

    .hero-kpi-pill strong {
      display: block;
      font-size: 11px;
    }

    .hero-kpi-pill span {
      font-size: 9px;
      color: var(--text-soft);
    }

    .hero-stats-row {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 8px;
      font-size: 10px;
    }

    .hero-stat-badge {
      padding: 8px 8px;
      border-radius: 14px;
      background: rgba(7, 10, 35, 0.96);
      border: 1px solid rgba(255, 255, 255, 0.06);
      display: flex;
      flex-direction: column;
      gap: 2px;
    }

    .hero-stat-label {
      color: var(--text-soft);
      font-size: 9px;
    }

    .hero-stat-value {
      font-weight: 600;
      font-size: 13px;
    }

    .hero-stat-tag {
      font-size: 9px;
      color: var(--accent);
    }

    .hero-right-footer {
      font-size: 11px;
      color: var(--text-soft);
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
    }

    .hero-right-footer span.highlight {
      color: var(--accent);
    }

    @keyframes chartPulse {
      0% {
        transform: scaleY(0.85);
      }
      100% {
        transform: scaleY(1.05);
      }
    }

    /* ====== SECTIONS GENERALI ====== */
    .section {
      margin-bottom: 40px;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 10px;
      margin-bottom: 16px;
    }

    .section-title {
      font-size: 18px;
      font-weight: 600;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: #e6ebff;
    }

    .section-subtitle {
      font-size: 13px;
      color: var(--text-soft);
      max-width: 480px;
    }

    .section-tag {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--accent);
    }

    /* ====== CARDS GENERALI ====== */
    .grid-3 {
      display: grid;
      grid-template-columns: minmax(0, 1fr);
      gap: 14px;
    }

    @media (min-width: 800px) {
      .grid-3 {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }
    }

    .card {
      border-radius: var(--radius-xl);
      background: var(--bg-card);
      border: 1px solid var(--border-glass);
      box-shadow: var(--shadow-soft);
      padding: 16px 16px 18px;
      position: relative;
      overflow: hidden;
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), border-color var(--transition-fast), background var(--transition-fast);
    }

    .card::before {
      content: "";
      position: absolute;
      inset: -40%;
      background:
        radial-gradient(circle at top left, rgba(74, 242, 197, 0.12), transparent 65%),
        radial-gradient(circle at bottom right, rgba(124, 92, 255, 0.16), transparent 65%);
      opacity: 0;
      transition: opacity var(--transition-slow);
      pointer-events: none;
      mix-blend-mode: screen;
    }

    .card:hover {
      transform: translateY(-4px) translateZ(0);
      box-shadow:
        0 26px 60px rgba(0, 0, 0, 0.9),
        0 0 28px rgba(74, 242, 197, 0.35);
      border-color: rgba(147, 255, 226, 0.45);
      background: rgba(6, 10, 36, 0.98);
    }

    .card:hover::before {
      opacity: 1;
    }

    .card-label {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--text-soft);
      margin-bottom: 6px;
    }

    .card-title {
      font-size: 16px;
      font-weight: 600;
      margin-bottom: 6px;
    }

    .card-desc {
      font-size: 12px;
      color: var(--text-soft);
      margin-bottom: 10px;
    }

    .card-meta-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
      font-size: 11px;
      color: var(--text-soft);
    }

    .badge {
      font-size: 10px;
      padding: 4px 8px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      text-transform: uppercase;
      letter-spacing: 0.1em;
    }

    .badge-accent {
      border-color: rgba(74, 242, 197, 0.8);
      color: var(--accent);
      background: rgba(10, 45, 36, 0.7);
    }

    .badge-soft {
      background: rgba(10, 14, 35, 0.9);
      color: var(--text-soft);
    }

    /* ====== VETRINA TEMPLATE ====== */
    .templates-layout {
      display: grid;
      grid-template-columns: minmax(0, 1.6fr) minmax(0, 1.1fr);
      gap: 18px;
    }

    @media (max-width: 899px) {
      .templates-layout {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .templates-main {
      border-radius: var(--radius-xl);
      background: var(--bg-card-soft);
      border: 1px solid rgba(255, 255, 255, 0.08);
      padding: 16px 16px 18px;
      box-shadow: var(--shadow-soft);
    }

    .filter-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 12px;
      font-size: 11px;
    }

    .filter-pill {
      padding: 4px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.15);
      color: var(--text-soft);
      cursor: pointer;
      text-transform: uppercase;
      letter-spacing: 0.11em;
      background: rgba(4, 7, 24, 0.95);
      transition: var(--transition-fast);
    }

    .filter-pill.active {
      border-color: rgba(74, 242, 197, 0.85);
      color: var(--accent);
      background: radial-gradient(circle at top, rgba(74, 242, 197, 0.2), transparent 60%);
      box-shadow: 0 0 18px rgba(74, 242, 197, 0.55);
    }

    .template-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
    }

    @media (max-width: 640px) {
      .template-grid {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .template-card {
      border-radius: 14px;
      background: rgba(5, 8, 28, 0.98);
      border: 1px solid rgba(255, 255, 255, 0.08);
      padding: 10px;
      font-size: 11px;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      gap: 6px;
      transition: var(--transition-fast);
    }

    .template-card:hover {
      border-color: rgba(74, 242, 197, 0.8);
      transform: translateY(-3px);
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.9);
    }

    .template-name {
      font-size: 13px;
      font-weight: 500;
    }

    .template-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 4px;
      font-size: 10px;
      color: var(--text-soft);
    }

    .template-price-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 11px;
      margin-top: 4px;
    }

    .template-price {
      font-weight: 600;
      color: var(--accent);
    }

    .templates-side {
      border-radius: var(--radius-xl);
      background: var(--bg-card);
      border: 1px solid var(--border-glass);
      padding: 14px 14px 16px;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .side-highlight {
      border-radius: 14px;
      background: radial-gradient(circle at top, rgba(124, 92, 255, 0.28), transparent 65%);
      border: 1px solid rgba(184, 167, 255, 0.8);
      padding: 10px;
      font-size: 11px;
    }

    /* ====== PRICING ====== */
    .pricing-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1.1fr) minmax(0, 0.9fr);
      gap: 14px;
    }

    @media (max-width: 900px) {
      .pricing-grid {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .pricing-card {
      position: relative;
    }

    .pricing-price {
      font-size: 22px;
      font-weight: 600;
      margin-bottom: 6px;
    }

    .pricing-price span {
      font-size: 11px;
      font-weight: 400;
      color: var(--text-soft);
    }

    .pricing-list {
      list-style: none;
      font-size: 11px;
      color: var(--text-soft);
      display: grid;
      gap: 4px;
      margin-bottom: 10px;
    }

    .pricing-list li::before {
      content: "●";
      color: var(--accent);
      margin-right: 6px;
      font-size: 9px;
    }

    .ribbon {
      position: absolute;
      top: 10px;
      right: 14px;
      font-size: 10px;
      padding: 3px 8px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      color: #050713;
      text-transform: uppercase;
      letter-spacing: 0.1em;
    }

    /* ====== HOW IT WORKS ====== */
    .steps-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 12px;
    }

    @media (max-width: 800px) {
      .steps-grid {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .step-num {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--accent);
      margin-bottom: 4px;
    }

    /* ====== CHI SONO + FAQ + CONTATTI ====== */
    .two-column {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1.1fr);
      gap: 16px;
    }

    @media (max-width: 900px) {
      .two-column {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .faq-item {
      border-radius: 14px;
      background: rgba(6, 9, 30, 0.95);
      border: 1px solid rgba(255, 255, 255, 0.08);
      padding: 10px 12px;
      font-size: 12px;
      margin-bottom: 8px;
    }

    .faq-q {
      font-weight: 500;
      margin-bottom: 4px;
    }

    .faq-a {
      color: var(--text-soft);
      font-size: 11px;
    }

    .contact-card {
      border-radius: var(--radius-xl);
      background: var(--bg-card-soft);
      border: 1px solid rgba(255, 255, 255, 0.1);
      padding: 14px 14px 18px;
    }

    .contact-row {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1.1fr);
      gap: 10px;
      margin-bottom: 8px;
    }

    @media (max-width: 640px) {
      .contact-row {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .input-group {
      display: flex;
      flex-direction: column;
      gap: 4px;
      font-size: 11px;
      color: var(--text-soft);
    }

    .input-group label {
      text-transform: uppercase;
      letter-spacing: 0.12em;
    }

    .input-group input,
    .input-group textarea {
      border-radius: 10px;
      border: 1px solid rgba(255, 255, 255, 0.16);
      background: rgba(3, 6, 20, 0.96);
      color: var(--text-main);
      padding: 8px 10px;
      font-family: inherit;
      font-size: 12px;
      outline: none;
      resize: vertical;
      min-height: 36px;
    }

    .input-group textarea {
      min-height: 80px;
    }

    .input-group input:focus,
    .input-group textarea:focus {
      border-color: rgba(74, 242, 197, 0.9);
      box-shadow: 0 0 18px rgba(74, 242, 197, 0.55);
    }

    .small-text {
      font-size: 10px;
      color: var(--text-soft);
    }

    /* ====== FOOTER ====== */
    .footer {
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid rgba(255, 255, 255, 0.06);
      font-size: 11px;
      color: var(--text-soft);
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 8px;
    }

    .footer span.highlight {
      color: var(--accent);
    }
  </style>
</head>
<body>
  <!-- VIDEO SFONDO: sostituisci src con il tuo video ologramma/AI -->
  <div class="bg-video">
    <video autoplay muted loop playsinline>
      <!-- Metti qui il tuo file mp4, ad es.: video/sourav-ai-loop.mp4 -->
      <source src="https://cdn.coverr.co/videos/coverr-futuristic-interface-technology-6041/1080p.mp4" type="video/mp4" />
    </video>
  </div>
  <div class="bg-overlay"></div>

  <div class="page-wrap">
    <!-- NAVBAR -->
    <header class="nav">
      <div class="logo-wrap">
        <div class="logo-mark">
          <!-- Logo futuristico: puoi cambiare "SH" se vuoi -->
          <span>SH</span>
        </div>
        <div>
          <div class="logo-text-main">Sourav Hoque</div>
          <div class="logo-text-sub">Excel Systems di Livello Superiore</div>
        </div>
      </div>

      <nav class="nav-links">
        <a data-scroll="#hero">Home</a>
        <a data-scroll="#soluzioni">Soluzioni</a>
        <a data-scroll="#templates">Template</a>
        <a data-scroll="#pricing">Pacchetti</a>
        <a data-scroll="#chi-sono">Chi sono</a>
        <a data-scroll="#contatti">Contatti</a>
      </nav>

      <div class="nav-cta">
        <button class="btn btn-outline" data-scroll="#templates">Vedi i file</button>
        <button class="btn btn-primary" data-scroll="#contatti">Richiedi sistema su misura</button>
      </div>

      <div class="nav-burger" id="navBurger">
        <span></span><span></span><span></span>
      </div>
    </header>

    <div class="nav-mobile-menu" id="navMobileMenu">
      <a data-scroll="#hero">Home</a>
      <a data-scroll="#soluzioni">Soluzioni</a>
      <a data-scroll="#templates">Template</a>
      <a data-scroll="#pricing">Pacchetti</a>
      <a data-scroll="#chi-sono">Chi sono</a>
      <a data-scroll="#contatti">Contatti</a>
    </div>

    <!-- HERO -->
    <main id="hero" class="hero">
      <section class="hero-left">
        <div class="hero-chip-row">
          <div class="chip">
            <span class="chip-dot"></span>
            Sistemi Excel di nuova generazione
          </div>
          <div class="chip">
            Automazione turni · Gestione DPI · Produzione
          </div>
        </div>

        <h1 class="hero-title">
          <span class="accent">Excel Systems di Livello Superiore</span><br />
          per aziende che vogliono controllo totale.
        </h1>

        <p class="hero-subtitle">
          Piattaforma Excel di nuova generazione per aziende moderne.  
          <strong>Sistemi intelligenti progettati per ottimizzare turni, gestione del personale, controllo produttivo</strong> e automazione avanzata dei processi aziendali.  
          Precisione, efficienza e controllo in un’unica soluzione professionale.
        </p>

        <div class="hero-actions">
          <button class="btn btn-primary" data-scroll="#templates">
            Sfoglia i template pronti
          </button>
          <button class="btn btn-outline" data-scroll="#pricing">
            Vedi pacchetti & licenze
          </button>
        </div>

        <div class="hero-meta">
          <span><span class="meta-pill"></span> Ottimizzato per turni, ferie, DPI e produzione</span>
          <span>✔ Pronto per cantiere, officina, produzione, servizi</span>
        </div>
        <div class="hero-footnote">
          Ogni file può essere personalizzato su misura per la tua realtà aziendale.
        </div>
      </section>

      <aside class="hero-right">
        <div class="hero-dashboard-preview">
          <div class="hero-dashboard-header">
            <div class="hero-dots">
              <span></span><span></span><span></span>
            </div>
            <div class="mini-tabs">
              <div class="mini-tab active">Turni</div>
              <div class="mini-tab">DPI</div>
              <div class="mini-tab">Produzione</div>
            </div>
          </div>

          <div class="hero-dashboard-grid">
            <div class="hero-chart-card">
              Turni di oggi · Vista sintetica
              <div class="hero-chart-bars">
                <div class="hero-chart-bar" style="height: 40%;"></div>
                <div class="hero-chart-bar"></div>
                <div class="hero-chart-bar"></div>
                <div class="hero-chart-bar"></div>
              </div>
            </div>
            <div class="hero-kpi-card">
              KPI in tempo reale
              <div class="hero-kpi-row">
                <div class="hero-kpi-pill">
                  <strong>97,3%</strong>
                  <span>Presenze regolari</span>
                </div>
                <div class="hero-kpi-pill">
                  <strong>0</strong>
                  <span>DPI scaduti</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="hero-stats-row">
          <div class="hero-stat-badge">
            <div class="hero-stat-label">Gestione turni</div>
            <div class="hero-stat-value">+35%</div>
            <div class="hero-stat-tag">Velocità pianificazione</div>
          </div>
          <div class="hero-stat-badge">
            <div class="hero-stat-label">Errori ridotti</div>
            <div class="hero-stat-value">-60%</div>
            <div class="hero-stat-tag">Convalida automatica dati</div>
          </div>
          <div class="hero-stat-badge">
            <div class="hero-stat-label">Analisi</div>
            <div class="hero-stat-value">Real-time</div>
            <div class="hero-stat-tag">Dashboard operative</div>
          </div>
        </div>

        <div class="hero-right-footer">
          <span>Interfacce pensate per chi lavora ogni giorno con i fogli di Excel.</span>
          <span class="highlight">Made by Sourav Hoque</span>
        </div>
      </aside>
    </main>

    <!-- SEZIONE: PERCHE' I SISTEMI -->
    <section id="soluzioni" class="section">
      <div class="section-header">
        <div>
          <div class="section-tag">Perché scegliere questi sistemi</div>
          <h2 class="section-title">Progettati per il lavoro reale, non per la teoria</h2>
        </div>
        <p class="section-subtitle">
          Ogni file nasce dall’esperienza diretta in cantiere, produzione e gestione del personale.
          Non sono modelli generici: sono sistemi già testati in situazioni reali.
        </p>
      </div>

      <div class="grid-3">
        <article class="card">
          <div class="card-label">01 · Ottimizzazione operativa</div>
          <h3 class="card-title">Turni, ferie e straordinari sempre sotto controllo</h3>
          <p class="card-desc">
            Pianificazione automatica dei turni, controllo ferie e assenze, gestione straordinari e banca ore.
            Tutto collegato in un’unica interfaccia, senza formule da inventare.
          </p>
          <div class="card-meta-row">
            <span class="badge badge-accent">Focus: Gestione Personale</span>
            <span>Riduci gli errori umani e risparmia ore ogni settimana.</span>
          </div>
        </article>

        <article class="card">
          <div class="card-label">02 · Sicurezza & DPI</div>
          <h3 class="card-title">Tracciamento DPI e scadenze in tempo reale</h3>
          <p class="card-desc">
            Dashboard per monitorare consegne, restituzioni e scadenze di caschi, scarpe, guanti, imbracature e altri DPI.
            Alert automatici per la sicurezza e la conformità.
          </p>
          <div class="card-meta-row">
            <span class="badge badge-soft">Allineato con procedure HSE</span>
            <span>Evita sorprese nei controlli del cliente.</span>
          </div>
        </article>

        <article class="card">
          <div class="card-label">03 · Controllo produttivo</div>
          <h3 class="card-title">Produzione, avanzamento e performance</h3>
          <p class="card-desc">
            Schede di produzione, avanzamento lavori, saturazione squadre e KPI grafici.
            Tutto visibile in pochi click, pronto per report a direzione e clienti.
          </p>
          <div class="card-meta-row">
            <span class="badge badge-soft">Dashboard dinamiche</span>
            <span>Ideale per officine, cantieri e reparti produttivi.</span>
          </div>
        </article>
      </div>
    </section>

    <!-- SEZIONE: VETRINA TEMPLATE -->
    <section id="templates" class="section">
      <div class="section-header">
        <div>
          <div class="section-tag">Vetrina template</div>
          <h2 class="section-title">File Excel pronti da usare e personalizzare</h2>
        </div>
        <p class="section-subtitle">
          Qui potrai inserire i tuoi file in vendita: ogni riquadro può rappresentare un template
          con descrizione, prezzo e breve anteprima funzionalità.
        </p>
      </div>

      <div class="templates-layout">
        <div class="templates-main">
          <div class="filter-row">
            <div class="filter-pill active" data-filter="all">Tutti</div>
            <div class="filter-pill" data-filter="turni">Turni & Personale</div>
            <div class="filter-pill" data-filter="dpi">DPI & Sicurezza</div>
            <div class="filter-pill" data-filter="produzione">Produzione</div>
            <div class="filter-pill" data-filter="hr">HR & Documenti</div>
          </div>

          <div class="template-grid" id="templateGrid">
            <!-- Esempio template – qui poi li sostituirai con i tuoi veri file -->
            <article class="template-card" data-category="turni">
              <div class="template-name">Gestione Turni Multifoglio</div>
              <div class="template-tags">
                <span>Turni 2/3 squadre</span>
                <span>Ferie & Permessi</span>
                <span>Dashboard presenze</span>
              </div>
              <div class="template-price-row">
                <span class="template-price">€ 39</span>
                <span>Ideale per cantieri e officine</span>
              </div>
            </article>

            <article class="template-card" data-category="dpi">
              <div class="template-name">Registro DPI con Scadenze</div>
              <div class="template-tags">
                <span>Consegne & Resi</span>
                <span>Alert scadenza</span>
                <span>Storico lavoratore</span>
              </div>
              <div class="template-price-row">
                <span class="template-price">€ 29</span>
                <span>Per responsabili sicurezza</span>
              </div>
            </article>

            <article class="template-card" data-category="produzione">
              <div class="template-name">Dashboard Avanzamento Produzione</div>
              <div class="template-tags">
                <span>Grafici automatici</span>
                <span>Ore lavorate</span>
                <span>Progress % lotto</span>
              </div>
              <div class="template-price-row">
                <span class="template-price">€ 49</span>
                <span>Per reparti produttivi</span>
              </div>
            </article>

            <article class="template-card" data-category="hr">
              <div class="template-name">Anagrafica Personale Pro</div>
              <div class="template-tags">
                <span>Contratti & scadenze</span>
                <span>Documenti</span>
                <span>Note disciplinari</span>
              </div>
              <div class="template-price-row">
                <span class="template-price">€ 35</span>
                <span>Per uffici HR</span>
              </div>
            </article>
          </div>
        </div>

        <aside class="templates-side">
          <div class="side-highlight">
            <strong>Anteprime realistiche dei tuoi sistemi</strong><br />
            Puoi inserire screenshot dei tuoi file Excel (dashboard, tabelle, grafici)
            direttamente qui o nella parte interna dei template.  
            Così il cliente vede subito come sarà il foglio.
          </div>
          <div class="card">
            <div class="card-label">Personalizzazione</div>
            <h3 class="card-title">Vuoi un sistema su misura?</h3>
            <p class="card-desc">
              A partire dai template base, è possibile richiedere una personalizzazione
              completa: nuove tabelle, formule, VBA, automazioni, grafici e layout
              grafici in stile futuristico.
            </p>
            <div class="card-meta-row">
              <span class="badge badge-accent">Su preventivo</span>
              <span>Contattami dalla sezione "Contatti".</span>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <!-- SEZIONE: PRICING -->
    <section id="pricing" class="section">
      <div class="section-header">
        <div>
          <div class="section-tag">Pacchetti & licenze</div>
          <h2 class="section-title">Scegli come iniziare con i sistemi Excel</h2>
        </div>
        <p class="section-subtitle">
          Puoi partire da un singolo file oppure da un set completo per la gestione
          totale di turni, DPI e produzione.
        </p>
      </div>

      <div class="pricing-grid">
        <article class="card pricing-card">
          <h3 class="card-title">Pacchetto Starter</h3>
          <p class="card-desc">
            Ideale per piccole realtà che vogliono iniziare a mettere ordine con pochi strumenti ma ben fatti.
          </p>
          <div class="pricing-price">€ 79 <span>una tantum</span></div>
          <ul class="pricing-list">
            <li>1 template a scelta (turni, DPI o produzione)</li>
            <li>Guida rapida per l’uso</li>
            <li>Piccole modifiche di layout incluse</li>
          </ul>
          <button class="btn btn-outline" data-scroll="#contatti">Richiedi info Starter</button>
        </article>

        <article class="card pricing-card">
          <div class="ribbon">Consigliato</div>
          <h3 class="card-title">Pacchetto Operations</h3>
          <p class="card-desc">
            Set coordinato di file per gestire turni, DPI e produzione con una logica unica e coerente.
          </p>
          <div class="pricing-price">€ 199 <span>una tantum</span></div>
          <ul class="pricing-list">
            <li>3 template completi (Turni · DPI · Produzione)</li>
            <li>Dashboard riassuntiva</li>
            <li>Personalizzazione base inclusa</li>
            <li>Supporto via email per l’avvio</li>
          </ul>
          <button class="btn btn-primary" data-scroll="#contatti">Richiedi Pacchetto Operations</button>
        </article>

        <article class="card pricing-card">
          <h3 class="card-title">Soluzione su Misura</h3>
          <p class="card-desc">
            Per aziende che vogliono un sistema costruito esattamente attorno al loro flusso di lavoro.
          </p>
          <div class="pricing-price">Su preventivo <span>progetto completo</span></div>
          <ul class="pricing-list">
            <li>Analisi del tuo processo</li>
            <li>Sistemi Excel custom · anche con VBA</li>
            <li>Layout grafico in stile futuristico</li>
            <li>Affiancamento all’avvio</li>
          </ul>
          <button class="btn btn-outline" data-scroll="#contatti">Parla con Sourav</button>
        </article>
      </div>
    </section>

    <!-- SEZIONE: HOW IT WORKS -->
    <section class="section">
      <div class="section-header">
        <div>
          <div class="section-tag">Come funziona</div>
          <h2 class="section-title">Dalla richiesta al file pronto in 4 passi</h2>
        </div>
      </div>

      <div class="steps-grid">
        <article class="card">
          <div class="step-num">Passo 1</div>
          <h3 class="card-title">Mi racconti come lavori oggi</h3>
          <p class="card-desc">
            Mi spieghi come gestisci attualmente turni, DPI, avanzamento o quello che ti serve.
            Anche con esempi, foto di fogli scritti a mano o file Excel che già usi.
          </p>
        </article>

        <article class="card">
          <div class="step-num">Passo 2</div>
          <h3 class="card-title">Definizione del sistema ideale</h3>
          <p class="card-desc">
            Insieme definiamo campi, tabelle, controlli, colori, dashboard e logiche di calcolo.
            Tutto pensando alla praticità di chi usa il file ogni giorno.
          </p>
        </article>

        <article class="card">
          <div class="step-num">Passo 3 & 4</div>
          <h3 class="card-title">Realizzazione · Test · Consegna</h3>
          <p class="card-desc">
            Creo il sistema, lo testiamo con dati reali e lo consegno pronto all’uso,
            con eventuali piccole modifiche finali incluse.
          </p>
        </article>
      </div>
    </section>

    <!-- SEZIONE: CHI SONO + FAQ -->
    <section id="chi-sono" class="section">
      <div class="two-column">
        <article class="card">
          <div class="card-label">Chi è Sourav Hoque</div>
          <h3 class="card-title">Sistemi Excel nati dal lavoro quotidiano</h3>
          <p class="card-desc">
            Lavoro ogni giorno con turni, persone, DPI, produzione e documenti.
            I sistemi che creo non sono solo “belli da vedere”, ma soprattutto utili, veloci
            e pensati per chi deve prendere decisioni in poco tempo.
          </p>
          <p class="card-desc">
            Negli anni ho sviluppato file Excel avanzati per:
          </p>
          <ul class="pricing-list">
            <li>Gestione turni su più reparti e squadre</li>
            <li>Monitoraggio DPI con scadenze e consegne</li>
            <li>Controllo avanzamento produttivo</li>
            <li>Dashboard per responsabili e titolari</li>
          </ul>
          <p class="card-desc">
            Il mio obiettivo è sempre lo stesso: trasformare Excel in un vero
            <strong>“sistema di controllo”</strong> per la tua azienda.
          </p>
        </article>

        <aside>
          <div class="section-tag" style="margin-bottom:8px;">Domande frequenti</div>

          <div class="faq-item">
            <div class="faq-q">Serve una versione particolare di Excel?</div>
            <div class="faq-a">
              I file sono pensati principalmente per Excel su PC (Windows).  
              Se hai esigenze specifiche (Excel Mac, 365, versione aziendale) lo valutiamo insieme.
            </div>
          </div>

          <div class="faq-item">
            <div class="faq-q">Posso modificare i file dopo l’acquisto?</div>
            <div class="faq-a">
              Sì, puoi modificare campi, colori e testi.  
              Per modifiche strutturali più complesse (nuove tabelle, automazioni, VBA) è disponibile
              il servizio di personalizzazione.
            </div>
          </div>

          <div class="faq-item">
            <div class="faq-q">Posso avere una demo prima?</div>
            <div class="faq-a">
              Possiamo concordare una breve call o uno scambio di screenshot/video
              per mostrarti l’interfaccia e verificare che il sistema sia adatto alle tue esigenze.
            </div>
          </div>
        </aside>
      </div>
    </section>

    <!-- SEZIONE: CONTATTI -->
    <section id="contatti" class="section">
      <div class="section-header">
        <div>
          <div class="section-tag">Contatti</div>
          <h2 class="section-title">Raccontami di cosa hai bisogno</h2>
        </div>
        <p class="section-subtitle">
          Compila il form con poche informazioni chiare.  
          Ti risponderò per proporre il file più adatto o una soluzione personalizzata.
        </p>
      </div>

      <div class="contact-card">
        <div class="contact-row">
          <div class="input-group">
            <label for="nome">Nome e azienda</label>
            <input id="nome" type="text" placeholder="Es. Marco – Officina XYZ" />
          </div>
          <div class="input-group">
            <label for="email">Email</label>
            <input id="email" type="email" placeholder="nome@azienda.it" />
          </div>
        </div>

        <div class="contact-row">
          <div class="input-group">
            <label for="selezione">Cosa ti interessa?</label>
            <input id="selezione" type="text" placeholder="Es. turni, DPI, produzione, altro..." />
          </div>
          <div class="input-group">
            <label for="dimensione">Dimensione squadra/reparto</label>
            <input id="dimensione" type="text" placeholder="Es. 15 operai, 3 reparti, 2 turni" />
          </div>
        </div>

        <div class="input-group" style="margin-bottom:10px;">
          <label for="messaggio">Descrivi brevemente la tua esigenza</label>
          <textarea id="messaggio" placeholder="Raccontami come gestisci oggi turni/DPI/produzione e cosa vorresti migliorare."></textarea>
        </div>

        <button class="btn btn-primary">Invia richiesta (simulazione front-end)</button>
        <p class="small-text" style="margin-top:8px;">
          Questo form è solo la parte grafica (front-end).  
          Per collegarlo alla tua email o ad altro sistema (es. invio via PHP, servizio esterno, ecc.)
          va aggiunta l’integrazione lato server.
        </p>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
      <span>© <span id="year"></span> Sourav Hoque – Excel Systems di Livello Superiore.</span>
      <span>Interfaccia futuristica progettata per mostrare il valore dei tuoi file Excel.</span>
    </footer>
  </div>

  <script>
    // Anno footer
    document.getElementById("year").textContent = new Date().getFullYear();

    // Smooth scroll
    function scrollToTarget(selector) {
      const el = document.querySelector(selector);
      if (!el) return;
      const rect = el.getBoundingClientRect();
      const offset = window.scrollY + rect.top - 90; // spazio per la navbar sticky
      window.scrollTo({ top: offset, behavior: "smooth" });
    }

    document.querySelectorAll("[data-scroll]").forEach(function (el) {
      el.addEventListener("click", function () {
        const target = this.getAttribute("data-scroll");
        scrollToTarget(target);
        // chiudi menu mobile se aperto
        const mm = document.getElementById("navMobileMenu");
        if (mm && mm.style.display === "flex") {
          mm.style.display = "none";
        }
      });
    });

    // Burger menu mobile
    const burger = document.getElementById("navBurger");
    const mobileMenu = document.getElementById("navMobileMenu");
    if (burger && mobileMenu) {
      burger.addEventListener("click", function () {
        mobileMenu.style.display = mobileMenu.style.display === "flex" ? "none" : "flex";
      });
    }

    // Filtro template
    const filterPills = document.querySelectorAll(".filter-pill");
    const templateCards = document.querySelectorAll(".template-card");

    filterPills.forEach(function (pill) {
      pill.addEventListener("click", function () {
        const filter = this.getAttribute("data-filter");
        filterPills.forEach(p => p.classList.remove("active"));
        this.classList.add("active");

        templateCards.forEach(function (card) {
          const cat = card.getAttribute("data-category");
          if (filter === "all" || filter === cat) {
            card.style.display = "flex";
          } else {
            card.style.display = "none";
          }
        });
      });
    });
  </script>
</body>
</html>
