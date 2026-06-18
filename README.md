
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HP Enterprising — Redline your enterprise.</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@600;700;800;900&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --graphite:#12161D;
    --panel:#1B212B;
    --panel-light:#232A36;
    --amber:#FF7A29;
    --cyan:#2FD1C2;
    --bone:#EDEAE2;
    --slate:#8893A1;
    --line: rgba(237,234,226,0.09);
    --maxw: 1180px;
  }

  *{margin:0;padding:0;box-sizing:border-box;}

  html{scroll-behavior:smooth;}

  body{
    background:var(--graphite);
    color:var(--bone);
    font-family:'Inter', sans-serif;
    font-size:16px;
    line-height:1.55;
    -webkit-font-smoothing:antialiased;
  }

  .mono{font-family:'JetBrains Mono', monospace;}
  .display{font-family:'Big Shoulders Display', sans-serif; text-transform:uppercase; letter-spacing:0.01em;}

  a{color:inherit; text-decoration:none;}

  img,svg{display:block; max-width:100%;}

  .wrap{
    max-width:var(--maxw);
    margin:0 auto;
    padding:0 28px;
  }

  :focus-visible{
    outline:2px solid var(--cyan);
    outline-offset:3px;
  }

  /* ---------- NAV ---------- */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(18,22,29,0.86);
    backdrop-filter: blur(10px);
    border-bottom:1px solid var(--line);
  }
  nav.wrap{
    display:flex; align-items:center; justify-content:space-between;
    height:76px;
  }
  .logo{
    display:flex; align-items:center; gap:10px;
    font-family:'Big Shoulders Display', sans-serif;
    font-weight:800;
    font-size:1.25rem;
    letter-spacing:0.02em;
    text-transform:uppercase;
  }
  .logo .mark{
    width:34px; height:34px;
    border-radius:7px;
    background:linear-gradient(135deg, var(--amber), #c9551b);
    display:flex; align-items:center; justify-content:center;
    color:var(--graphite);
    font-family:'JetBrains Mono', monospace;
    font-weight:700;
    font-size:0.78rem;
    flex-shrink:0;
  }
  .logo small{
    display:block;
    font-family:'JetBrains Mono', monospace;
    text-transform:uppercase;
    letter-spacing:0.18em;
    font-size:0.56rem;
    color:var(--slate);
    font-weight:500;
    margin-top:1px;
  }
  .nav-links{
    display:flex; align-items:center; gap:36px;
    font-size:0.92rem;
    font-weight:500;
    color:var(--slate);
  }
  .nav-links a:hover{color:var(--bone);}
  .nav-cta{
    display:flex; align-items:center; gap:18px;
  }
  .btn{
    display:inline-flex; align-items:center; justify-content:center;
    padding:11px 22px;
    border-radius:6px;
    font-size:0.88rem;
    font-weight:600;
    cursor:pointer;
    border:1px solid transparent;
    transition:transform .15s ease, background .2s ease, border-color .2s ease;
    white-space:nowrap;
  }
  .btn-primary{
    background:var(--amber);
    color:#1a0d04;
  }
  .btn-primary:hover{ transform:translateY(-1px); background:#ff8a45; }
  .btn-ghost{
    background:transparent;
    border-color:var(--line);
    color:var(--bone);
  }
  .btn-ghost:hover{ border-color:var(--cyan); color:var(--cyan); }

  .nav-toggle{ display:none; background:none; border:none; color:var(--bone); }

  /* ---------- HERO ---------- */
  .hero{
    padding:88px 0 70px;
    border-bottom:1px solid var(--line);
    position:relative;
    overflow:hidden;
  }
  .hero::before{
    content:'';
    position:absolute; inset:0;
    background:
      radial-gradient(ellipse 700px 380px at 78% 18%, rgba(255,122,41,0.10), transparent 70%),
      radial-gradient(ellipse 500px 320px at 5% 90%, rgba(47,209,194,0.07), transparent 70%);
    pointer-events:none;
  }
  .hero-grid{
    display:grid;
    grid-template-columns: 1.05fr 0.85fr;
    gap:56px;
    align-items:center;
    position:relative;
  }
  .eyebrow{
    display:inline-flex; align-items:center; gap:9px;
    font-family:'JetBrains Mono', monospace;
    font-size:0.74rem;
    letter-spacing:0.16em;
    text-transform:uppercase;
    color:var(--amber);
    font-weight:600;
    margin-bottom:22px;
  }
  .eyebrow::before{
    content:'';
    width:7px; height:7px; border-radius:50%;
    background:var(--amber);
    box-shadow:0 0 0 3px rgba(255,122,41,0.18);
  }
  h1{
    font-family:'Big Shoulders Display', sans-serif;
    font-weight:800;
    text-transform:uppercase;
    font-size:clamp(2.6rem, 5.4vw, 4.4rem);
    line-height:0.98;
    letter-spacing:0.005em;
    margin-bottom:22px;
  }
  h1 .accent{ color:var(--amber); }
  .hero p.lede{
    color:var(--slate);
    font-size:1.12rem;
    max-width:520px;
    margin-bottom:34px;
  }
  .hero-actions{ display:flex; gap:14px; margin-bottom:46px; flex-wrap:wrap;}
  .btn-lg{ padding:14px 26px; font-size:0.95rem; }

  .readout-strip{
    display:flex; gap:34px; flex-wrap:wrap;
    border-top:1px solid var(--line);
    padding-top:26px;
  }
  .readout{ }
  .readout .val{
    font-family:'JetBrains Mono', monospace;
    font-size:1.5rem;
    font-weight:700;
    color:var(--bone);
  }
  .readout .val.up{ color:var(--cyan); }
  .readout .label{
    font-size:0.7rem;
    letter-spacing:0.1em;
    text-transform:uppercase;
    color:var(--slate);
    font-family:'JetBrains Mono', monospace;
    margin-top:4px;
  }

  /* ---------- GAUGE ---------- */
  .gauge-wrap{
    background:var(--panel);
    border:1px solid var(--line);
    border-radius:16px;
    padding:30px 26px 22px;
    position:relative;
  }
  .gauge-wrap .tag{
    font-family:'JetBrains Mono', monospace;
    font-size:0.68rem;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--slate);
    display:flex; justify-content:space-between;
    margin-bottom:6px;
  }
  .gauge-wrap .tag span:last-child{ color:var(--cyan); }
  #gauge-svg{ width:100%; height:auto; }
  .gauge-readout{ text-align:center; margin-top:-18px; }
  .gauge-readout .num{
    font-family:'JetBrains Mono', monospace;
    font-weight:700;
    font-size:2.6rem;
    color:var(--bone);
  }
  .gauge-readout .num small{ font-size:1.2rem; color:var(--slate); }
  .gauge-readout .cap{
    font-size:0.72rem;
    letter-spacing:0.12em;
    text-transform:uppercase;
    color:var(--amber);
    font-weight:600;
    margin-top:2px;
  }
  .gauge-readout .sub{
    font-size:0.78rem;
    color:var(--slate);
    margin-top:6px;
  }

  /* ---------- SECTION shared ---------- */
  section{ padding:96px 0; }
  .section-head{ max-width:640px; margin-bottom:56px; }
  .section-head .eyebrow{ color:var(--cyan); }
  .section-head .eyebrow::before{ background:var(--cyan); box-shadow:0 0 0 3px rgba(47,209,194,0.18); }
  h2{
    font-family:'Big Shoulders Display', sans-serif;
    font-weight:800;
    text-transform:uppercase;
    font-size:clamp(2rem, 3.6vw, 2.9rem);
    line-height:1.04;
  }
  .section-head p{ color:var(--slate); margin-top:16px; font-size:1.04rem; }

  .reveal{ opacity:0; transform:translateY(18px); transition:opacity .6s ease, transform .6s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }

  /* ---------- CAPABILITIES ---------- */
  .cap-grid{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:22px;
  }
  .cap-card{
    background:var(--panel);
    border:1px solid var(--line);
    border-radius:14px;
    padding:30px 26px;
    transition:border-color .2s ease, transform .2s ease;
  }
  .cap-card:hover{ border-color:rgba(255,122,41,0.4); transform:translateY(-3px); }
  .cap-top{ display:flex; align-items:center; justify-content:space-between; margin-bottom:22px; }
  .mini-dial{ position:relative; width:54px; height:54px; }
  .mini-dial svg{ width:100%; height:100%; transform:rotate(-90deg); }
  .mini-dial .bg{ fill:none; stroke:var(--panel-light); stroke-width:6; }
  .mini-dial .fg{ fill:none; stroke:var(--amber); stroke-width:6; stroke-linecap:round; }
  .mini-dial .pct{
    position:absolute; inset:0; display:flex; align-items:center; justify-content:center;
    font-family:'JetBrains Mono', monospace; font-size:0.68rem; font-weight:700; color:var(--bone);
  }
  .cap-card h3{
    font-family:'Big Shoulders Display', sans-serif;
    font-weight:700;
    text-transform:uppercase;
    font-size:1.35rem;
    margin-bottom:12px;
  }
  .cap-card p{ color:var(--slate); font-size:0.96rem; }
  .cap-card .for{
    margin-top:18px; padding-top:16px; border-top:1px solid var(--line);
    font-family:'JetBrains Mono', monospace; font-size:0.7rem; letter-spacing:0.08em; text-transform:uppercase; color:var(--cyan);
  }

  /* ---------- METHOD ---------- */
  .method{ background:var(--panel); border-top:1px solid var(--line); border-bottom:1px solid var(--line); }
  .method-grid{
    display:grid; grid-template-columns:repeat(3,1fr); gap:0;
    position:relative;
  }
  .step{ padding:0 30px 0 0; position:relative; }
  .step:not(:last-child)::after{
    content:'';
    position:absolute; top:18px; right:-1px; bottom:auto;
    width:1px; height:calc(100% - 18px);
    background:var(--line);
  }
  .step-num{
    font-family:'JetBrains Mono', monospace;
    font-weight:700; font-size:0.85rem;
    color:var(--amber);
    border:1px solid rgba(255,122,41,0.35);
    border-radius:50%;
    width:36px; height:36px;
    display:flex; align-items:center; justify-content:center;
    margin-bottom:20px;
  }
  .step h3{
    font-family:'Big Shoulders Display', sans-serif;
    text-transform:uppercase; font-weight:700; font-size:1.5rem;
    margin-bottom:12px;
  }
  .step p{ color:var(--slate); font-size:0.96rem; max-width:300px; }

  /* ---------- STATS DASHBOARD ---------- */
  .dash{
    background:linear-gradient(160deg, var(--panel), var(--graphite));
    border:1px solid var(--line);
    border-radius:18px;
    padding:54px 44px;
    display:grid;
    grid-template-columns:repeat(4, 1fr);
    gap:36px;
  }
  .dash-item{ border-left:1px solid var(--line); padding-left:24px; }
  .dash-item:first-child{ border-left:none; padding-left:0; }
  .dash-item .num{
    font-family:'JetBrains Mono', monospace; font-weight:700;
    font-size:clamp(2rem, 4vw, 2.6rem);
    color:var(--bone);
  }
  .dash-item .num.cyan{ color:var(--cyan); }
  .dash-item .lbl{
    color:var(--slate); font-size:0.86rem; margin-top:8px;
  }

  /* ---------- TESTIMONIALS ---------- */
  .quote-grid{
    display:grid; grid-template-columns:repeat(3,1fr); gap:22px;
  }
  .quote-card{
    background:var(--panel); border:1px solid var(--line); border-radius:14px;
    padding:28px 26px;
  }
  .quote-card .mark{ color:var(--amber); font-family:'Big Shoulders Display'; font-size:2.4rem; line-height:1; display:block; margin-bottom:6px;}
  .quote-card p.q{ font-size:1.01rem; margin-bottom:20px; }
  .quote-card .who{ font-family:'JetBrains Mono', monospace; font-size:0.76rem; color:var(--slate); text-transform:uppercase; letter-spacing:0.04em;}
  .quote-card .who b{ color:var(--cyan); font-weight:600; }

  /* ---------- CTA ---------- */
  .cta-panel{
    background:radial-gradient(ellipse 600px 300px at 20% 0%, rgba(255,122,41,0.16), transparent 70%), var(--panel);
    border:1px solid var(--line);
    border-radius:18px;
    padding:64px 50px;
    display:flex; align-items:center; justify-content:space-between; gap:40px;
    flex-wrap:wrap;
  }
  .cta-panel h2{ max-width:480px; }
  .cta-panel .note{ color:var(--slate); font-size:0.88rem; margin-top:10px; }
  .cta-actions{ display:flex; flex-direction:column; align-items:flex-start; gap:10px; }

  /* ---------- FOOTER ---------- */
  footer{ border-top:1px solid var(--line); padding:56px 0 36px; }
  .foot-grid{
    display:grid; grid-template-columns:1.6fr 1fr 1fr 1fr; gap:40px;
    margin-bottom:48px;
  }
  .foot-brand p{ color:var(--slate); font-size:0.92rem; margin-top:14px; max-width:280px; }
  .foot-col h4{
    font-family:'JetBrains Mono', monospace; font-size:0.74rem; letter-spacing:0.12em; text-transform:uppercase;
    color:var(--slate); margin-bottom:16px;
  }
  .foot-col a{ display:block; color:var(--bone); font-size:0.92rem; margin-bottom:10px; opacity:0.85; }
  .foot-col a:hover{ color:var(--cyan); opacity:1; }
  .foot-bottom{
    display:flex; justify-content:space-between; align-items:center;
    border-top:1px solid var(--line); padding-top:26px;
    color:var(--slate); font-size:0.82rem; flex-wrap:wrap; gap:10px;
  }
  .foot-bottom .mono{ color:var(--slate); }

  /* ---------- RESPONSIVE ---------- */
  @media (max-width: 920px){
    .hero-grid{ grid-template-columns:1fr; }
    .gauge-wrap{ max-width:420px; }
    .cap-grid{ grid-template-columns:1fr; }
    .method-grid{ grid-template-columns:1fr; gap:40px; }
    .step:not(:last-child)::after{ display:none; }
    .dash{ grid-template-columns:repeat(2,1fr); }
    .dash-item:nth-child(3){ border-left:none; padding-left:0; }
    .quote-grid{ grid-template-columns:1fr; }
    .foot-grid{ grid-template-columns:1fr 1fr; gap:32px; }
  }
  @media (max-width: 760px){
    .nav-links{ display:none; }
    .nav-toggle{ display:block; }
    .nav-cta .btn-ghost{ display:none; }
  }
  @media (max-width: 560px){
    .readout-strip{ gap:24px; }
    .cta-panel{ padding:42px 26px; }
    .foot-grid{ grid-template-columns:1fr; }
  }

  @media (prefers-reduced-motion: reduce){
    *{ transition:none !important; animation:none !important; }
    html{ scroll-behavior:auto; }
  }

/* --- Premium Expansion Layer --- */
.impact-grid,.insight-grid{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:22px;
}
.impact-card,.insight-card{
background:var(--panel);
border:1px solid var(--line);
border-radius:14px;
padding:28px;
}
.impact-card h3,.insight-card h3{
font-family:'Big Shoulders Display',sans-serif;
font-size:1.5rem;
text-transform:uppercase;
margin-bottom:12px;
}
.metric-bar{
height:10px;
background:var(--panel-light);
border-radius:999px;
overflow:hidden;
margin-top:12px;
}
.metric-fill{
height:100%;
background:linear-gradient(90deg,var(--amber),var(--cyan));
}
.marquee{
overflow:hidden;
border-top:1px solid var(--line);
border-bottom:1px solid var(--line);
padding:18px 0;
white-space:nowrap;
}
.marquee-track{
display:inline-block;
animation:scroll 20s linear infinite;
font-family:'JetBrains Mono',monospace;
color:var(--slate);
}
@keyframes scroll{
from{transform:translateX(0)}
to{transform:translateX(-50%)}
}
@media(max-width:920px){
.impact-grid,.insight-grid{grid-template-columns:1fr;}
}


/* Visual Upgrade */
.hero::after{
content:'';
position:absolute;
right:-120px;
top:40px;
width:420px;
height:420px;
border-radius:50%;
background:radial-gradient(circle, rgba(47,209,194,.12), transparent 70%);
pointer-events:none;
}
section{padding:110px 0;}
.cap-card,.quote-card,.impact-card,.insight-card,.gauge-wrap{
box-shadow:0 20px 60px rgba(0,0,0,.18);
}
.section-head{
margin-left:auto;
margin-right:auto;
text-align:center;
}
.cap-grid,.quote-grid,.impact-grid,.insight-grid{
align-items:stretch;
}
.cap-card p,.quote-card p,.impact-card p,.insight-card p{
line-height:1.7;
}
.dash{
margin-top:20px;
}

</style>
</head>
<body>

<header>
  <nav class="wrap">
    <div class="logo">
      <span class="mark">HP</span>
      <span>HP Enterprising<small>Performance &amp; Growth Tuning</small></span>
    </div>
    <div class="nav-links">
      <a href="#capabilities">Capabilities</a>
      <a href="#method">Method</a>
      <a href="#results">Results</a>
      <a href="#insights">Insights</a>
      <a href="#impact">Impact</a>
      <a href="#contact">Contact</a>
    </div>
    <div class="nav-cta">
      <a href="#contact" class="btn btn-ghost">Log in</a>
      <a href="#contact" class="btn btn-primary">Book a diagnostic</a>
    </div>
    <button class="nav-toggle" aria-label="Menu">☰</button>
  </nav>
</header>

<section class="hero">
  <div class="wrap hero-grid">
    <div>
      <div class="eyebrow">Enterprise performance tuning</div>
      <h1>Redline your <span class="accent">enterprise.</span></h1>
      <p class="lede">We help enterprises scale faster by removing friction, accelerating growth, and improving execution.</p>
      <div class="hero-actions">
        <a href="#contact" class="btn btn-primary btn-lg">Book a diagnostic</a>
        <a href="#method" class="btn btn-ghost btn-lg">See the method</a>
      </div>
      <div class="readout-strip">
        <div class="readout">
          <div class="val up">+38%</div>
          <div class="label">Throughput</div>
        </div>
        <div class="readout">
          <div class="val up">2.4×</div>
          <div class="label">Pipeline velocity</div>
        </div>
        <div class="readout">
          <div class="val up">+51%</div>
          <div class="label">Share of voice</div>
        </div>
        <div class="readout">
          <div class="val">90d</div>
          <div class="label">To first result</div>
        </div>
      </div>
    </div>

    <div class="gauge-wrap">
      <div class="tag"><span>LIVE READOUT</span><span id="gauge-status">● CALIBRATING</span></div>
      <svg id="gauge-svg" viewBox="0 0 300 185" xmlns="http://www.w3.org/2000/svg">
        <path d="M20,160 A130,130 0 0 1 280,160" fill="none" stroke="#232A36" stroke-width="14" stroke-linecap="round"/>
        <path id="gauge-fg" d="M20,160 A130,130 0 0 1 280,160" fill="none" stroke="#FF7A29" stroke-width="14" stroke-linecap="round"/>
        <line x1="30" y1="160" x2="10" y2="160" stroke="#8893A1" stroke-width="2"/>
        <line x1="65.15" y1="75.15" x2="51.01" y2="61.01" stroke="#8893A1" stroke-width="2"/>
        <line x1="150" y1="40" x2="150" y2="20" stroke="#8893A1" stroke-width="2"/>
        <line x1="234.85" y1="75.15" x2="248.99" y2="61.01" stroke="#8893A1" stroke-width="2"/>
        <line x1="270" y1="160" x2="290" y2="160" stroke="#8893A1" stroke-width="2"/>
        <circle cx="150" cy="160" r="9" fill="#12161D" stroke="#FF7A29" stroke-width="2"/>
        <line id="needle" x1="150" y1="160" x2="150" y2="45" stroke="#EDEAE2" stroke-width="3" stroke-linecap="round" style="transform-origin:150px 160px; transform:rotate(-90deg); transition:transform 1.7s cubic-bezier(.2,.8,.2,1);"/>
      </svg>
      <div class="gauge-readout">
        <div class="num"><span id="gauge-number">0</span><small>/100</small></div>
        <div class="cap">Performance index</div>
        <div class="sub">Median client, 90 days post-tune</div>
      </div>
    </div>
  </div>
</section>

<section id="capabilities">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">What we tune</div>
      <h2>Three systems, one output.</h2>
      <p>Three core systems. One measurable outcome.</p>
    </div>
    <div class="cap-grid">
      <div class="cap-card reveal">
        <div class="cap-top">
          <h3 style="margin:0;">Productivity<br>engineering</h3>
          <div class="mini-dial">
            <svg viewBox="0 0 60 60"><circle class="bg" cx="30" cy="30" r="24"/><circle class="fg" cx="30" cy="30" r="24" stroke-dasharray="150.8" stroke-dashoffset="93.5"/></svg>
            <div class="pct">38%</div>
          </div>
        </div>
        <p>We strip the friction out of how work actually moves — handoffs, approvals, tooling — so teams produce more without burning out doing it.</p>
        <div class="for">For operations &amp; teams</div>
      </div>
      <div class="cap-card reveal">
        <div class="cap-top">
          <h3 style="margin:0;">Growth<br>systems</h3>
          <div class="mini-dial">
            <svg viewBox="0 0 60 60"><circle class="bg" cx="30" cy="30" r="24"/><circle class="fg" cx="30" cy="30" r="24" stroke-dasharray="150.8" stroke-dashoffset="36.2"/></svg>
            <div class="pct">2.4×</div>
          </div>
        </div>
        <p>We rebuild the machinery between a lead and a closed deal — pipeline, pricing, retention — so growth compounds instead of plateauing.</p>
        <div class="for">For revenue &amp; leadership</div>
      </div>
      <div class="cap-card reveal">
        <div class="cap-top">
          <h3 style="margin:0;">Demand &amp;<br>reach</h3>
          <div class="mini-dial">
            <svg viewBox="0 0 60 60"><circle class="bg" cx="30" cy="30" r="24"/><circle class="fg" cx="30" cy="30" r="24" stroke-dasharray="150.8" stroke-dashoffset="73.9"/></svg>
            <div class="pct">51%</div>
          </div>
        </div>
        <p>We put your name in front of the people who decide your budget exists, through channels built around how your buyers actually pay attention.</p>
        <div class="for">For marketing &amp; brand</div>
      </div>
    </div>
  </div>
</section>

<section class="method" id="method">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">How a tune-up runs</div>
      <h2>Three weeks. Three gears.</h2>
      <p>A proven process designed for speed and clarity.</p>
    </div>
    <div class="method-grid">
      <div class="step reveal">
        <div class="step-num">01</div>
        <h3>Diagnostic</h3>
        <p>We instrument your operation for two weeks — the real one, not the org chart — and find exactly where output is leaking.</p>
      </div>
      <div class="step reveal">
        <div class="step-num">02</div>
        <h3>Tune</h3>
        <p>We rebuild the three or four systems doing the most damage, working alongside the people who run them day to day.</p>
      </div>
      <div class="step reveal">
        <div class="step-num">03</div>
        <h3>Run</h3>
        <p>We hand back a faster machine, plus the readouts to keep it that way — no permanent dependency on us.</p>
      </div>
    </div>
  </div>
</section>

<section id="results">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">On the gauges</div>
      <h2>What clients see by day 90.</h2>
    </div>
    <div class="dash reveal">
      <div class="dash-item">
        <div class="num">38%</div>
        <div class="lbl">Average throughput gain</div>
      </div>
      <div class="dash-item">
        <div class="num cyan">2.4×</div>
        <div class="lbl">Pipeline velocity</div>
      </div>
      <div class="dash-item">
        <div class="num">51%</div>
        <div class="lbl">Lift in qualified reach</div>
      </div>
      <div class="dash-item">
        <div class="num cyan">90</div>
        <div class="lbl">Days to measurable gain</div>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">From the dashboard</div>
      <h2>Three teams, three readouts.</h2>
    </div>
    <div class="quote-grid">
      <div class="quote-card reveal">
        <span class="mark">"</span>
        <p class="q">We stopped guessing which lever to pull. Now we can actually watch the dial move.</p>
        <div class="who">Solace Freight — <b>COO</b></div>
      </div>
      <div class="quote-card reveal">
        <span class="mark">"</span>
        <p class="q">Our pipeline didn't get bigger. It got honest. That mattered a lot more than size.</p>
        <div class="who">Northwind Materials — <b>CMO</b></div>
      </div>
      <div class="quote-card reveal">
        <span class="mark">"</span>
        <p class="q">Three weeks in, and the backlog that haunted us for a year was simply gone.</p>
        <div class="who">Vantage Retail Group — <b>CEO</b></div>
      </div>
    </div>
  </div>
</section>


<section class="marquee">
  <div class="marquee-track">
    STRATEGY • OPERATIONS • AI ENABLEMENT • PRODUCTIVITY • EXPANSION • MARKET DOMINANCE • EXECUTION EXCELLENCE • STRATEGY • OPERATIONS • AI ENABLEMENT • PRODUCTIVITY • EXPANSION •
  </div>
</section>

<section id="insights">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">Executive intelligence</div>
      <h2>See the enterprise before you change it.</h2>
      <p>Clear visibility. Faster decisions. Better outcomes.</p>
    </div>
    <div class="insight-grid">
      <div class="insight-card reveal">
        <h3>Growth Mapping</h3>
        <p>Identify bottlenecks, revenue leaks, and expansion opportunities across the entire organization.</p>
      </div>
      <div class="insight-card reveal">
        <h3>AI Integration</h3>
        <p>Deploy practical AI workflows that reduce operational drag and increase team capacity.</p>
      </div>
      <div class="insight-card reveal">
        <h3>Executive Dashboards</h3>
        <p>Real-time KPI visibility for leaders who need fast, confident decision making.</p>
      </div>
    </div>
  </div>
</section>

<section id="impact">
  <div class="wrap">
    <div class="section-head reveal">
      <div class="eyebrow">Transformation scorecard</div>
      <h2>Measured impact across the enterprise.</h2>
    </div>
    <div class="impact-grid">
      <div class="impact-card reveal">
        <h3>Operational Efficiency</h3>
        <p>92/100 performance index</p>
        <div class="metric-bar"><div class="metric-fill" style="width:92%"></div></div>
      </div>
      <div class="impact-card reveal">
        <h3>Revenue Velocity</h3>
        <p>87/100 acceleration score</p>
        <div class="metric-bar"><div class="metric-fill" style="width:87%"></div></div>
      </div>
      <div class="impact-card reveal">
        <h3>Market Visibility</h3>
        <p>95/100 awareness score</p>
        <div class="metric-bar"><div class="metric-fill" style="width:95%"></div></div>
      </div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap">
    <div class="cta-panel reveal">
      <div>
        <h2>Ready to see your numbers?</h2>
        <p class="note">A 30-minute diagnostic call. We'll tell you, free, where your three biggest leaks are. No deck, no pitch — just your dashboard.</p>
      </div>
      <div class="cta-actions">
        <a href="mailto:hello@hpenterprising.com" class="btn btn-primary btn-lg">Book a diagnostic</a>
        <span class="mono" style="font-size:0.82rem; color:var(--slate);">hello@hpenterprising.com</span>
      </div>
    </div>
  </div>
</section>


<section>
<div class="wrap">
<div style="height:220px;border-radius:20px;border:1px solid rgba(255,255,255,.08);background:
radial-gradient(circle at 20% 30%, rgba(255,122,41,.18), transparent 35%),
radial-gradient(circle at 80% 70%, rgba(47,209,194,.18), transparent 35%),
linear-gradient(180deg,#1B212B,#12161D);"></div>
</div>
</section>
<footer>

  <div class="wrap">
    <div class="foot-grid">
      <div class="foot-brand">
        <div class="logo"><span class="mark">HP</span><span>HP Enterprising</span></div>
        <p>We tune large organizations the way an engineer tunes a machine — diagnose the drag, rebuild the system, hand back the readouts.</p>
      </div>
      <div class="foot-col">
        <h4>Company</h4>
        <a href="#capabilities">Capabilities</a>
        <a href="#method">Method</a>
        <a href="#results">Results</a>
      </div>
      <div class="foot-col">
        <h4>Get in touch</h4>
        <a href="mailto:hello@hpenterprising.com">hello@hpenterprising.com</a>
        <a href="#contact">Book a diagnostic</a>
      </div>
      <div class="foot-col">
        <h4>Office</h4>
        <a href="#" style="opacity:.6; cursor:default;">Columbus, Ohio</a>
      </div>
    </div>
    <div class="foot-bottom">
      <span>© 2026 HP Enterprising. All systems go.</span>
      <span class="mono">v4.6 / build stable</span>
    </div>
  </div>
</footer>

<script>
  // Respect reduced motion
  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  // Gauge sweep + counter
  function runGauge(){
    const needle = document.getElementById('needle');
    const fg = document.getElementById('gauge-fg');
    const numEl = document.getElementById('gauge-number');
    const status = document.getElementById('gauge-status');
    const target = 92;
    const len = fg.getTotalLength();

    fg.style.strokeDasharray = len;
    fg.style.strokeDashoffset = len;
    fg.style.transition = reduceMotion ? 'none' : 'stroke-dashoffset 1.7s cubic-bezier(.2,.8,.2,1)';

    if(reduceMotion){
      needle.style.transition = 'none';
      needle.style.transform = 'rotate(75.6deg)';
      fg.style.strokeDashoffset = len * (1 - target/100);
      numEl.textContent = target;
      status.textContent = '● TUNED';
      return;
    }

    requestAnimationFrame(() => {
      needle.style.transform = 'rotate(75.6deg)';
      fg.style.strokeDashoffset = len * (1 - target/100);
    });

    let cur = 0;
    const dur = 1700, start = performance.now();
    function tick(now){
      const p = Math.min((now - start) / dur, 1);
      const eased = 1 - Math.pow(1 - p, 3);
      cur = Math.round(eased * target);
      numEl.textContent = cur;
      if(p < 1){ requestAnimationFrame(tick); } else { status.textContent = '● TUNED'; }
    }
    requestAnimationFrame(tick);
  }
  window.addEventListener('load', () => setTimeout(runGauge, 250));

  // Scroll reveal
  const revealEls = document.querySelectorAll('.reveal');
  if(reduceMotion){
    revealEls.forEach(el => el.classList.add('in'));
  } else {
    const obs = new IntersectionObserver((entries) => {
      entries.forEach(e => { if(e.isIntersecting){ e.target.classList.add('in'); obs.unobserve(e.target); } });
    }, { threshold: 0.15 });
    revealEls.forEach(el => obs.observe(el));
  }

  // Mobile nav toggle (simple show/hide of links as a stacked menu)
  const toggle = document.querySelector('.nav-toggle');
  const links = document.querySelector('.nav-links');
  toggle.addEventListener('click', () => {
    const open = links.style.display === 'flex';
    links.style.display = open ? 'none' : 'flex';
    links.style.flexDirection = 'column';
    links.style.position = 'absolute';
    links.style.top = '76px';
    links.style.left = '0';
    links.style.right = '0';
    links.style.background = '#1B212B';
    links.style.padding = '20px 28px';
    links.style.borderBottom = '1px solid rgba(237,234,226,0.09)';
    links.style.gap = '18px';
  });
</script>

</body>
</html>   
