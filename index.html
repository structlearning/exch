<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <title>Exchangeability of GNN Representations with Applications to Graph Retrieval</title>

  <!-- Fonts: Fraunces (display serif) + Inter (body sans) + JetBrains Mono (code) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

  <!-- MathJax -->
  <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: { inlineMath: [['$','$'], ['\\(','\\)']], displayMath: [['$$','$$'], ['\\[','\\]']] },
      TeX: { extensions: ["AMSmath.js","AMSsymbols.js","color.js"] },
      "HTML-CSS": { availableFonts: ["TeX"], scale: 100 },
      showProcessingMessages: false, messageStyle: "none"
    });
  </script>
  <script async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>

  <style>
    :root {
      --bg: #f5f1e8;              /* warm cream paper */
      --surface: #fdfaf3;          /* slightly lighter cream for cards */
      --ink: #1c2826;              /* deep blackened teal */
      --ink-soft: #2f3e3b;
      --muted: #6b7a76;
      --rule: #ddd4c0;
      --rule-soft: #e8e0cc;
      --accent: #8b3a2a;           /* deep russet / reddish-brown */
      --accent-soft: #b8745f;
      --accent-bg: #f5e7e0;
      --accent-2: #c8631e;         /* warm copper for secondary highlights */
      --accent-2-bg: #f9ede0;
      --tag-bg: #e8e0cc;
      --tag-ink: #4a5550;
      --code-bg: #efe8d4;
      --code-ink: #25302d;
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }
    html, body {
      margin: 0;
      padding: 0;
      background: var(--bg);
      color: var(--ink);
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.72;
      font-feature-settings: "ss01", "cv11";
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }
    body {
      font-size: 21px;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 0;
      background-image:
        radial-gradient(circle at 15% 0%, rgba(139, 58, 42, 0.04) 0%, transparent 45%),
        radial-gradient(circle at 85% 100%, rgba(200, 99, 30, 0.03) 0%, transparent 45%);
    }

    .navbar {
      position: sticky;
      top: 0;
      z-index: 50;
      background: rgba(245, 241, 232, 0.85);
      backdrop-filter: saturate(180%) blur(12px);
      -webkit-backdrop-filter: saturate(180%) blur(12px);
      border-bottom: 1px solid var(--rule);
      padding: 16px 0;
    }
    .navbar-inner {
      max-width: 1180px;
      margin: 0 auto;
      padding: 0 22px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      font-size: 14.5px;
    }
    .nav-brand {
      font-family: 'Fraunces', serif;
      font-weight: 600;
      font-size: 19px;
      color: var(--ink);
      text-decoration: none;
      letter-spacing: -0.01em;
    }
    .nav-brand .dot { color: var(--accent); }
    .nav-links { display: flex; gap: 28px; }
    .nav-links a {
      color: var(--ink-soft);
      text-decoration: none;
      font-weight: 500;
      transition: color 0.2s ease;
      position: relative;
    }
    .nav-links a:hover { color: var(--accent); }
    .nav-links .current { color: var(--accent); font-weight: 600; }
    .nav-links .current::after {
      content: "";
      position: absolute;
      left: 0; right: 0; bottom: -22px;
      height: 2px;
      background: var(--accent);
    }

    article {
      max-width: 1080px;
      margin: 0 auto;
      padding: 64px 18px 88px;
      position: relative;
      z-index: 1;
    }

    .hero {
      margin-bottom: 56px;
      animation: fadeUp 0.6s ease-out;
    }
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(8px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    /* === ICLR ORAL — prominent venue badge ===
       Two-tier ribbon: venue (left) + oral honour (right, accent-filled). */
    .venue-badge {
      display: inline-flex;
      align-items: stretch;
      font-family: 'Inter', sans-serif;
      margin-bottom: 26px;
      border-radius: 10px;
      overflow: hidden;
      border: 1.5px solid var(--accent);
      box-shadow:
        0 1px 0 rgba(255,255,255,0.6) inset,
        0 6px 20px -8px rgba(139, 58, 42, 0.35),
        0 2px 6px -2px rgba(139, 58, 42, 0.18);
      animation: badgeIn 0.7s cubic-bezier(0.2, 0.8, 0.25, 1) both;
      position: relative;
    }
    @keyframes badgeIn {
      0%   { opacity: 0; transform: translateY(-6px) scale(0.97); }
      100% { opacity: 1; transform: translateY(0) scale(1); }
    }
    .venue-badge .venue-side {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 14px 8px 16px;
      background: linear-gradient(180deg, #fdfaf3 0%, #f5e7e0 100%);
      color: var(--accent);
      font-size: 13px;
      font-weight: 700;
      letter-spacing: 0.06em;
      text-transform: uppercase;
    }
    .venue-badge .venue-side .conf {
      font-family: 'Fraunces', serif;
      font-weight: 600;
      font-size: 16px;
      letter-spacing: 0.01em;
      text-transform: none;
      color: var(--ink);
    }
    .venue-badge .venue-side .yr {
      font-family: 'JetBrains Mono', monospace;
      font-size: 12.5px;
      font-weight: 500;
      color: var(--muted);
      letter-spacing: 0;
      text-transform: none;
    }
    .venue-badge .divider {
      width: 1.5px;
      background: var(--accent);
      opacity: 0.85;
    }
    .venue-badge .oral-side {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 18px 8px 14px;
      background: linear-gradient(135deg, var(--accent) 0%, #6e2a1f 100%);
      color: #fff7ed;
      font-size: 13.5px;
      font-weight: 700;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      position: relative;
    }
    .venue-badge .oral-side::after {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(
        100deg,
        transparent 30%,
        rgba(255, 247, 237, 0.18) 48%,
        rgba(255, 247, 237, 0.32) 50%,
        rgba(255, 247, 237, 0.18) 52%,
        transparent 70%
      );
      animation: badgeShine 4.2s ease-in-out 0.9s infinite;
      pointer-events: none;
    }
    @keyframes badgeShine {
      0%   { transform: translateX(-110%); }
      55%  { transform: translateX(110%); }
      100% { transform: translateX(110%); }
    }
    .venue-badge .star {
      display: inline-block;
      font-size: 13px;
      color: #ffd9a8;
      filter: drop-shadow(0 0 4px rgba(255, 200, 130, 0.55));
      animation: starPulse 2.6s ease-in-out infinite;
    }
    @keyframes starPulse {
      0%, 100% { transform: scale(1);    opacity: 0.9; }
      50%      { transform: scale(1.15); opacity: 1;   }
    }
    @media (max-width: 540px) {
      .venue-badge { flex-wrap: wrap; }
      .venue-badge .venue-side, .venue-badge .oral-side { font-size: 12.5px; padding: 7px 12px; }
      .venue-badge .venue-side .conf { font-size: 15px; }
    }
    @media (prefers-reduced-motion: reduce) {
      .venue-badge, .venue-badge .oral-side::after, .venue-badge .star { animation: none; }
    }

    h1.post-title {
      font-family: 'Fraunces', serif;
      font-weight: 500;
      font-size: clamp(2rem, 4vw, 2.85rem);
      line-height: 1.15;
      margin: 0 0 20px;
      letter-spacing: -0.02em;
      color: var(--ink);
    }
    h1.post-title em {
      font-style: italic;
      font-weight: 500;
      color: var(--accent);
    }

    .post-meta {
      font-size: 14px;
      color: var(--muted);
      display: flex;
      align-items: center;
      gap: 14px;
      margin-bottom: 18px;
    }
    .post-meta .dot { color: var(--rule); }

    .post-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 32px;
    }
    .post-tags a {
      display: inline-block;
      background: var(--tag-bg);
      color: var(--tag-ink);
      padding: 4px 12px;
      border-radius: 4px;
      text-decoration: none;
      font-size: 12.5px;
      font-weight: 500;
      transition: all 0.2s ease;
    }
    .post-tags a:hover { background: var(--accent); color: white; }

    .post-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      padding: 18px 0;
      border-top: 1px solid var(--rule);
      border-bottom: 1px solid var(--rule);
    }
    .post-actions a {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 9px 16px;
      background: white;
      border: 1px solid var(--rule);
      border-radius: 8px;
      font-size: 14px;
      font-weight: 500;
      color: var(--ink-soft);
      text-decoration: none;
      transition: all 0.2s ease;
    }
    .post-actions a:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-1px);
      box-shadow: 0 4px 12px rgba(139, 58, 42, 0.08);
    }
    .post-actions svg { width: 14px; height: 14px; }
    .post-actions .primary {
      background: var(--accent);
      color: white;
      border-color: var(--accent);
    }
    .post-actions .primary:hover {
      background: #5e2418;
      border-color: #5e2418;
      color: white;
    }

    .authors {
      margin-top: 28px;
      font-size: 17px;
      color: var(--muted);
      line-height: 1.7;
    }
    .authors strong { color: var(--ink-soft); font-weight: 500; }
    .authors .affil { color: var(--muted); font-size: 15px; }

    h2 {
      font-family: 'Fraunces', serif;
      font-weight: 500;
      font-size: 1.7rem;
      line-height: 1.3;
      letter-spacing: -0.015em;
      margin: 64px 0 18px;
      color: var(--ink);
      display: flex;
      align-items: center;
      gap: 14px;
    }
    h2::before {
      content: "";
      display: inline-block;
      width: 12px;
      height: 12px;
      background: var(--accent);
      flex-shrink: 0;
    }
    h3 {
      font-family: 'Fraunces', serif;
      font-weight: 600;
      font-size: 1.45rem;
      margin: 36px 0 12px;
      color: var(--ink);
      letter-spacing: -0.005em;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    h3::before {
      content: "";
      display: inline-block;
      width: 10px;
      height: 10px;
      background: var(--accent);
      border-radius: 50%;
      flex-shrink: 0;
    }
    h3:has(.num)::before { display: none; }
    h3 .num {
      display: inline-block;
      width: 36px; height: 36px;
      line-height: 36px;
      text-align: center;
      background: var(--accent);
      color: white;
      border-radius: 50%;
      font-family: 'Inter', sans-serif;
      font-size: 17px;
      font-weight: 600;
      margin-right: 14px;
      vertical-align: 1px;
    }

    p { margin: 0 0 18px; color: var(--ink-soft); text-align: justify; hyphens: auto; -webkit-hyphens: auto; }
    p strong { color: var(--ink); font-weight: 600; }
    a { color: var(--accent); text-decoration-color: rgba(139, 58, 42, 0.3); text-underline-offset: 3px; transition: text-decoration-color 0.2s; }
    a:hover { text-decoration-color: var(--accent); }

    .lead {
      font-family: 'Fraunces', serif;
      font-weight: 400;
      font-size: 1.18rem;
      line-height: 1.6;
      color: var(--ink);
      letter-spacing: -0.005em;
      padding: 24px 28px;
      background: linear-gradient(135deg, var(--accent-bg) 0%, var(--bg) 100%);
      border-left: 3px solid var(--accent);
      border-radius: 0 8px 8px 0;
      margin: 8px 0 32px;
      text-align: justify;
      hyphens: auto;
      -webkit-hyphens: auto;
    }
    .lead strong { color: var(--accent); font-weight: 600; }

    .theorem {
      background: var(--surface);
      border: 1px solid var(--rule);
      border-left: 3px solid var(--accent);
      padding: 20px 24px;
      margin: 24px 0;
      border-radius: 0 8px 8px 0;
    }
    .theorem-label {
      font-family: 'Inter', sans-serif;
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--accent);
      margin-bottom: 8px;
    }
    .theorem p:last-child { margin-bottom: 0; }

    .MathJax_Display { overflow-x: auto; overflow-y: hidden; padding: 8px 0; margin: 16px 0; }

    figure {
      margin: 40px -8px;
      padding: 28px;
      background: var(--surface);
      border: 1px solid var(--rule);
      border-radius: 14px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.02);
    }
    figure img {
      display: block;
      max-width: 100%;
      height: auto;
      margin: 0 auto;
      border-radius: 4px;
    }
    figure figcaption {
      font-size: 13.5px;
      color: var(--muted);
      margin-top: 16px;
      line-height: 1.6;
      padding: 0 8px;
      text-align: left;
    }
    figure figcaption strong {
      color: var(--ink-soft);
      font-weight: 600;
      display: inline-block;
      margin-right: 4px;
    }

    .block-diagram {
      width: 100%;
      max-width: 720px;
      margin: 0 auto;
      display: block;
    }

    ul, ol { padding-left: 24px; margin: 0 0 18px; color: var(--ink-soft); }
    li { margin-bottom: 8px; text-align: justify; hyphens: auto; -webkit-hyphens: auto; }
    li::marker { color: var(--accent); }

    .feature-list { list-style: none; padding-left: 0; }
    .feature-list li {
      position: relative;
      padding-left: 32px;
      margin-bottom: 14px;
    }
    .feature-list li::before {
      content: "";
      position: absolute;
      left: 0; top: 0.55em;
      width: 18px; height: 2px;
      background: var(--accent);
    }

    pre {
      background: var(--code-bg);
      border: 1px solid var(--rule);
      border-radius: 10px;
      padding: 18px 22px;
      overflow-x: auto;
      font-family: 'JetBrains Mono', "SF Mono", Menlo, Consolas, monospace;
      font-size: 13.5px;
      line-height: 1.65;
      color: var(--code-ink);
      margin: 20px 0;
    }
    code { font-family: 'JetBrains Mono', "SF Mono", Menlo, monospace; font-size: 0.9em; }
    p code, li code {
      background: var(--code-bg);
      padding: 2px 6px;
      border-radius: 4px;
      color: var(--code-ink);
      font-size: 0.88em;
    }
    .code-comment { color: #8a7a5a; font-style: italic; }
    .code-keyword { color: #8b3a2a; font-weight: 500; }

    .ornament {
      text-align: center;
      margin: 48px 0;
      color: var(--rule);
      font-size: 18px;
      letter-spacing: 0.5em;
    }

    .results-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 16px;
      margin: 24px 0;
    }
    .result-card {
      background: var(--surface);
      border: 1px solid var(--rule);
      border-radius: 10px;
      padding: 18px 20px;
      transition: all 0.2s ease;
    }
    .result-card:hover {
      border-color: var(--accent-soft);
      transform: translateY(-2px);
      box-shadow: 0 4px 16px rgba(139, 58, 42, 0.06);
    }
    .result-card .label {
      font-size: 11.5px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      color: var(--accent);
      margin-bottom: 6px;
    }
    .result-card .value {
      font-family: 'Fraunces', serif;
      font-size: 1.05rem;
      color: var(--ink);
      line-height: 1.4;
    }

    .contact-card {
      margin-top: 56px;
      padding: 28px 32px;
      background: linear-gradient(135deg, var(--accent-bg) 0%, var(--bg) 100%);
      border: 1px solid var(--rule);
      border-radius: 12px;
    }
    .contact-card h2 { margin-top: 0; padding-left: 0; }
    .contact-card h2::before { display: none; }
    .contact-card .authors-list {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 12px;
    }
    .contact-card .authors-list a {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 6px 14px;
      background: white;
      border: 1px solid var(--rule);
      border-radius: 6px;
      text-decoration: none;
      font-size: 14px;
      color: var(--ink-soft);
      transition: all 0.2s ease;
    }
    .contact-card .authors-list a:hover {
      border-color: var(--accent);
      color: var(--accent);
    }

    footer {
      max-width: 1180px;
      margin: 64px auto 32px;
      padding: 32px 22px;
      border-top: 1px solid var(--rule);
      font-size: 13px;
      color: var(--muted);
      text-align: center;
    }

    /* Definition callout — like .theorem but in a softer slate tone */
    .definition {
      background: #f7f5f0;
      border: 1px solid var(--rule);
      border-left: 3px solid #8a7a5a;
      padding: 20px 24px;
      margin: 24px 0;
      border-radius: 0 8px 8px 0;
    }
    .definition-label {
      font-family: 'Inter', sans-serif;
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: #8a7a5a;
      margin-bottom: 8px;
    }
    .definition p:last-child { margin-bottom: 0; }

    /* Vertical proof-step flow */
    .proof-flow {
      display: flex;
      flex-direction: column;
      gap: 14px;
      margin: 24px 0 28px;
      counter-reset: stepnum;
    }
    .proof-step {
      display: grid;
      grid-template-columns: 44px 1fr;
      gap: 18px;
      align-items: start;
      padding: 18px 20px;
      background: var(--surface);
      border: 1px solid var(--rule);
      border-radius: 10px;
      transition: all 0.2s ease;
      position: relative;
    }
    .proof-step:hover {
      border-color: var(--accent-soft);
      transform: translateX(2px);
      box-shadow: 0 4px 12px rgba(139, 58, 42, 0.05);
    }
    .proof-step .step-num {
      counter-increment: stepnum;
      width: 36px; height: 36px;
      line-height: 36px;
      text-align: center;
      background: var(--accent);
      color: white;
      border-radius: 50%;
      font-family: 'Fraunces', serif;
      font-size: 16px;
      font-weight: 600;
    }
    .proof-step .step-body { font-size: 15.5px; line-height: 1.6; color: var(--ink-soft); }
    .proof-step .step-body strong { color: var(--ink); display: block; margin-bottom: 4px; font-family: 'Fraunces', serif; font-size: 1.05rem; font-weight: 600; }
    .proof-step .step-body code { background: var(--code-bg); padding: 1px 5px; border-radius: 3px; font-size: 0.82em; }
    .proof-step .lemma-tag {
      display: inline-block;
      font-size: 10.5px;
      font-weight: 600;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--accent);
      background: var(--accent-bg);
      padding: 2px 8px;
      border-radius: 3px;
      margin-left: 8px;
      vertical-align: 2px;
    }
    /* Connecting line between steps */
    .proof-step:not(:last-child)::after {
      content: "";
      position: absolute;
      left: 38px; bottom: -14px;
      width: 2px; height: 14px;
      background: var(--rule);
    }

    /* Two-column intuition / formal pair */
    .pair-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 16px;
      margin: 24px 0;
    }
    .pair-card {
      background: var(--surface);
      border: 1px solid var(--rule);
      border-radius: 10px;
      padding: 20px 22px;
    }
    .pair-card .pair-label {
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--accent);
      margin-bottom: 10px;
    }
    .pair-card.intuition { background: linear-gradient(135deg, #f5e7e0 0%, var(--bg) 100%); }
    .pair-card.formal { background: var(--surface); }
    .pair-card p:last-child { margin-bottom: 0; }
    .pair-card p { font-size: 15px; }

    /* Inline emphasis boxes — Scope, Why it matters */
    .scope-note {
      margin: 24px 0;
      padding: 18px 22px;
      background: var(--bg);
      border: 1px dashed var(--rule);
      border-radius: 8px;
      font-size: 15.5px;
    }
    .scope-note .scope-icon {
      display: inline-block;
      font-family: 'Fraunces', serif;
      font-size: 1.1rem;
      font-weight: 700;
      color: var(--accent);
      margin-right: 8px;
    }

    /* Permutation visual */
    .permvis {
      width: 100%;
      max-width: 640px;
      margin: 0 auto;
      display: block;
    }

    /* TL;DR bullet — short, scannable points */
    .tldr {
      list-style: none;
      padding: 0;
      margin: 20px 0;
    }
    .tldr li {
      position: relative;
      padding: 10px 16px 10px 36px;
      margin-bottom: 8px;
      background: var(--surface);
      border-left: 2px solid var(--accent);
      border-radius: 0 6px 6px 0;
      font-size: 15px;
      color: var(--ink-soft);
    }
    .tldr li::before {
      content: "→";
      position: absolute;
      left: 14px; top: 10px;
      color: var(--accent);
      font-weight: 700;
    }

    @media (max-width: 720px) {
      article { padding: 40px 14px 56px; }
      figure { margin: 28px -4px; padding: 18px; }
      h2 { font-size: 1.45rem; }
      .navbar-inner { padding: 0 14px; }
      .nav-links { gap: 18px; }
      .proof-step { grid-template-columns: 36px 1fr; gap: 12px; padding: 14px 16px; }
      .proof-step .step-num { width: 30px; height: 30px; line-height: 30px; font-size: 14px; }
    }
  </style>
</head>
<body>

<article>

  <div class="hero">
    <div class="venue-badge" role="img" aria-label="Accepted to ICLR 2026 as an Oral Presentation">
      <span class="venue-side">
        <span class="conf">ICLR 2026</span>
        <!-- <span class="yr">2026</span> -->
      </span>
      <span class="divider" aria-hidden="true"></span>
      <span class="oral-side">
        <span class="star" aria-hidden="true">★</span>
        Oral
      </span>
    </div>
    <h1 class="post-title">Exchangeability of GNN Representations <br>
      <span style="color: var(--accent);">with Applications to Graph Retrieval</span></h1>

    <div class="post-actions">
      <a class="primary" href="https://openreview.net/pdf?id=HQcCd0laFq">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
        Paper
      </a>
      <a href="https://rebrand.ly/graphhash">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
        Code
      </a>
      <a href="#contact">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Contact
      </a>
    </div>

    <p class="authors">
      <strong>Kartik Nair</strong> <span class="affil">(CMU)</span>,
      <strong>Indradyumna Roy</strong> <span class="affil">(IIT Bombay)</span>,
      <strong>Soumen Chakrabarti</strong> <span class="affil">(IIT Bombay)</span>,<br>
      <strong>Anirban Dasgupta</strong> <span class="affil">(IIT Gandhinagar)</span>,
      <strong>Abir De</strong> <span class="affil">(IIT Bombay)</span>
    </p>
  </div>

  <p class="lead">
    We discover a probabilistic symmetry hidden in trained graph neural networks: under standard initialization and
    training, the per-dimension components of node embeddings are <strong>exchangeable</strong> random variables.
    This single property collapses costly transportation-based graph similarity into a sorted-vector Euclidean
    similarity, giving the first unified locality-sensitive hashing framework for diverse graph retrieval tasks.
  </p>

  <h2>Motivation</h2>
  <p>
    Symmetries in neural networks have largely been studied <em>algebraically</em> — the invariance of an MLP's output
    under simultaneous permutations of its weight matrices, for instance. These symmetries are typically treated in
    isolation from the training process. We ask a different question: are there <em>probabilistic</em> symmetries
    that emerge naturally during the standard training of a GNN, induced by random initialization itself?
  </p>
  <p>
    The answer turns out to be yes — and the structure it exposes has direct, far-reaching consequences for scalable
    graph retrieval. Across a wide variety of message-passing architectures (GCN, GAT, GIN, gated GNN, graph transformers)
    and standard optimizers (SGD, Adam), the columns of the learned embedding matrix are exchangeable, where the randomness
    is induced by the model initialization.
  </p>

  <h2>Problem Setup</h2>
  <p>
    Given a graph $G = (V, E)$ with $|V| = n$, a graph neural network with parameters $\theta$ computes a node embedding
    matrix $X = [\mathbf{x}(u)]_{u \in [n]} \in \mathbb{R}^{n \times D}$, where $D$ is the embedding dimension. Parameters
    are initialized i.i.d. (e.g., Kaiming or Xavier) and trained by a gradient-based optimizer on a permutation-invariant loss.
  </p>
  <p>
    For graph retrieval, given a query graph $G_q$ and a corpus $\mathcal{C} = \{G_c\}$, we seek the top-$b$ corpus graphs
    most relevant to $G_q$. State-of-the-art relevance is captured by a unified transportation-based distance, decomposable
    across embedding dimensions:
  </p>
  \[
    \Delta(G_c, G_q) = \min_{P \in \mathcal{P}_n} \sum_{u, u'} \sum_{d \in [D]} \rho\!\left(\mathbf{x}^{(q)}(u)[d] - \mathbf{x}^{(c)}(u')[d]\right) \cdot P[u, u'],
  \]
  <p>
    where $\rho$ is convex and possibly asymmetric. Setting $\rho(\cdot) = [\cdot]_+$ recovers the hinge distance for
    subgraph isomorphism; $\rho(\cdot) = e_\ominus[\cdot]_+ + e_\oplus[-\cdot]_+$ recovers asymmetric graph edit distance.
    The catch: computing $\Delta$ exactly is $\mathcal{O}(n^3)$ and Sinkhorn approximations are $\mathcal{O}(n^2)$ —
    neither fits any standard index.
  </p>

  <!-- <div class="ornament">· · ·</div> -->

  <h2>Exchangeability of GNN Representations</h2>

  <p>
    Before we use it, let us take a careful look at <em>what</em> exchangeability of GNN embeddings actually says, <em>why</em>
    it holds, and <em>how far</em> it travels. The story has three parts: a precise definition, a four-step argument that turns
    a property of i.i.d. initialization into a property of trained models, and a discussion of how restrictive the assumptions
    really are.
  </p>

  <h3>What exchangeability says</h3>

  <div class="definition">
    <div class="definition-label">Definition · Exchangeability (Aldous, 1985)</div>
    <p>
      Random vectors $Y_1, \dots, Y_D \in \mathbb{R}^n$ are <em>exchangeable</em> if for every permutation
      $\pi : [D] \to [D]$, the joint density satisfies
      $p_{Y_1, \dots, Y_D}(y_1, \dots, y_D) = p_{Y_{\pi(1)}, \dots, Y_{\pi(D)}}(y_1, \dots, y_D).$
      Reordering the indices does not change the joint distribution.
    </p>
  </div>

  <p>
    For a trained GNN, the random vectors of interest are the <em>columns</em> of the embedding matrix $X = \text{GNN}_\theta(G) \in \mathbb{R}^{n \times D}$ —
    i.e., one $\mathbb{R}^n$ vector per embedding dimension. The randomness is induced by the random initialization of the
    parameters $\theta$. The claim is that these $D$ columns are exchangeable: shuffling them around does not change the
    joint distribution we get when we average over training runs with different seeds.
  </p>

  <p>
    Two things are worth pulling apart, because they are easy to conflate:
  </p>

  <div class="pair-grid">
    <div class="pair-card intuition">
      <div class="pair-label">The intuition</div>
      <p>
        At initialization, all $D$ embedding dimensions are drawn from the same distribution. Training does not "break" this
        symmetry, because the loss does not care which dimension is which. So the dimensions remain interchangeable
        throughout training.
      </p>
    </div>
    <div class="pair-card formal">
      <div class="pair-label">The formal claim</div>
      <p>
        $p(X) = p(X\pi)$ for every permutation matrix $\pi \in \mathcal{P}_D$. The randomness is over initializations,
        not over data. Two embedding dimensions are not the same vector — but their joint distribution is invariant
        under reordering.
      </p>
    </div>
  </div>

  <p>
    Two notes on what this is <strong>not</strong>. First, exchangeability does <em>not</em> say that two dimensions of
    the same trained model are equal. They are typically different vectors. It says that if you train many independent
    GNNs and look at the empirical density across runs, you get the same density for every dimension — and the same
    joint density for every reordering. Second, exchangeability is a <em>probabilistic</em> symmetry, distinct from
    the algebraic permutation symmetries of weight matrices that have been studied since Hecht-Nielsen (1990). Algebraic
    symmetry is about a single trained model; probabilistic symmetry is about the distribution of trained models.
  </p>

 

  <h3>Why it holds — a four-step argument</h3>

  <p>
    The core observation is simple, but turning it into a proof for arbitrary GNN architectures takes care. The argument
    in Section 3 of the paper has four steps. The first three are technical lemmas; the fourth is the main theorem.
  </p>

  <p><strong>Warm-up: a 2-layer MLP.</strong> Consider the map $\mathbf{x} = \sigma(\sigma(\text{feat}\cdot\Psi)\Theta)$.
    To reorder the columns of $\mathbf{x}$ by a permutation $\pi$, simply right-multiply $\Theta$ by $\pi$:
    $\Theta \mapsto \Theta\pi$ produces $\mathbf{x} \mapsto \mathbf{x}\pi$. The map
    $\Gamma_\pi(\theta) := \theta \cdot \mathrm{Diag}(I, \pi)$ is the parameter-side bijection that induces this
    output permutation. Because $\Theta$ is initialized i.i.d., $p(\Theta) = p(\Theta\pi)$, so
    $p(\mathbf{x}) = p(\mathbf{x}\pi)$ at $t = 0$. The whole argument extends this single observation through the
    full training trajectory of a GNN.
  </p>

  <div class="proof-flow">
    <div class="proof-step">
      <div class="step-num">1</div>
      <div class="step-body">
        <strong>Permutation-induced parameter transformation <span class="lemma-tag">Lemma 2</span></strong>
        For any permutation $\pi$ on the embedding dimension axis, there exists a bijection $\Gamma_\pi$ on
        the GNN parameters $\theta$ such that $X\pi=$ GNN$_{\Gamma _{\pi} (\theta)}(G)$, with
        $|\det(\partial \Gamma_\pi(\theta) / \partial \theta)| = 1$. Constructing $\Gamma_\pi$ for a GNN is harder than for an MLP,
        because permutations propagate through neighborhood aggregation across layers. The lemma certifies it can be done for
        the architectures of interest (GCN, GAT, GIN, gated GNN, graph transformers).
      </div>
    </div>
    <div class="proof-step">
      <div class="step-num">2</div>
      <div class="step-body">
        <strong>Gradient equivariance <span class="lemma-tag">Lemma 3</span></strong>
        Because the loss is invariant under permutations of the embedding dimensions, it is invariant under $\Gamma_\pi$
        on the parameters: $\text{loss}(\Gamma_\pi(\theta)) = \text{loss}(\theta)$. Differentiating gives the gradient
        equivariance $\nabla_\theta \text{loss}\big|_{\Gamma_\pi(\theta)} = \Gamma_\pi\!\left(\nabla_\theta \text{loss}\big|_{\theta}\right)$.
        In words: shuffle the parameters, and the gradient shuffles in lockstep.
      </div>
    </div>
    <div class="proof-step">
      <div class="step-num">3</div>
      <div class="step-body">
        <strong>Invariance of parameter density during training <span class="lemma-tag">Lemma 4</span></strong>
        Combining initialization symmetry $p(\theta_0) = p(\Gamma_\pi(\theta_0))$ with gradient equivariance,
        the entire training trajectory is permutation-equivariant: if $\theta_0 \mapsto \Gamma_\pi(\theta_0)$, then
        $\theta_t \mapsto \Gamma_\pi(\theta_t)$ for all $t \geq 0$. The Jacobian-1 condition from Lemma 2 lets us
        push the symmetry through to densities: $p(\theta_t) = p(\Gamma_\pi(\theta_t))$ for every epoch.
      </div>
    </div>
    <div class="proof-step">
      <div class="step-num">4</div>
      <div class="step-body">
        <strong>Exchangeability of embeddings <span class="lemma-tag">Theorem 5</span></strong>
        Apply the GNN to the trained $\theta_t$. Since $X\pi = \text{GNN}_{\Gamma_\pi(\theta_t)}(G)$ and
        $\theta_t \stackrel{d}{=} \Gamma_\pi(\theta_t)$, we conclude $X \stackrel{d}{=} X\pi$, i.e. $p(X) = p(X\pi)$.
        Proposition 6 extends this to query–corpus pairs $Y = [X^{(q)}; X^{(c)}]$ when the loss is invariant under
        simultaneous permutation of both.
      </div>
    </div>
  </div>

  <p>
    The structure of the argument is general: any time you have (i) i.i.d. initialization, (ii) a loss invariant under
    a group action on intermediate representations, and (iii) a gradient-based optimizer, you get exchangeability
    of those representations under that group. GNNs are an instance of this template; CNNs and MLPs are others
    (independently noted in contemporaneous work).
  </p>

  <h3>Three consequences worth pausing on</h3>

  <p>
    The theorem is stated as a distributional statement, but it has concrete fingerprints that are useful both as
    sanity checks and as engineering tools. Each consequence below corresponds to a specific empirical test that
    the paper performs on the cox2 dataset, training 5,000 independent GNNs and looking at what the symmetry
    actually does in practice.
  </p>

  <h4 style="font-family:'Fraunces',serif;font-weight:600;font-size:1.05rem;margin:32px 0 10px;color:var(--ink);">Consequence 1 — Identical marginals across embedding dimensions</h4>

  <p>
    The most direct fingerprint: each component $\mathbf{x}(u)[d]$ should have the same marginal density across
    $d \in [D]$. To test this, the authors fix a corpus node $v$ in cox2, train 5,000 GNNs from scratch with
    different random seeds, and for each model record the scalar value $X^{(c)}[v, d]$ for $d \in \{1, 5, 10\}$.
    The histogram across seeds is the empirical density for that dimension. If exchangeability holds, these
    three histograms should overlap.
  </p>

  <figure>
    <img src="assets/fig1_density.png" alt="Empirical probability densities of embedding dimensions across training">
    <figcaption>
      <strong>Figure 2 (paper Fig. 1).</strong> Empirical probability density of $X^{(c)}[v, d]$ for the highlighted
      node $v$ in the example corpus graph $G_c$ in cox2, computed over 5,000 independently trained GNNs. Panels
      (b)–(d) show the density at three points in training: initialization, epoch 8, epoch 20. Across all three
      stages of training, the densities for $d = 1, 5, 10$ are visually indistinguishable — exchangeability is preserved
      throughout training, not just at initialization.
    </figcaption>
  </figure>

  <h4 style="font-family:'Fraunces',serif;font-weight:600;font-size:1.05rem;margin:32px 0 10px;color:var(--ink);">Consequence 2 — A direct distributional test via MMD</h4>

  <p>
    Identical marginals are necessary but not sufficient for exchangeability — two different joint distributions
    can share marginals. The authors therefore run a stronger test: estimate the maximum mean discrepancy (MMD$^2$)
    between the empirical distribution of $X$ and that of $X\pi$ across 100 random permutations $\pi$. If the two
    distributions agree, MMD$^2$ should be near zero (and is allowed to go slightly negative, since the unbiased
    estimator can underestimate).
  </p>

  <figure style="padding:32px 28px;">
    <img src="assets/table2_mmd.png" alt="Unbiased MMD-squared estimator between p_X and p_{X pi}" style="max-width:560px;">
    <figcaption>
      <strong>Table 2 (from the paper).</strong> Unbiased MMD$^2$ estimator between $p_X$ and $p_{X\pi}$ for the
      cox2 dataset, averaged over 100 random permutations. Both supervisions (GED and SM) yield estimates on the
      order of $10^{-5}$ or $10^{-6}$ — strong empirical support that $p_X$ and $p_{X\pi}$ coincide.
    </figcaption>
  </figure>

  <h4 style="font-family:'Fraunces',serif;font-weight:600;font-size:1.05rem;margin:32px 0 10px;color:var(--ink);">Consequence 3 — The expected embedding matrix is rank one</h4>

  <p>
    A more surprising fingerprint follows from identical marginals plus exchangeability of joint columns:
    $\mathbb{E}[X]$ has all columns equal, so it is a <em>rank-one</em> matrix. To test this, compute the SVD
    of the empirical sample mean $\frac{1}{R}\sum_{r=1}^R X^{(r)}$ over $R$ independently trained models, and
    track the ratio $\sigma_1^2 / \sum_i \sigma_i^2$ — the fraction of total variance captured by the leading
    singular value. If $\mathbb{E}[X]$ truly is rank one, this ratio should converge to 1 as $R$ grows.
  </p>

  <figure style="padding:32px 28px;">
    <img src="assets/fig3_rank1.png" alt="Relative size of top singular value of mean embedding matrix" style="max-width:780px;">
    <figcaption>
      <strong>Figure 3 (from the paper).</strong> Relative size $\sigma_1^2 / \sum_i \sigma_i^2$ of the top singular
      value of the mean (trained) embedding matrix as a function of the number of independent initializations $R$,
      on cox2 under (a) Subgraph Matching and (b) GED supervision. As $R$ grows, the ratio approaches 1 from below,
      confirming that $\mathbb{E}[X]$ has rank 1. This is independently consistent with rank-collapse findings in
      transformers (Dong et al., 2023) and state-space models (Joseph et al., 2025).
    </figcaption>
  </figure>

  <h4 style="font-family:'Fraunces',serif;font-weight:600;font-size:1.05rem;margin:32px 0 10px;color:var(--ink);">Consequence 4 — Per-dimension scoring is unbiased (the engineering hook)</h4>

  <p>
    The last consequence is what powers the GraphHash pipeline. Because dimensions are identically distributed,
    the score $\text{sim}_d(G_c, G_q)$ computed in any single dimension $d$ is an unbiased estimate (up to scaling)
    of the full $D$-dimensional transportation score. Aggregating per-dimension estimates therefore approximates
    the full cost. This is the formal hook that lets the next section replace optimal transport with sorting —
    a sublinear-time operation that fits cleanly into a locality-sensitive hash.
  </p>

  <!-- <h3>How restrictive are the assumptions?</h3>

  <p>
    The setting in Section 3.1 of the paper lists four conditions: (a) the GNN comes from a broad class of message-passing
    architectures, (b) parameters are initialized i.i.d. within each layer, (c) the loss is invariant to permutations
    of the embedding dimensions, and (d) the optimizer is gradient-based. It is fair to ask which of these is doing
    real work and which is for technical convenience.
  </p>

  <div class="scope-note">
    <span class="scope-icon">§</span>
    <strong>Initialization.</strong> Standard Kaiming and Xavier schemes both satisfy (b). Block-diagonal or
    structured-sparse initializations would violate the i.i.d. requirement and are out of scope.
  </div>
  <div class="scope-note">
    <span class="scope-icon">§</span>
    <strong>Loss permutation invariance.</strong> Many natural losses satisfy (c) for free. Pairwise ranking and
    binary cross-entropy losses computed from <em>transportation similarity</em> between embedding sets are invariant,
    because the transport plan does not care about dimension order. Dot-product link prediction
    $\mathbf{x}(u)^\top \mathbf{x}(v)$ is similarly invariant. Even when the loss is <em>not</em> invariant
    on its own, exchangeability can still hold under joint transformations of intermediate representations and
    subsequent-layer parameters (Appendix E.1.6 of the paper).
  </div>
  <div class="scope-note">
    <span class="scope-icon">§</span>
    <strong>Architecture.</strong> The proof covers GCN, GAT, GIN, gated GNN, and graph transformers. Normalization
    layers (LayerNorm, BatchNorm) introduce no obstructions because they too act dimension-wise and equivariantly.
    The construction of $\Gamma_\pi$ is the architecture-dependent step; for any new architecture, this is the
    technical step to verify.
  </div>
  <div class="scope-note">
    <span class="scope-icon">§</span>
    <strong>Optimizer.</strong> SGD and Adam are explicitly covered. The argument needs only that the update rule
    is permutation-equivariant; momentum and adaptive-rate schemes maintain this because they apply the same
    elementwise rule to every parameter coordinate.
  </div>

  <p>
    The takeaway: the conditions sound technical but capture the standard training pipeline almost exactly. If you
    are training a GNN on graph retrieval with PyTorch defaults, exchangeability holds.
  </p> -->

  <div class="ornament">· · ·</div>

  <h2>The GraphHash Pipeline</h2>
  <p>
    Our framework <strong>GraphHash</strong> turns the intractable transportation problem into a sequence of indexable
    operations, end to end:
  </p>

  <figure>
      <img src="pipeline.svg" alt="GraphHash indexing and query algorithms">
    <!-- <figcaption>
      <strong>Figure 1: GraphHash pipeline.</strong> Exchangeability of embedding dimensions (highlighted block) is the
      pivot that makes the rest of the pipeline work — it justifies replacing high-dimensional optimal transport with
      one-dimensional sorted-vector similarity, which a standard random-Fourier-feature LSH can index in sublinear time.
    </figcaption> -->
  </figure>

  <h2>Core Components</h2>

  <h3><span class="num">1</span>Exchangeability of GNN Embeddings</h3>
  <p>
    A sequence of random vectors $Y_1, \dots, Y_D \in \mathbb{R}^n$ is <em>exchangeable</em> if its joint density is invariant
    under any permutation of indices: $p(Y_1, \dots, Y_D) = p(Y_{\pi(1)}, \dots, Y_{\pi(D)})$ for all $\pi$. Our main result
    establishes exchangeability for the columns of the embedding matrix.
  </p>
  <div class="theorem">
    <div class="theorem-label">Theorem · Exchangeability of embedding elements</div>
    <p>Under (i) i.i.d. initialization within each layer, (ii) a permutation-invariant loss, and (iii) a gradient-based
       optimizer (SGD, Adam, ...),</p>
    \[ p(X) = p(X \pi) \quad \text{for all permutation matrices } \pi, \]
    <p>where the randomness is induced by the random initialization. The result extends to joint distributions over
       query–corpus pairs: with $Y = [X^{(q)}; X^{(c)}]$, $p(Y) = p(Y \pi)$.</p>
  </div>
  <p>
    A direct consequence: the components $\mathbf{x}(u)[1], \dots, \mathbf{x}(u)[D]$ are <em>identically distributed</em>.
    Across many random seeds, the expected embedding matrix $\mathbb{E}\big[[\mathbf{x}(u)]_{u \in V}\big]$ collapses to
    a rank-one matrix — an observation aligned with recent rank-collapse findings in transformers and SSMs.
  </p>

  <h3><span class="num">2</span>Transport → Sorted-Vector Euclidean Similarity</h3>
  <p>
    Exchangeability implies the $D$ embedding coordinates are identically distributed, so each dimension yields a
    concentrated estimate of the full transportation similarity. Aggregating per-dimension estimates approximates the
    full $D$-dimensional cost. For a single dimension $d$, the transportation problem reduces to optimal transport
    between scalars — solved <em>exactly</em> by sorting:
  </p>
  \[
    \mathrm{sim}_d(G_c, G_q) = s\!\left( \mathrm{SORT}(X^{(q)}[:, d]) \;-\; \mathrm{SORT}(X^{(c)}[:, d]) \right),
  \]
  <p>
    where $s(\cdot) = \rho_{\max} - \rho(\cdot)$ is the corresponding score. A problem with no good index becomes
    a Euclidean similarity over fixed-length sorted vectors.
  </p>

  <h3><span class="num">3</span>GraphHash: a unified LSH framework</h3>
  <p>
    Once the score is Euclidean on sorted-embedding columns, classical LSH applies. Building on the Fourier-feature
    LSH construction of Roy et al. (2023), we embed order-statistics vectors via random Fourier features and bucket
    by sign:
  </p>

<pre><code><span class="code-comment">// GraphHash: indexing a corpus graph G_c</span>
X = GNN_<span class="code-keyword">θ</span>(G_c)
<span class="code-keyword">for</span> d <span class="code-keyword">in</span> range(D):
    v_d   = SORT(X[:, d])              <span class="code-comment">// per-dim order statistics</span>
    φ_d   = fourier_features(v_d, ω)   <span class="code-comment">// random Fourier projection</span>
    h_d   = sign(φ_d @ R)              <span class="code-comment">// sign hash</span>
bucket(G_c) = concat(h_1, ..., h_D)</code></pre>

  <p>
    We prove this is a valid LSH for the original transportation-based graph similarity, working uniformly across
    hinge similarity (subgraph matching), asymmetric GED, and other decomposable transportation distances. To our
    knowledge this is the first principled LSH for asymmetric transportation-based graph similarity.
  </p>

  <figure>
    <img src="assets/algos.png" alt="GraphHash indexing and query algorithms">
    <figcaption>
      <strong>Figure 3 (from the paper).</strong> Algorithm 1 (left) precomputes hash codes for each corpus graph
      and stores them in buckets. Algorithm 2 (right) hashes the query graph the same way and returns the top-$b$
      graphs from the matching buckets — query time is sublinear in $|\mathcal{C}|$.
    </figcaption>
  </figure>

  <div class="ornament">· · ·</div>

  <h2>Experimental Findings</h2>

  <p>
    The experimental section evaluates GraphHash on four real-world TU benchmark datasets, against five competitive
    indexing baselines, under two distinct supervision signals, and on two complementary retrieval metrics. The setup
    is summarised below; full details are in Section 5 of the paper.
  </p>

  <div class="results-grid">
    <div class="result-card">
      <div class="label">Datasets</div>
      <div class="value">PTC-FR, PTC-FM, COX2, PTC-MR — 100K corpus graphs, 500 query graphs each</div>
    </div>
    <div class="result-card">
      <div class="label">Supervision</div>
      <div class="value">Subgraph matching (VF2) and asymmetric GED ($e_\oplus = 1$, $e_\ominus = 2$)</div>
    </div>
    <div class="result-card">
      <div class="label">Baselines</div>
      <div class="value">FourierHashNet, IVF, DiskANN, Random Hyperplane, Random</div>
    </div>
    <div class="result-card">
      <div class="label">Metrics</div>
      <div class="value">MAP and NDCG vs. retrieval budget</div>
    </div>
  </div>

  <figure>
    <img src="assets/table6_sm_stats.png" alt="Dataset statistics for Subgraph Matching">
    <figcaption>
      <strong>Table 1 (paper Table 6).</strong> Per-dataset statistics under Subgraph Matching supervision: query
      and corpus graph sizes (min / max / avg) and label ratio (fraction of relevant corpus graphs per query).
      Label ratios are between 12% and 13% across the four datasets, so retrieval is non-trivial — random sampling
      would recover relevant graphs only at that base rate. Statistics for the GED setting are similar.
    </figcaption>
  </figure>

  <h3>MAP vs. retrieval budget</h3>

  <figure>
    <img src="assets/fig4_map.png" alt="MAP vs. number of retrieved graphs across all four datasets">
    <figcaption>
      <strong>Figure 4 (from the paper).</strong> Trade-off between mean average precision (MAP) and number of
      retrieved graphs across all four TU-benchmark datasets. Top row: subgraph matching (SM); bottom row: GED.
      The horizontal red line denotes 50% of exhaustive MAP. <strong>GraphHash</strong> (red) consistently dominates
      all baselines across the accuracy-efficiency Pareto front, in many cases reaching the 50% line at one-third
      the candidate budget needed by the next-best method.
    </figcaption>
  </figure>

  <h3>Robustness across metrics and hyperparameters</h3>

  <p>
    A single MAP curve can hide failure modes — a method might lift average precision while ranking the very best
    candidates poorly. To check for that, the paper repeats the comparison under NDCG, a position-sensitive metric,
    and adds a third supervision signal (equal-cost GED, where insertion and deletion costs are both 1).
  </p>

  <figure>
    <img src="assets/fig11_ndcg.png" alt="NDCG vs retrieved graphs across all datasets and supervisions">
    <figcaption>
      <strong>Figure 5 (paper Fig. 11, Appendix H.2).</strong> Trade-off between NDCG@1000 and number of retrieved
      graphs across all four datasets. Top row: subgraph matching; middle row: asymmetric GED ($e_\oplus = 1$,
      $e_\ominus = 2$); bottom row: equal-cost GED ($e_\oplus = e_\ominus = 1$). Every grid cell tells the same
      story as the MAP analysis — GraphHash dominates the curve, and the same hashing scheme transfers across
      supervision regimes without retuning.
    </figcaption>
  </figure>

  <p>
    A second axis: the hashcode dimension $\dim_h$ controls the bit-budget of the LSH. Too few bits collapse
    everything into a single bucket; too many fragment the corpus and inflate the candidate set. The paper sweeps
    $\dim_h$ and tracks the area under the MAP-vs-budget curve (AUC) — a single scalar summarising the whole
    accuracy–efficiency trade-off.
  </p>

 

 

  <div class="contact-card" id="contact">
    <h2>Contact</h2>
    <p>If you have questions or suggestions, please reach out to any of the authors.</p>
    <div class="authors-list">
      <a href="mailto:ksnair@cs.cmu.edu">✉ Kartik Nair</a>
      <a href="mailto:indraroy15@cse.iitb.ac.in">✉ Indradyumna Roy</a>
      <a href="mailto:soumen@cse.iitb.ac.in">✉ Soumen Chakrabarti</a>
      <a href="mailto:anirbandg@iitgn.ac.in">✉ Anirban Dasgupta</a>
      <a href="mailto:abir@cse.iitb.ac.in">✉ Abir De</a>
    </div>
  </div>

</article>

<footer>
  <p>©KN/IR/ADG/SC/AD. Built with help of Claude. <a href="https://openreview.net/pdf?id=HQcCd0laFq" style="color: var(--muted);">read the paper</a></p>
</footer>

</body>
</html>
