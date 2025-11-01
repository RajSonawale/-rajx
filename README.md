<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Simple Responsive Landing — Demo</title>
  <meta name="description" content="A clean, responsive single-file landing page template (HTML/CSS/JS)." />
  <style>
    /* Simple modern CSS - single-file template */
    :root{
      --bg:#0f1724; /* deep navy */
      --card:#0b1220;
      --muted:#9aa4b2;
      --accent:#7c3aed;
      --glass: rgba(255,255,255,0.04);
      --radius:14px;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      background:linear-gradient(180deg,var(--bg),#071025 60%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:24px;
    }
    .container{max-width:1100px;margin:0 auto}/* Header / Nav */
header{display:flex;align-items:center;justify-content:space-between;padding:12px 0}
.brand{display:flex;gap:12px;align-items:center}
.logo{width:44px;height:44px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#06b6d4);display:flex;align-items:center;justify-content:center;font-weight:700;color:#fff}
nav{display:flex;gap:18px;align-items:center}
nav a{color:var(--muted);text-decoration:none;font-weight:600}
.btn{background:linear-gradient(90deg,var(--accent),#06b6d4);padding:10px 14px;border-radius:10px;color:white;text-decoration:none;font-weight:700}
.mobile-toggle{display:none}

/* Hero */
.hero{display:grid;grid-template-columns:1fr 420px;gap:32px;align-items:center;padding:36px 0}
.eyebrow{display:inline-block;background:var(--glass);padding:6px 10px;border-radius:999px;color:var(--muted);font-weight:700;margin-bottom:12px}
h1{font-size:36px;margin:6px 0 10px}
p.lead{color:var(--muted);max-width:64ch}
.cards{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:18px}
.card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:14px;border-radius:12px}
.hero-img{background:linear-gradient(180deg,#0b1220,#071025);border-radius:14px;padding:18px;box-shadow:0 6px 30px rgba(2,6,23,0.6)}
.feature-list{list-style:none;padding:0;margin:16px 0 0}
.feature-list li{margin:10px 0;color:var(--muted)}

/* Sections */
section{padding:36px 0}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.pricing{display:flex;gap:18px;flex-wrap:wrap}
.plan{background:var(--card);padding:18px;border-radius:12px;flex:1;min-width:180px}

/* Footer */
footer{padding:28px 0;color:var(--muted);border-top:1px solid rgba(255,255,255,0.03);margin-top:18px}

/* Responsive */
@media (max-width:900px){
  .hero{grid-template-columns:1fr;}
  .cards{grid-template-columns:repeat(2,1fr)}
  .grid-3{grid-template-columns:1fr 1fr}
  nav{display:none}
  .mobile-toggle{display:block}
}
@media (max-width:520px){
  .cards{grid-template-columns:1fr}
  .grid-3{grid-template-columns:1fr}
  h1{font-size:28px}
}

/* small utilities */
.muted{color:var(--muted)}
.center{text-align:center}
.pill{display:inline-block;padding:6px 10px;background:rgba(255,255,255,0.03);border-radius:999px}
input,textarea{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit}
.row{display:flex;gap:12px}

  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">LP</div>
        <div>
          <div style="font-weight:800">LaunchPad</div>
          <div style="font-size:12px;color:var(--muted);margin-top:2px">Clean single-file starter</div>
        </div>
      </div><nav>
    <a href="#features">Features</a>
    <a href="#pricing">Pricing</a>
    <a href="#contact">Contact</a>
    <a class="btn" href="#get-started">Get started</a>
  </nav>

  <button class="mobile-toggle" aria-expanded="false" aria-label="Menu" id="mobileBtn">☰</button>
</header>

<main>
  <section class="hero">
    <div>
      <div class="eyebrow">New — 2025 template</div>
      <h1>Ship faster with a tiny, beautiful landing page</h1>
      <p class="lead">A single-file HTML template with responsive layout, simple components, and a small JS helper. Plug in your copy, change the colors, and you're ready to launch.</p>

      <div style="margin-top:18px">
        <a class="btn" href="#get-started">Start free trial</a>
        <a href="#features" style="margin-left:12px;color:var(--muted);font-weight:700">Explore features →</a>
      </div>

      <div class="cards" aria-hidden="true">
        <div class="card">
          <strong>Fast to edit</strong>
          <div class="muted">Single HTML file — zero build tools required.</div>
        </div>
        <div class="card">
          <strong>Accessible</strong>
          <div class="muted">Keyboard-friendly and responsive from the start.</div>
        </div>
        <div class="card">
          <strong>Customizable</strong>
          <div class="muted">Change colors and content in seconds.</div>
        </div>
      </div>
    </div>

    <aside class="hero-img">
      <div style="display:flex;flex-direction:column;gap:12px">
        <div style="background:linear-gradient(90deg,rgba(255,255,255,0.02),transparent);padding:12px;border-radius:10px">
          <div style="font-weight:800">Dashboard</div>
          <div class="muted" style="font-size:13px;margin-top:6px">Quick metrics at a glance</div>
        </div>

        <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px">
          <div style="background:rgba(255,255,255,0.02);padding:10px;border-radius:10px">
            <div style="font-weight:700">Uptime</div>
            <div class="muted">99.99%</div>
          </div>
          <div style="background:rgba(255,255,255,0.02);padding:10px;border-radius:10px">
            <div style="font-weight:700">Response</div>
            <div class="muted">120ms</div>
          </div>
        </div>

        <div style="margin-top:6px;border-radius:10px;padding:12px;background:linear-gradient(90deg,rgba(124,58,237,0.12),rgba(6,182,212,0.06));">
          <div style="font-weight:800">Ready to ship</div>
          <div class="muted" style="font-size:13px;margin-top:6px">Copy this file, edit content, and host anywhere.</div>
        </div>
      </div>
    </aside>
  </section>

  <section id="features">
    <div style="display:flex;justify-content:space-between;align-items:center">
      <div>
        <h2>Features</h2>
        <p class="muted">Everything you need to present your product, service, or idea.</p>
      </div>
      <div class="pill">No frameworks • Single file</div>
    </div>

    <div class="grid-3" style="margin-top:16px">
      <div>
        <h3 style="margin:6px 0">Responsive layout</h3>
        <p class="muted">Works great on phones, tablets and desktop without extra work.</p>
      </div>
      <div>
        <h3 style="margin:6px 0">Accessible</h3>
        <p class="muted">Semantic markup and sensible contrast make it usable for more people.</p>
      </div>
      <div>
        <h3 style="margin:6px 0">Small JS</h3>
        <p class="muted">Only a few lines of JavaScript for UI interactions.</p>
      </div>
    </div>
  </section>

  <section id="pricing">
    <h2>Pricing</h2>
    <p class="muted">Simple plans for small teams and solopreneurs.</p>

    <div class="pricing" style="margin-top:16px">
      <div class="plan">
        <div style="font-weight:800">Free</div>
        <div class="muted">$0 • Basic features, community support</div>
      </div>
      <div class="plan">
        <div style="font-weight:800">Pro</div>
        <div class="muted">$12 / month • Support, analytics</div>
      </div>
      <div class="plan">
        <div style="font-weight:800">Enterprise</div>
        <div class="muted">Custom • Priority support</div>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p class="muted">Have questions? Send a message and we'll reply within 1–2 business days.</p>

    <form id="contactForm" style="margin-top:16px;max-width:720px">
      <div class="row">
        <input type="text" id="name" placeholder="Your name" required />
        <input type="email" id="email" placeholder="Email" required />
      </div>
      <div style="margin-top:12px">
        <textarea id="message" rows="5" placeholder="How can we help?" required></textarea>
      </div>
      <div style="margin-top:12px;display:flex;gap:8px;align-items:center">
        <button class="btn" id="sendBtn" type="submit">Send message</button>
        <div id="formStatus" class="muted" aria-live="polite"></div>
      </div>
    </form>
  </section>
</main>

<footer>
  <div style="display:flex;justify-content:space-between;align-items:center">
    <div>
      <div style="font-weight:800">LaunchPad</div>
      <div class="muted" style="font-size:13px">© "2025" • Made with care</div>
    </div>
    <div class="muted">Built with ❤ — edit this template</div>
  </div>
</footer>

  </div>  <script>
    // tiny JS helpers
    const mobileBtn = document.getElementById('mobileBtn');
    mobileBtn.addEventListener('click', ()=>{
      const nav = document.querySelector('nav');
      const expanded = mobileBtn.getAttribute('aria-expanded') === 'true';
      mobileBtn.setAttribute('aria-expanded', String(!expanded));
      nav.style.display = expanded ? 'none' : 'flex';
    });

    // simple client-side form handler (no backend) — demonstrates validation + fake send
    const form = document.getElementById('contactForm');
    const status = document.getElementById('formStatus');
    form.addEventListener('submit', (e)=>{
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      if(!name || !email || !message){
        status.textContent = 'Please fill out all fields.';
        return;
      }
      status.textContent = 'Sending...';
      // simulate a send
      setTimeout(()=>{
        status.textContent = 'Thanks — we received your message! (Demo)';
        form.reset();
      },900);
    });

    // smooth scroll for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', (e)=>{
        const target = a.getAttribute('href').slice(1);
        if(!target) return;
        e.preventDefault();
        const el = document.getElementById(target);
        if(el) el.scrollIntoView({behavior:'smooth',block:'start'});
      });
    });
  </script></body>
</html>
