// Serene Hospice LLC — Site Animations
(function () {
  function init() {
    injectStyles();
    setupHeroParallax();
    setupScrollReveal();
    setupHeaderFx();
    setupButtonBounce();
    setupHeroEntrance();
    setupMobileNav();
    setupResponsive();
  }

  // ── RESPONSIVE JS (overrides React inline styles directly) ──────────────
  function setupResponsive() {
    function apply() {
      var w = window.innerWidth;
      document.querySelectorAll('.sh-grid-4').forEach(function(el) {
        el.style.gridTemplateColumns = w <= 600 ? '1fr' : w <= 900 ? '1fr 1fr' : '';
        el.style.gap = w <= 900 ? '14px' : '';
      });
      document.querySelectorAll('.sh-grid-3').forEach(function(el) {
        el.style.gridTemplateColumns = w <= 600 ? '1fr' : w <= 900 ? '1fr 1fr' : '';
        el.style.gap = w <= 900 ? '14px' : '';
      });
      document.querySelectorAll('.sh-grid-2').forEach(function(el) {
        el.style.gridTemplateColumns = w <= 600 ? '1fr' : '';
        el.style.gap = w <= 600 ? '14px' : '';
      });
      document.querySelectorAll('.sh-footer-grid').forEach(function(el) {
        el.style.gridTemplateColumns = w <= 600 ? '1fr' : w <= 900 ? '1fr 1fr' : '';
        el.style.gap = w <= 900 ? '20px' : '';
      });
      document.querySelectorAll('.sh-flex-row, .flex-col-mobile, .hero-flex').forEach(function(el) {
        el.style.flexDirection = w <= 900 ? 'column' : '';
        el.style.gap = w <= 900 ? '24px' : '';
      });
      document.querySelectorAll('.sh-fixed-col, .hero-card, .full-width-mobile').forEach(function(el) {
        el.style.flex = w <= 900 ? 'none' : '';
        el.style.width = w <= 900 ? '100%' : '';
        el.style.maxWidth = w <= 900 ? '100%' : '';
      });
      document.querySelectorAll('section, footer').forEach(function(el) {
        el.style.paddingLeft = w <= 900 ? '20px' : '';
        el.style.paddingRight = w <= 900 ? '20px' : '';
      });
      document.querySelectorAll('h1').forEach(function(el) {
        if (!el.closest('header')) el.style.fontSize = w <= 600 ? '28px' : w <= 900 ? '32px' : '';
      });
      document.querySelectorAll('h2').forEach(function(el) {
        el.style.fontSize = w <= 600 ? '22px' : w <= 900 ? '26px' : '';
      });
      var nav = document.querySelector('header nav');
      var cta = document.querySelector('.header-cta');
      var btn = document.querySelector('.mobile-menu-btn');
      if (nav) nav.style.display = w <= 900 ? 'none' : '';
      if (cta) cta.style.display = w <= 900 ? 'none' : '';
      if (btn) btn.style.display = w <= 900 ? 'flex' : 'none';
    }

    // Retry until elements exist (DC renders async)
    function tryApply(attempts) {
      var grids = document.querySelectorAll('.sh-grid-4, .sh-grid-3, .sh-grid-2, .sh-flex-row, .hero-flex');
      if (grids.length === 0 && attempts > 0) {
        setTimeout(function(){ tryApply(attempts - 1); }, 200);
        return;
      }
      apply();
      window.addEventListener('resize', apply);
    }
    tryApply(20);
  }

  // ── MOBILE NAV ────────────────────────────────────────────────────────────
  function setupMobileNav() {
    // Single capture-phase delegated handler. Capture phase fires before any
    // bubble-phase stopPropagation in the framework, and delegation means it
    // works no matter when React mounts the button. No direct/bubble listeners
    // (those caused a double-toggle that cancelled the open).
    if (window.__shNavBound) return;
    window.__shNavBound = true;
    document.addEventListener('click', function(e) {
      var el = e.target, btn = null;
      while (el && el.nodeType === 1) {
        if (el.classList && el.classList.contains('mobile-menu-btn')) { btn = el; break; }
        el = el.parentElement;
      }
      var nav = document.getElementById('mobileNav');
      if (!nav) return;
      if (btn) { nav.classList.toggle('open'); return; }
      // Clicking a link inside the nav, or anywhere outside it, closes it
      if (nav.classList.contains('open')) {
        if (!nav.contains(e.target) || e.target.closest('a')) nav.classList.remove('open');
      }
    }, true);
  }

  // ── STYLES ────────────────────────────────────────────────────────────────
  function injectStyles() {
    const s = document.createElement('style');
    s.textContent = `
      /* ---- Scroll-reveal states ---- */
      .sh-reveal {
        opacity: 0;
        transform: translateY(36px);
        transition: opacity 0.65s cubic-bezier(.22,1,.36,1), transform 0.65s cubic-bezier(.22,1,.36,1);
      }
      .sh-reveal-left {
        opacity: 0;
        transform: translateX(-36px);
        transition: opacity 0.65s cubic-bezier(.22,1,.36,1), transform 0.65s cubic-bezier(.22,1,.36,1);
      }
      .sh-reveal-right {
        opacity: 0;
        transform: translateX(36px);
        transition: opacity 0.65s cubic-bezier(.22,1,.36,1), transform 0.65s cubic-bezier(.22,1,.36,1);
      }
      .sh-visible { opacity: 1 !important; transform: none !important; }

      /* ---- Card lift ---- */
      a[style*="border-radius:22px"],
      a[style*="border-radius:20px"],
      a[style*="border-radius:18px"],
      div[style*="border-radius:22px"]:not(header):not(footer),
      div[style*="border-radius:20px"]:not(header):not(footer) {
        transition: transform 0.28s cubic-bezier(.22,1,.36,1),
                    box-shadow 0.28s cubic-bezier(.22,1,.36,1) !important;
        will-change: transform;
      }
      a[style*="border-radius:22px"]:hover,
      a[style*="border-radius:20px"]:hover,
      a[style*="border-radius:18px"]:hover {
        transform: translateY(-6px) !important;
        box-shadow: 0 20px 50px rgba(149,117,205,0.22) !important;
      }

      /* ---- Buttons handled via .sh-btn class in setupButtonBounce ---- */

      /* ---- Photo zoom ---- */
      [style*="overflow:hidden"] img {
        transition: transform 0.55s cubic-bezier(.22,1,.36,1) !important;
      }
      [style*="overflow:hidden"]:hover img {
        transform: scale(1.07) !important;
      }

      /* ---- Nav links ---- */
      nav a {
        transition: color 0.2s ease, border-color 0.2s ease !important;
      }

      /* ---- Header logo ---- */
      header img {
        transition: transform 0.25s ease !important;
      }
      header a:hover img {
        transform: scale(1.06) !important;
      }

      /* ---- Icon boxes ---- */
      div[style*="border-radius:16px"],
      div[style*="border-radius:14px"] {
        transition: transform 0.25s ease !important;
      }
      a:hover div[style*="border-radius:16px"],
      a:hover div[style*="border-radius:14px"] {
        transform: rotate(-6deg) scale(1.15) !important;
      }

      /* ---- Stat numbers ---- */
      .sh-stat {
        display: inline-block;
        transition: transform 0.3s ease;
      }
      .sh-stat:hover { transform: scale(1.12); }

      /* ---- Parallax hero blobs ---- */
      .sh-blob { will-change: transform; }

      /* ---- Photo caption overlay ---- */
      [style*="position:absolute"][style*="bottom:0"] {
        transition: padding 0.3s ease;
      }
      [style*="overflow:hidden"]:hover [style*="position:absolute"][style*="bottom:0"] {
        padding-bottom: 32px !important;
      }

      /* ---- Footer links ---- */
      footer a {
        transition: color 0.2s ease, letter-spacing 0.2s ease !important;
      }
      footer a:hover { color: white !important; letter-spacing: 0.5px; }
    `;
    document.head.appendChild(s);
  }

  // ── HERO PARALLAX ─────────────────────────────────────────────────────────
  function setupHeroParallax() {
    const hero = document.querySelector('section');
    if (!hero) return;

    // Tag blobs
    hero.querySelectorAll('[style*="border-radius:50%"]').forEach((b, i) => {
      b.classList.add('sh-blob');
      b._shSpeed = i % 2 === 0 ? 0.18 : -0.12;
    });

    // Tag hero content for mild shift
    const heroContent = hero.querySelector('[style*="max-width:1200px"]');
    if (heroContent) heroContent.style.willChange = 'transform';

    window.addEventListener('scroll', function () {
      const y = window.scrollY;
      if (y > window.innerHeight) return;

      // Background parallax
      hero.style.backgroundPositionY = (y * 0.35) + 'px';

      // Blob parallax
      hero.querySelectorAll('.sh-blob').forEach(b => {
        b.style.transform = `translateY(${y * b._shSpeed}px)`;
      });

      // Hero content gentle float up
      if (heroContent) {
        heroContent.style.transform = `translateY(${y * 0.08}px)`;
      }
    }, { passive: true });
  }

  // ── SCROLL REVEAL ─────────────────────────────────────────────────────────
  function setupScrollReveal() {
    // Skip first section (hero)
    const sections = Array.from(document.querySelectorAll('section')).slice(1);

    sections.forEach(sec => {
      // Headings
      sec.querySelectorAll('h2').forEach(h => tag(h, 'reveal'));

      // Grid children — stagger them
      sec.querySelectorAll('[style*="grid-template-columns"]').forEach(grid => {
        Array.from(grid.children).forEach((child, i) => {
          tag(child, 'reveal');
          child.style.transitionDelay = (i * 80) + 'ms';
        });
      });

      // Side-by-side flex panels
      sec.querySelectorAll('[style*="gap:64px"],[style*="gap:72px"],[style*="gap:80px"]').forEach(row => {
        const kids = Array.from(row.children).filter(k => k.tagName !== 'SCRIPT');
        if (kids[0]) tag(kids[0], 'reveal-left');
        if (kids[1]) tag(kids[1], 'reveal-right');
      });
    });

    // Footer
    const footer = document.querySelector('footer');
    if (footer) tag(footer, 'reveal');

    // Observer
    const io = new IntersectionObserver(entries => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.add('sh-visible');
          io.unobserve(e.target);
        }
      });
    }, { threshold: 0.12 });

    document.querySelectorAll('.sh-reveal, .sh-reveal-left, .sh-reveal-right').forEach(el => io.observe(el));
  }

  // ── HERO ENTRANCE ANIMATIONS ──────────────────────────────────────────────
  function setupHeroEntrance() {
    const s = document.createElement('style');
    s.textContent = `
      @keyframes shFadeUp   { from { transform:translateY(24px); } to { transform:translateY(0); } }
      @keyframes shFadeRight{ from { transform:translateX(28px); } to { transform:translateX(0); } }
      @keyframes shFadeIn   { from { transform:translateY(12px); } to { transform:translateY(0); } }
      @keyframes shScaleIn  { from { transform:scale(0.94); } to { transform:scale(1); } }
      .sh-hero-badge  { animation: shFadeUp   0.6s  0.1s  cubic-bezier(.22,1,.36,1) both; }
      .sh-hero-h1     { animation: shFadeUp   0.7s  0.25s cubic-bezier(.22,1,.36,1) both; }
      .sh-hero-p      { animation: shFadeUp   0.7s  0.42s cubic-bezier(.22,1,.36,1) both; }
      .sh-hero-btns   { animation: shFadeUp   0.6s  0.58s cubic-bezier(.22,1,.36,1) both; }
      .sh-hero-stats  { animation: shFadeIn   0.7s  0.75s ease both; }
      .sh-hero-card   { animation: shFadeRight 0.75s 0.35s cubic-bezier(.22,1,.36,1) both; }
    `;
    document.head.appendChild(s);

    // Tag hero elements
    const hero = document.querySelector('section');
    if (!hero) return;

    // Badge (first inline-flex inside left col)
    const badge = hero.querySelector('div[style*="inline-flex"]');
    if (badge) badge.classList.add('sh-hero-badge');

    // H1
    const h1 = hero.querySelector('h1');
    if (h1) h1.classList.add('sh-hero-h1');

    // First p tag in hero
    const p = hero.querySelector('p');
    if (p) p.classList.add('sh-hero-p');

    // Buttons row
    const btnRow = hero.querySelector('div[style*="gap:16px"][style*="flex-wrap"]');
    if (btnRow) btnRow.classList.add('sh-hero-btns');

    // Stats row
    const statsRow = hero.querySelector('div[style*="gap:36px"]');
    if (statsRow) statsRow.classList.add('sh-hero-stats');

    // Right card (second flex child)
    const heroFlex = hero.querySelector('div[style*="max-width:1200px"]');
    if (heroFlex && heroFlex.children[1]) heroFlex.children[1].classList.add('sh-hero-card');

    // Safety net: CSS entrance animations can get stuck at opacity:0 when the
    // framework re-renders mid-animation (esp. in the bundled build). Force the
    // hero content visible once the entrance window has passed, and again on a
    // later tick in case a late re-render resets it.
    function forceHeroVisible() {
      ['.sh-hero-badge','.sh-hero-h1','.sh-hero-p','.sh-hero-btns','.sh-hero-stats','.sh-hero-card']
        .forEach(function(sel){
          hero.querySelectorAll(sel).forEach(function(el){
            el.style.animation = 'none';
            el.style.opacity = '1';
            el.style.transform = 'none';
          });
        });
    }
    setTimeout(forceHeroVisible, 1600);
    setTimeout(forceHeroVisible, 3200);
  }

  function tag(el, type) {
    el.classList.add('sh-' + type);
  }

  // ── HEADER FX ─────────────────────────────────────────────────────────────
  function setupHeaderFx() {
    const header = document.querySelector('header');
    if (!header) return;

    // Scroll-aware header
    const headerStyle = document.createElement('style');
    headerStyle.textContent = `
      header {
        transition: box-shadow 0.3s ease, background 0.3s ease !important;
      }
      header.sh-scrolled {
        box-shadow: 0 4px 32px rgba(149,117,205,0.18) !important;
        background: rgba(255,255,255,1) !important;
      }

      /* Nav link pill hover */
      nav a {
        position: relative;
        padding: 6px 12px !important;
        border-radius: 8px;
        transition: color 0.2s ease, background 0.2s ease !important;
      }
      nav a::after {
        content: '';
        position: absolute;
        bottom: 2px; left: 12px; right: 12px;
        height: 2px;
        background: #9575CD;
        border-radius: 2px;
        transform: scaleX(0);
        transform-origin: center;
        transition: transform 0.25s cubic-bezier(.34,1.56,.64,1);
      }
      nav a:hover {
        background: rgba(149,117,205,0.08) !important;
        color: #6B3AAE !important;
      }
      nav a:hover::after { transform: scaleX(1); }
      nav a[style*="border-bottom:2px solid #"]::after { transform: scaleX(1); }

      /* Logo spin on load */
      @keyframes logoLoad {
        from { opacity: 0; transform: scale(0.85) rotate(-4deg); }
        to   { opacity: 1; transform: scale(1) rotate(0deg); }
      }
      header img.sh-logo-loaded {
        animation: logoLoad 0.55s cubic-bezier(.34,1.56,.64,1) both;
      }
      header img {
        transition: transform 0.25s cubic-bezier(.34,1.56,.64,1) !important;
      }
      header a:first-child:hover img {
        transform: scale(1.08) rotate(-3deg) !important;
      }
    `;
    document.head.appendChild(headerStyle);

    // Scroll listener for header
    window.addEventListener('scroll', () => {
      if (window.scrollY > 20) {
        header.classList.add('sh-scrolled');
      } else {
        header.classList.remove('sh-scrolled');
      }
    }, { passive: true });

    // Animate logo on load
    const logo = header.querySelector('img');
    if (logo) setTimeout(() => logo.classList.add('sh-logo-loaded'), 100);
  }
  function setupButtonBounce() {
    // Add bounce CSS class
    const s = document.createElement('style');
    s.textContent = `
      .sh-btn {
        transition: transform 0.22s cubic-bezier(.34,1.56,.64,1),
                    box-shadow 0.22s ease,
                    filter 0.22s ease !important;
        will-change: transform;
        cursor: pointer;
        display: inline-flex;
      }
      .sh-btn:hover {
        transform: translateY(-7px) scale(1.08) !important;
        box-shadow: 0 20px 44px rgba(149,117,205,0.5) !important;
        filter: brightness(1.08) !important;
      }
      .sh-btn:active {
        transform: translateY(-2px) scale(1.02) !important;
        box-shadow: 0 8px 18px rgba(149,117,205,0.3) !important;
        transition-duration: 0.08s !important;
      }
    `;
    document.head.appendChild(s);

    // Find all CTA-style anchor tags (have padding + background color)
    function tagButtons() {
      document.querySelectorAll('a').forEach(a => {
        const st = a.getAttribute('style') || '';
        const cs = getComputedStyle(a);
        const hasPadding = st.includes('padding:') || parseInt(cs.paddingTop) > 8;
        const hasBg = st.includes('background') && !st.includes('transparent');
        const hasRadius = st.includes('border-radius:50px') || st.includes('border-radius: 50px');
        if ((hasPadding && hasBg) || hasRadius) {
          a.classList.add('sh-btn');
        }
      });
    }

    tagButtons();
    // Re-run after a tick in case DC hasn't fully rendered
    setTimeout(tagButtons, 400);
    setTimeout(tagButtons, 1200);
  }

  // ── INIT ──────────────────────────────────────────────────────────────────
  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', init);
  } else {
    init();
  }
})();
