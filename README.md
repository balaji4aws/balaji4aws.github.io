<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Venky · BI + AI Builder</title>
<meta name="description" content="Portfolio of Venky (Balaji Venkatesh) — data products, decision systems, and AI on AWS. Business-first engineering that helps people make better decisions." />
<meta name="author" content="Balaji Venkatesh" />

<!-- Open Graph / social preview -->
<meta property="og:title" content="Venky · BI + AI Builder" />
<meta property="og:description" content="Data products, decision systems, and AI on AWS — engineering that helps people make better decisions." />
<meta property="og:type" content="website" />
<meta property="og:url" content="https://balaji4aws.github.io/" />

<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />

<style>
  :root {
    --bg: #131a22;          /* Amazon squid-ink */
    --surface: #1b232d;
    --surface-2: #232f3e;   /* Amazon navy */
    --border: #2d3a48;
    --text: #e8eef4;
    --muted: #9fb0c0;
    --accent: #ff9900;      /* Amazon orange */
    --link: #4ea1ff;        /* link blue */
    --radius: 14px;
    --maxw: 820px;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
    padding: 0 20px;
  }

  .wrap { max-width: var(--maxw); margin: 0 auto; }

  /* ---------- Hero ---------- */
  header.hero {
    padding: 88px 0 48px;
    border-bottom: 1px solid var(--border);
  }
  .eyebrow {
    color: var(--accent);
    font-weight: 600;
    font-size: 0.9rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 14px;
  }
  h1 {
    font-size: clamp(2.1rem, 5vw, 3rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    line-height: 1.1;
    margin-bottom: 18px;
  }
  h1 .name { color: var(--text); }
  .lead {
    font-size: 1.15rem;
    color: var(--muted);
    max-width: 640px;
    margin-bottom: 28px;
  }
  .lead strong { color: var(--text); font-weight: 600; }

  .quote {
    border-left: 3px solid var(--accent);
    padding: 6px 0 6px 18px;
    color: var(--text);
    font-style: italic;
    font-size: 1.05rem;
    max-width: 620px;
  }

  /* ---------- Sections ---------- */
  section { padding: 44px 0; border-bottom: 1px solid var(--border); }
  section:last-of-type { border-bottom: none; }

  h2 {
    font-size: 1.4rem;
    font-weight: 700;
    margin-bottom: 20px;
    letter-spacing: -0.01em;
  }

  /* ---------- Approach pills ---------- */
  .flow {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 16px;
  }
  .flow span {
    background: var(--surface);
    border: 1px solid var(--border);
    color: var(--muted);
    padding: 6px 12px;
    border-radius: 999px;
    font-size: 0.85rem;
    font-weight: 500;
  }
  .flow span.arrow { border: none; background: none; color: var(--accent); padding: 6px 2px; }
  .approach-note { color: var(--muted); font-size: 0.98rem; }

  /* ---------- Project card ---------- */
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    overflow: hidden;
  }
  .card .shot {
    display: block;
    width: 100%;
    aspect-ratio: 16 / 8;
    object-fit: cover;
    background: var(--surface-2);
    border-bottom: 1px solid var(--border);
  }
  /* placeholder shown if no screenshot yet */
  .shot-placeholder {
    width: 100%;
    aspect-ratio: 16 / 8;
    background: linear-gradient(135deg, var(--surface-2), var(--surface));
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--muted);
    font-size: 0.9rem;
    text-align: center;
    padding: 20px;
  }
  .card .body { padding: 24px; }
  .card h3 {
    font-size: 1.25rem;
    font-weight: 700;
    margin-bottom: 10px;
  }
  .card h3 a { color: var(--text); text-decoration: none; }
  .card h3 a:hover { color: var(--link); }
  .card p { color: var(--muted); margin-bottom: 16px; }
  .card ul { list-style: none; margin-bottom: 20px; }
  .card li {
    color: var(--muted);
    padding-left: 22px;
    position: relative;
    margin-bottom: 8px;
    font-size: 0.98rem;
  }
  .card li::before {
    content: "✓";
    color: var(--accent);
    position: absolute;
    left: 0;
    font-weight: 700;
  }
  .card li strong { color: var(--text); font-weight: 600; }

  .btn-row { display: flex; flex-wrap: wrap; gap: 12px; align-items: center; }
  .btn {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    background: var(--accent);
    color: #131a22;
    font-weight: 700;
    font-size: 0.95rem;
    padding: 10px 18px;
    border-radius: 8px;
    text-decoration: none;
    transition: filter 0.15s ease;
  }
  .btn:hover { filter: brightness(1.08); }
  .btn.secondary {
    background: transparent;
    color: var(--link);
    border: 1px solid var(--border);
  }
  .btn.secondary:hover { border-color: var(--link); filter: none; }

  .stack {
    margin-top: 16px;
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
  }
  .stack code {
    background: var(--surface-2);
    color: var(--muted);
    padding: 3px 9px;
    border-radius: 6px;
    font-size: 0.8rem;
    font-family: 'SFMono-Regular', Consolas, monospace;
  }

  /* ---------- Focus areas ---------- */
  .focus { color: var(--muted); font-size: 1.02rem; }
  .focus b { color: var(--text); font-weight: 600; }

  /* ---------- Connect ---------- */
  .links { display: flex; flex-wrap: wrap; gap: 14px; }
  .links a {
    color: var(--link);
    text-decoration: none;
    font-weight: 500;
    border: 1px solid var(--border);
    padding: 9px 16px;
    border-radius: 8px;
    transition: border-color 0.15s ease;
  }
  .links a:hover { border-color: var(--link); }

  footer {
    padding: 36px 0 56px;
    color: var(--muted);
    font-size: 0.88rem;
    text-align: center;
  }

  a { color: var(--link); }

  @media (max-width: 560px) {
    header.hero { padding: 56px 0 36px; }
    .card .body { padding: 18px; }
  }
</style>
</head>
<body>
<div class="wrap">

  <header class="hero">
    <div class="eyebrow">Business Intelligence · Data Engineering · AI</div>
    <h1><span class="name">Hi, I'm Venky</span> 👋</h1>
    <p class="lead">
      I build <strong>data products and decision systems</strong> that help businesses act on their
      data — not just report it. My work sits at the intersection of Business Intelligence,
      Data Engineering, AWS, and AI, and it starts with the business problem, not the technology.
    </p>
    <p class="quote">"Technology is only valuable when it helps people make better decisions."</p>
  </header>

  <section>
    <h2>How I present work</h2>
    <div class="flow">
      <span>Business Problem</span><span class="arrow">→</span>
      <span>Context &amp; Constraints</span><span class="arrow">→</span>
      <span>Solution Design</span><span class="arrow">→</span>
      <span>Technology Choices</span><span class="arrow">→</span>
      <span>Business Impact</span><span class="arrow">→</span>
      <span>Lessons Learned</span>
    </div>
    <p class="approach-note">
      Every project is told through a business-first lens, not a tech demo — how engineering,
      data, and AI come together to enable better decisions at scale.
    </p>
  </section>

  <section>
    <h2>Featured project</h2>
    <div class="card">
      <!-- SCREENSHOT: replace the placeholder below with a real image.
           1. Drop a file named "spice-vizcon.png" into the repo root.
           2. Delete the <div class="shot-placeholder">...</div> block.
           3. Uncomment the <img> line just below. -->
      <!-- <img class="shot" src="spice-vizcon.png" alt="spice-vizcon — world maps of where spices are grown vs. eaten" /> -->
      <div class="shot-placeholder">🌶️ Add a spice-vizcon screenshot here (a world map from the live app)</div>

      <div class="body">
        <h3><a href="https://github.com/balaji4aws/spice-vizcon" target="_blank" rel="noopener">🌶️ spice-vizcon — a data story you can trust</a></h3>
        <p>
          An interactive data product on 28 years of UN food data (45,000 rows, 198 countries):
          where the world's spices are <em>grown</em> vs. where they're <em>eaten</em> — they
          almost never match. The interesting part isn't the finding; it's the engineering that
          makes every number provably trustworthy.
        </p>
        <ul>
          <li><strong>One pipeline owns every number.</strong> The app only reads results — it never does its own maths, so the text and charts can't quietly disagree.</li>
          <li><strong>61 claims verified independently.</strong> A separate script recomputes every figure from raw data; CI fails the build if anything drifts.</li>
          <li><strong>An honest hallucination log</strong> — every judgement call, and where the analysis could be wrong.</li>
        </ul>
        <div class="btn-row">
          <a class="btn" href="https://spice-vizcon.streamlit.app" target="_blank" rel="noopener">▶️ Open the live app</a>
          <a class="btn secondary" href="https://github.com/balaji4aws/spice-vizcon" target="_blank" rel="noopener">View the code</a>
        </div>
        <div class="stack">
          <code>Python</code><code>Streamlit</code><code>pandas</code><code>Plotly</code><code>GitHub Actions CI</code>
        </div>
      </div>
    </div>
    <p class="approach-note" style="margin-top:18px;">More projects and write-ups landing here.</p>
  </section>

  <section>
    <h2>Focus areas</h2>
    <p class="focus">
      <b>Business Intelligence</b> · <b>Data Products</b> · <b>Decision Systems</b> ·
      AWS cloud engineering (Redshift, S3, Glue, QuickSight) · AI-enabled analytics ·
      B2B marketplace &amp; supply-chain analytics
    </p>
  </section>

  <section>
    <h2>Connect</h2>
    <div class="links">
      <a href="https://www.linkedin.com/in/balaji4aws" target="_blank" rel="noopener">💼 LinkedIn</a>
      <a href="https://github.com/balaji4aws" target="_blank" rel="noopener">💻 GitHub</a>
      <a href="mailto:balaji4aws@gmail.com">📧 Email</a>
    </div>
  </section>

  <footer>
    © 2026 Balaji Venkatesh · Built with plain HTML, hosted on GitHub Pages.
  </footer>

</div>
</body>
</html>
