<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Join Shing Noor Creative Design</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --blue: #38BDF8;
    --blue-dark: #0EA5E9;
    --pink: #E040FB;
    --pink-dark: #C026D3;
    --navy: #0A0C14;
    --navy-mid: #0F1220;
    --navy-card: #131726;
    --navy-border: rgba(56,189,248,0.12);
    --text: #E8F4FF;
    --text-muted: rgba(232,244,255,0.5);
    --text-dim: rgba(232,244,255,0.22);
  }

  body {
    background: var(--navy);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
    position: relative;
  }

  .bg-orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(110px);
    pointer-events: none;
    z-index: 0;
  }
  .bg-orb-1 { width: 700px; height: 700px; background: rgba(56,189,248,0.065); top: -250px; left: -200px; }
  .bg-orb-2 { width: 600px; height: 600px; background: rgba(224,64,251,0.065); bottom: -150px; right: -150px; }
  .bg-grid {
    position: fixed; inset: 0;
    background-image:
      linear-gradient(rgba(56,189,248,0.025) 1px, transparent 1px),
      linear-gradient(90deg, rgba(56,189,248,0.025) 1px, transparent 1px);
    background-size: 60px 60px;
    z-index: 0; pointer-events: none;
  }

  .wrapper {
    position: relative; z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 0 28px 80px;
  }

  /* TOP BAR */
  .topbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 28px 0 0;
    margin-bottom: 64px;
    animation: fadeDown 0.6s ease both;
  }
  .topbar-logo { display: flex; align-items: center; gap: 12px; }
  .logo-img {
    width: 48px; height: 48px;
    object-fit: contain; border-radius: 8px;
  }
  .logo-wordmark {
    font-family: 'Rajdhani', sans-serif;
    font-size: 20px; font-weight: 700; letter-spacing: 0.05em;
    line-height: 1;
  }
  .logo-wordmark .b { color: var(--blue); }
  .logo-wordmark .p { color: var(--pink); }
  .logo-sub {
    font-size: 9px; font-weight: 500;
    letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--text-dim); margin-top: 3px;
  }
  .topbar-badge {
    font-size: 10px; font-weight: 600;
    letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--blue);
    border: 1px solid rgba(56,189,248,0.3);
    padding: 7px 16px; border-radius: 2px;
    background: rgba(56,189,248,0.05);
  }

  /* HERO */
  .hero { margin-bottom: 60px; animation: fadeUp 0.8s ease 0.1s both; }
  .hero-eyebrow {
    display: flex; align-items: center; gap: 10px; margin-bottom: 22px;
  }
  .eyebrow-dot {
    width: 6px; height: 6px;
    background: var(--pink); border-radius: 50%;
    box-shadow: 0 0 10px var(--pink);
    animation: blink 2s ease infinite;
  }
  @keyframes blink {
    0%,100% { opacity:1; } 50% { opacity: 0.35; }
  }
  .eyebrow-text {
    font-size: 11px; font-weight: 600;
    letter-spacing: 0.22em; text-transform: uppercase;
    color: var(--text-muted);
  }
  .hero-h1 {
    font-family: 'Rajdhani', sans-serif;
    font-size: clamp(46px, 8vw, 78px);
    font-weight: 700; line-height: 1;
    letter-spacing: -0.01em; margin-bottom: 22px;
  }
  .hero-h1 .line1 { color: var(--text); display: block; }
  .hero-h1 .line2 {
    display: block;
    background: linear-gradient(90deg, var(--blue) 30%, var(--pink) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .hero-sub {
    font-size: clamp(14px, 1.9vw, 17px);
    font-weight: 300; line-height: 1.75;
    color: var(--text-muted); max-width: 520px;
  }

  /* DIVIDER */
  .hr {
    display: flex; align-items: center; gap: 0;
    margin: 48px 0; animation: fadeUp 0.7s ease 0.2s both;
  }
  .hr-l { height: 1px; flex: 1; background: linear-gradient(to right, transparent, var(--blue)); }
  .hr-diamond {
    width: 30px; height: 30px;
    border: 1px solid rgba(56,189,248,0.25);
    background: var(--navy-card);
    display: flex; align-items: center; justify-content: center;
    transform: rotate(45deg); flex-shrink: 0;
  }
  .hr-dot { width: 8px; height: 8px; background: linear-gradient(135deg, var(--blue), var(--pink)); }
  .hr-r { height: 1px; flex: 1; background: linear-gradient(to left, transparent, var(--pink)); }

  /* INTRO */
  .intro { margin-bottom: 48px; animation: fadeUp 0.8s ease 0.3s both; }
  .intro p {
    font-size: 15.5px; line-height: 1.82;
    color: rgba(232,244,255,0.68); margin-bottom: 18px;
  }
  .intro p:last-child { margin-bottom: 0; }
  .intro strong { color: var(--blue); font-weight: 600; }
  .intro em { color: var(--pink); font-style: normal; font-weight: 500; }

  /* SECTION LABEL */
  .sec-label {
    font-size: 10px; font-weight: 600;
    letter-spacing: 0.25em; text-transform: uppercase;
    margin-bottom: 18px;
    display: flex; align-items: center; gap: 12px;
  }
  .sec-label.blue { color: var(--blue); }
  .sec-label.blue::after {
    content: ''; height: 1px; flex: 1;
    background: linear-gradient(to right, rgba(56,189,248,0.35), transparent);
  }
  .sec-label.pink { color: var(--pink); }
  .sec-label.pink::after {
    content: ''; height: 1px; flex: 1;
    background: linear-gradient(to right, rgba(224,64,251,0.35), transparent);
  }

  /* PERKS */
  .perks {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 10px; margin-bottom: 52px;
    animation: fadeUp 0.8s ease 0.4s both;
  }
  .perk {
    background: var(--navy-card);
    border: 1px solid var(--navy-border);
    border-radius: 4px; padding: 24px 20px;
    position: relative; overflow: hidden;
    transition: border-color 0.3s, transform 0.2s, box-shadow 0.3s;
  }
  .perk::after {
    content: '';
    position: absolute; top: 0; left: 0;
    width: 3px; height: 100%;
    background: linear-gradient(to bottom, var(--blue), var(--pink));
    opacity: 0; transition: opacity 0.3s;
  }
  .perk:hover { border-color: rgba(56,189,248,0.28); transform: translateY(-3px); box-shadow: 0 10px 28px rgba(56,189,248,0.07); }
  .perk:hover::after { opacity: 1; }
  .perk-icon { font-size: 20px; margin-bottom: 12px; display: block; }
  .perk-title {
    font-family: 'Rajdhani', sans-serif;
    font-size: 14px; font-weight: 700;
    letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--text); margin-bottom: 7px;
  }
  .perk-desc {
    font-size: 13px; line-height: 1.6;
    color: var(--text-muted); font-weight: 300;
  }

  /* TAGS */
  .tags {
    display: flex; flex-wrap: wrap; gap: 9px;
    margin-bottom: 56px;
    animation: fadeUp 0.8s ease 0.5s both;
  }
  .tag {
    font-size: 12px; font-weight: 500;
    letter-spacing: 0.07em;
    padding: 7px 16px; border-radius: 2px;
    border: 1px solid rgba(224,64,251,0.18);
    color: rgba(232,244,255,0.6);
    background: rgba(224,64,251,0.04);
    cursor: default; transition: all 0.2s;
  }
  .tag:hover {
    border-color: var(--pink); color: var(--text);
    background: rgba(224,64,251,0.1);
    box-shadow: 0 0 14px rgba(224,64,251,0.14);
  }

  /* CTA */
  .cta-block {
    background: var(--navy-card);
    border: 1px solid rgba(56,189,248,0.14);
    border-radius: 6px; padding: 52px 44px;
    text-align: center; position: relative; overflow: hidden;
    animation: fadeUp 0.8s ease 0.6s both;
  }
  .cta-block::before {
    content: ''; position: absolute; inset: 0; pointer-events: none;
    background:
      radial-gradient(ellipse at 50% 0%, rgba(56,189,248,0.08) 0%, transparent 60%),
      radial-gradient(ellipse at 50% 100%, rgba(224,64,251,0.07) 0%, transparent 60%);
  }
  .cta-bar {
    width: 56px; height: 3px;
    background: linear-gradient(90deg, var(--blue), var(--pink));
    margin: 0 auto 26px; border-radius: 2px;
    position: relative;
  }
  .cta-h2 {
    font-family: 'Rajdhani', sans-serif;
    font-size: clamp(22px, 4vw, 34px);
    font-weight: 700; letter-spacing: 0.02em;
    color: var(--text); margin-bottom: 10px;
    position: relative;
  }
  .cta-sub {
    font-size: 14px; font-weight: 300;
    color: var(--text-muted); margin-bottom: 34px;
    letter-spacing: 0.03em; position: relative;
  }
  .cta-btn {
    display: inline-flex; align-items: center; gap: 10px;
    text-decoration: none;
    background: linear-gradient(135deg, var(--blue-dark) 0%, var(--pink-dark) 100%);
    color: #fff;
    font-family: 'Rajdhani', sans-serif;
    font-size: 15px; font-weight: 700;
    letter-spacing: 0.15em; text-transform: uppercase;
    padding: 16px 42px; border-radius: 3px;
    position: relative; overflow: hidden;
    transition: transform 0.2s, box-shadow 0.3s;
    box-shadow: 0 6px 28px rgba(56,189,248,0.22), 0 6px 28px rgba(224,64,251,0.18);
  }
  .cta-btn::before {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(135deg, var(--blue), var(--pink));
    opacity: 0; transition: opacity 0.3s;
  }
  .cta-btn:hover { transform: translateY(-3px); box-shadow: 0 14px 44px rgba(56,189,248,0.3), 0 14px 44px rgba(224,64,251,0.25); }
  .cta-btn:hover::before { opacity: 1; }
  .cta-btn-text { position: relative; z-index: 1; }
  .cta-arrow { position: relative; z-index: 1; font-size: 18px; transition: transform 0.2s; }
  .cta-btn:hover .cta-arrow { transform: translateX(5px); }
  .cta-note {
    margin-top: 18px; font-size: 11px;
    color: var(--text-dim); letter-spacing: 0.1em;
    position: relative;
  }

  /* FOOTER */
  .footer {
    margin-top: 52px;
    display: flex; align-items: center; justify-content: center; gap: 14px;
    animation: fadeUp 0.7s ease 0.7s both;
  }
  .footer-line { height: 1px; width: 40px; background: rgba(56,189,248,0.12); }
  .footer-text {
    font-size: 10px; letter-spacing: 0.2em;
    text-transform: uppercase; color: var(--text-dim);
  }

  /* CORNERS */
  .corner { position: fixed; width: 18px; height: 18px; opacity: 0.28; z-index: 2; pointer-events: none; }
  .c-tl { top: 18px; left: 18px; border-top: 1px solid var(--blue); border-left: 1px solid var(--blue); }
  .c-tr { top: 18px; right: 18px; border-top: 1px solid var(--pink); border-right: 1px solid var(--pink); }
  .c-bl { bottom: 18px; left: 18px; border-bottom: 1px solid var(--blue); border-left: 1px solid var(--blue); }
  .c-br { bottom: 18px; right: 18px; border-bottom: 1px solid var(--pink); border-right: 1px solid var(--pink); }

  @keyframes fadeUp { from { opacity:0; transform:translateY(22px); } to { opacity:1; transform:translateY(0); } }
  @keyframes fadeDown { from { opacity:0; transform:translateY(-14px); } to { opacity:1; transform:translateY(0); } }

  @media (max-width: 540px) {
    .perks { grid-template-columns: 1fr; }
    .topbar-badge { display: none; }
    .corner { display: none; }
    .cta-block { padding: 36px 22px; }
    .wrapper { padding: 0 18px 60px; }
  }
</style>
</head>
<body>

<div class="bg-orb bg-orb-1"></div>
<div class="bg-orb bg-orb-2"></div>
<div class="bg-grid"></div>
<div class="corner c-tl"></div>
<div class="corner c-tr"></div>
<div class="corner c-bl"></div>
<div class="corner c-br"></div>

<div class="wrapper">

  <!-- TOP BAR -->
  <div class="topbar">
    <div class="topbar-logo">
      <img class="logo-img" src="data:image/webp;base64,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
