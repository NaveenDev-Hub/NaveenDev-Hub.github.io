/* ── Design tokens ── */
:root {
  --bg: #06080f;
  --bg-elevated: #0c1019;
  --bg-card: rgba(14, 20, 35, 0.72);
  --border: rgba(255, 255, 255, 0.08);
  --border-strong: rgba(255, 255, 255, 0.14);
  --text: #e8ecf4;
  --muted: #8b95a8;
  --accent: #22d3ee;
  --accent-2: #818cf8;
  --accent-3: #a78bfa;
  --gradient: linear-gradient(135deg, #22d3ee 0%, #818cf8 50%, #c084fc 100%);
  --glow: 0 0 60px rgba(34, 211, 238, 0.15);
  --font-display: "Syne", system-ui, sans-serif;
  --font-body: "DM Sans", system-ui, sans-serif;
  --font-mono: "JetBrains Mono", ui-monospace, monospace;
  --nav-h: 4rem;
  --max-w: 1100px;
  --radius: 14px;
  --radius-sm: 8px;
  --ease: cubic-bezier(0.22, 1, 0.36, 1);
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html {
  scroll-behavior: smooth;
  scroll-padding-top: calc(var(--nav-h) + 1rem);
}

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-body);
  font-size: 1rem;
  line-height: 1.65;
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
}

/* Ambient background */
body::before {
  content: "";
  position: fixed;
  inset: 0;
  background:
    radial-gradient(ellipse 80% 50% at 50% -20%, rgba(34, 211, 238, 0.12), transparent),
    radial-gradient(ellipse 60% 40% at 100% 0%, rgba(129, 140, 248, 0.1), transparent),
    radial-gradient(ellipse 50% 30% at 0% 100%, rgba(167, 139, 250, 0.08), transparent);
  pointer-events: none;
  z-index: 0;
}

body::after {
  content: "";
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(rgba(255, 255, 255, 0.02) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.02) 1px, transparent 1px);
  background-size: 64px 64px;
  mask-image: radial-gradient(ellipse 70% 60% at 50% 30%, black, transparent);
  pointer-events: none;
  z-index: 0;
}

a { color: var(--accent); text-decoration: none; transition: color 0.2s; }
a:hover { color: #67e8f9; }

img { max-width: 100%; display: block; }

/* ── Layout shell ── */
.shell {
  position: relative;
  z-index: 1;
  max-width: var(--max-w);
  margin: 0 auto;
  padding: 0 1.5rem;
}

/* ── Navigation ── */
.nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: var(--nav-h);
  z-index: 100;
  border-bottom: 1px solid transparent;
  transition: background 0.3s var(--ease), border-color 0.3s, backdrop-filter 0.3s;
}

.nav.is-scrolled {
  background: rgba(6, 8, 15, 0.82);
  backdrop-filter: blur(16px);
  border-bottom-color: var(--border);
}

.nav__inner {
  max-width: var(--max-w);
  margin: 0 auto;
  padding: 0 1.5rem;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.nav__brand {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 1rem;
  letter-spacing: -0.02em;
  color: var(--text);
  white-space: nowrap;
}

.nav__brand span {
  background: var(--gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav__links {
  display: flex;
  align-items: center;
  gap: 0.25rem;
  list-style: none;
}

.nav__links a {
  color: var(--muted);
  font-size: 0.875rem;
  font-weight: 500;
  padding: 0.4rem 0.75rem;
  border-radius: var(--radius-sm);
  transition: color 0.2s, background 0.2s;
}

.nav__links a:hover,
.nav__links a.is-active {
  color: var(--text);
  background: rgba(255, 255, 255, 0.06);
  text-decoration: none;
}

.nav__cta {
  margin-left: 0.5rem;
  padding: 0.45rem 1rem !important;
  background: var(--gradient) !important;
  color: #06080f !important;
  font-weight: 600 !important;
  border-radius: 999px !important;
}

.nav__cta:hover {
  opacity: 0.92;
  color: #06080f !important;
  filter: brightness(1.05);
}

.nav__toggle {
  display: none;
  background: none;
  border: 1px solid var(--border);
  color: var(--text);
  width: 2.5rem;
  height: 2.5rem;
  border-radius: var(--radius-sm);
  cursor: pointer;
  font-size: 1.25rem;
}

/* ── Hero ── */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding: calc(var(--nav-h) + 3rem) 0 4rem;
}

.hero__badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.35rem 0.85rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: var(--bg-card);
  font-size: 0.8rem;
  color: var(--muted);
  margin-bottom: 1.5rem;
  backdrop-filter: blur(8px);
  animation: fadeUp 0.7s var(--ease) both;
}

.hero__badge-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #34d399;
  box-shadow: 0 0 12px rgba(52, 211, 153, 0.6);
  animation: pulse 2s ease infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}

.hero__title {
  font-family: var(--font-display);
  font-size: clamp(2.5rem, 8vw, 4.25rem);
  font-weight: 800;
  line-height: 1.05;
  letter-spacing: -0.03em;
  margin-bottom: 1rem;
  animation: fadeUp 0.7s 0.1s var(--ease) both;
}

.hero__title--stack {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.2em;
}

.hero__line {
  display: block;
}

.hero__line--primary {
  color: var(--text);
}

.hero__line--accent {
  font-size: 0.78em;
  font-weight: 700;
  letter-spacing: -0.02em;
  background: var(--gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero__title .gradient {
  background: var(--gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero__subtitle {
  font-size: clamp(1.05rem, 2.5vw, 1.35rem);
  color: var(--muted);
  max-width: 36rem;
  margin-bottom: 2rem;
  animation: fadeUp 0.7s 0.2s var(--ease) both;
}

.hero__subtitle strong {
  color: var(--text);
  font-weight: 600;
}

.hero__actions {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
  margin-bottom: 3rem;
  animation: fadeUp 0.7s 0.3s var(--ease) both;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.35rem;
  border-radius: 999px;
  font-size: 0.9rem;
  font-weight: 600;
  border: 1px solid transparent;
  cursor: pointer;
  transition: transform 0.2s var(--ease), box-shadow 0.2s, background 0.2s;
  font-family: inherit;
}

.btn:hover { transform: translateY(-2px); text-decoration: none; }

.btn--primary {
  background: var(--gradient);
  color: #06080f;
  box-shadow: var(--glow);
}

.btn--primary:hover { color: #06080f; filter: brightness(1.06); }

.btn--ghost {
  background: rgba(255, 255, 255, 0.04);
  border-color: var(--border-strong);
  color: var(--text);
}

.btn--ghost:hover {
  background: rgba(255, 255, 255, 0.08);
  color: var(--text);
}

/* Stats */
.stats {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  animation: fadeUp 0.7s 0.4s var(--ease) both;
}

.stat {
  padding: 1.25rem 1rem;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--bg-card);
  backdrop-filter: blur(12px);
  text-align: center;
  transition: border-color 0.25s, transform 0.25s var(--ease);
}

.stat:hover {
  border-color: rgba(34, 211, 238, 0.25);
  transform: translateY(-3px);
}

.stat__value {
  font-family: var(--font-display);
  font-size: 1.75rem;
  font-weight: 800;
  background: var(--gradient);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  line-height: 1.2;
}

.stat__label {
  font-size: 0.75rem;
  color: var(--muted);
  margin-top: 0.25rem;
  text-transform: uppercase;
  letter-spacing: 0.06em;
}

/* ── Sections ── */
.section {
  padding: 5rem 0;
}

.section__header {
  margin-bottom: 2.5rem;
}

.section__eyebrow {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--accent);
  margin-bottom: 0.5rem;
}

.section__title {
  font-family: var(--font-display);
  font-size: clamp(1.75rem, 4vw, 2.25rem);
  font-weight: 700;
  letter-spacing: -0.02em;
}

.section__desc {
  color: var(--muted);
  margin-top: 0.5rem;
  max-width: 42rem;
}

/* Reveal animation */
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.6s var(--ease), transform 0.6s var(--ease);
}

.reveal.is-visible {
  opacity: 1;
  transform: translateY(0);
}

/* About card */
.about-card {
  padding: 2rem;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--bg-card);
  backdrop-filter: blur(12px);
  font-size: 1.05rem;
  line-height: 1.75;
  color: var(--muted);
}

.about-card strong { color: var(--text); }

/* Timeline */
.timeline {
  position: relative;
  padding-left: 1.5rem;
}

.timeline::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0.5rem;
  bottom: 0.5rem;
  width: 2px;
  background: linear-gradient(180deg, var(--accent), var(--accent-3), transparent);
  border-radius: 2px;
}

.timeline__item {
  position: relative;
  padding-bottom: 2.5rem;
}

.timeline__item:last-child { padding-bottom: 0; }

.timeline__item::before {
  content: "";
  position: absolute;
  left: -1.5rem;
  top: 0.55rem;
  width: 10px;
  height: 10px;
  margin-left: -4px;
  border-radius: 50%;
  background: var(--bg);
  border: 2px solid var(--accent);
  box-shadow: 0 0 12px rgba(34, 211, 238, 0.4);
}

.job-card {
  padding: 1.75rem;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--bg-card);
  backdrop-filter: blur(12px);
  transition: border-color 0.25s, box-shadow 0.25s;
}

.job-card:hover {
  border-color: rgba(129, 140, 248, 0.3);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.25);
}

.job-card__role {
  font-family: var(--font-display);
  font-size: 1.2rem;
  font-weight: 700;
  margin-bottom: 0.35rem;
}

.job-card__company {
  color: var(--accent-2);
  font-weight: 500;
  font-size: 0.95rem;
}

.job-card__meta {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--muted);
  margin: 0.5rem 0 1rem;
}

.job-card__project {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--text);
  margin-bottom: 0.75rem;
}

.job-card p {
  color: var(--muted);
  font-size: 0.925rem;
  margin-bottom: 0.75rem;
}

.job-card p:last-child { margin-bottom: 0; }

/* Skills */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1.25rem;
}

.skill-group {
  padding: 1.5rem;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--bg-card);
  backdrop-filter: blur(12px);
}

.skill-group__title {
  font-family: var(--font-mono);
  font-size: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--accent);
  margin-bottom: 1rem;
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
}

.skill-tag {
  font-size: 0.8rem;
  padding: 0.3rem 0.65rem;
  border-radius: 6px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid var(--border);
  color: var(--text);
}

/* Cert & education cards */
.cards-row {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1rem;
}

.mini-card {
  padding: 1.5rem;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--bg-card);
  backdrop-filter: blur(12px);
}

.mini-card__title {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 1rem;
  margin-bottom: 0.35rem;
}

.mini-card__sub {
  color: var(--accent-2);
  font-size: 0.9rem;
}

.mini-card__meta {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--muted);
  margin-top: 0.5rem;
}

/* Footer */
.footer {
  border-top: 1px solid var(--border);
  padding: 3rem 0 2rem;
  margin-top: 2rem;
}

.footer__grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer__brand {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
}

.footer__tagline {
  color: var(--muted);
  font-size: 0.9rem;
}

.footer__heading {
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--muted);
  margin-bottom: 0.75rem;
}

.footer ul { list-style: none; }

.footer li {
  margin-bottom: 0.4rem;
  font-size: 0.9rem;
}

.footer li a { color: var(--muted); }
.footer li a:hover { color: var(--accent); }

.footer__copy {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--muted);
  padding-top: 1.5rem;
  border-top: 1px solid var(--border);
}

.footer--simple {
  margin-top: 3rem;
  padding: 2rem 0;
}

.footer--simple .footer__copy {
  border-top: none;
  padding-top: 1rem;
  margin-top: 0;
}

.footer--simple .profile-links {
  margin-top: 0;
}

/* About page (krasserm-style) */
.about-page {
  padding: calc(var(--nav-h) + 2.5rem) 0 2rem;
  max-width: var(--max-w);
}

.about-page__title {
  font-family: var(--font-display);
  font-size: clamp(2rem, 5vw, 2.5rem);
  font-weight: 300;
  letter-spacing: -0.03em;
  color: var(--text);
  margin-bottom: 1.25rem;
}

.about-page__bio {
  color: var(--text);
  font-size: 1rem;
  line-height: 1.75;
  margin-bottom: 1.5rem;
  max-width: 42rem;
}

.profile-links {
  list-style: disc;
  padding-left: 1.35rem;
  margin: 0;
}

.profile-links li {
  font-size: 0.95rem;
  color: var(--muted);
  line-height: 1.85;
}

.profile-links li::marker {
  color: var(--muted);
}

.profile-links a {
  color: var(--accent);
  text-decoration: none;
}

.profile-links a:hover {
  text-decoration: underline;
}

/* Contact page */
.page-hero {
  padding: calc(var(--nav-h) + 4rem) 0 2rem;
}

.page-hero h1 {
  font-family: var(--font-display);
  font-size: clamp(2rem, 5vw, 2.75rem);
  font-weight: 800;
  letter-spacing: -0.02em;
  margin-bottom: 0.5rem;
}

.page-hero p {
  color: var(--muted);
  max-width: 32rem;
}

.contact-layout {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 2.5rem;
  padding-bottom: 4rem;
  align-items: start;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.contact-chip {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.25rem;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--bg-card);
}

.contact-chip__icon {
  width: 2.5rem;
  height: 2.5rem;
  border-radius: var(--radius-sm);
  background: rgba(34, 211, 238, 0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.1rem;
}

.contact-chip__label {
  font-size: 0.75rem;
  color: var(--muted);
  text-transform: uppercase;
  letter-spacing: 0.06em;
}

.contact-chip__value {
  font-weight: 600;
  font-size: 0.95rem;
}

.contact-form-wrap {
  padding: 2rem;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--bg-card);
  backdrop-filter: blur(12px);
}

.form-group { margin-bottom: 1.25rem; }

.form-group label {
  display: block;
  font-size: 0.8rem;
  font-weight: 500;
  color: var(--muted);
  margin-bottom: 0.4rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.form-group input,
.form-group textarea {
  width: 100%;
  background: rgba(0, 0, 0, 0.25);
  color: var(--text);
  border: 1px solid var(--border-strong);
  border-radius: var(--radius-sm);
  padding: 0.75rem 1rem;
  font-family: var(--font-body);
  font-size: 0.95rem;
  outline: none;
  transition: border-color 0.2s, box-shadow 0.2s;
}

.form-group input:focus,
.form-group textarea:focus {
  border-color: var(--accent);
  box-shadow: 0 0 0 3px rgba(34, 211, 238, 0.12);
}

.form-group textarea {
  resize: vertical;
  min-height: 140px;
}

.form-msg {
  display: none;
  margin-top: 1rem;
  font-size: 0.9rem;
  padding: 0.75rem 1rem;
  border-radius: var(--radius-sm);
}

.form-msg.success {
  background: rgba(52, 211, 153, 0.1);
  border: 1px solid rgba(52, 211, 153, 0.3);
  color: #34d399;
}

.form-msg.error {
  background: rgba(248, 113, 113, 0.1);
  border: 1px solid rgba(248, 113, 113, 0.3);
  color: #f87171;
}

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsive */
@media (max-width: 900px) {
  .stats { grid-template-columns: repeat(2, 1fr); }
  .footer__grid { grid-template-columns: 1fr 1fr; }
  .contact-layout { grid-template-columns: 1fr; }
}

@media (max-width: 640px) {
  .nav__toggle { display: flex; align-items: center; justify-content: center; }

  .nav__links {
    position: fixed;
    top: var(--nav-h);
    left: 0;
    right: 0;
    flex-direction: column;
    padding: 1rem;
    background: rgba(6, 8, 15, 0.96);
    backdrop-filter: blur(16px);
    border-bottom: 1px solid var(--border);
    transform: translateY(-120%);
    opacity: 0;
    pointer-events: none;
    transition: transform 0.3s var(--ease), opacity 0.3s;
  }

  .nav__links.is-open {
    transform: translateY(0);
    opacity: 1;
    pointer-events: auto;
  }

  .nav__links a { width: 100%; text-align: center; padding: 0.75rem; }

  .nav__cta { margin-left: 0 !important; }

  .stats { grid-template-columns: 1fr 1fr; }
  .footer__grid { grid-template-columns: 1fr; }
}
