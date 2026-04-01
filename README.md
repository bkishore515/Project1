<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Nexus | modern digital presence</title>
  <!-- Google Fonts + simple reset -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #fafcff;
      color: #111827;
      line-height: 1.5;
      scroll-behavior: smooth;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 32px;
    }

    /* header / nav */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 24px 0;
      flex-wrap: wrap;
      gap: 20px;
    }

    .logo {
      font-size: 28px;
      font-weight: 800;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #1E3C72, #2A5298);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      transition: 0.2s;
    }

    .nav-links {
      display: flex;
      gap: 32px;
      font-weight: 500;
    }

    .nav-links a {
      text-decoration: none;
      color: #1f2937;
      transition: color 0.2s;
      font-size: 1rem;
    }

    .nav-links a:hover {
      color: #2A5298;
    }

    .btn-outline {
      border: 1.5px solid #2A5298;
      background: transparent;
      padding: 8px 20px;
      border-radius: 40px;
      font-weight: 600;
      color: #2A5298;
      cursor: pointer;
      transition: all 0.2s;
      font-family: inherit;
    }

    .btn-outline:hover {
      background: #2A5298;
      color: white;
    }

    /* hero section */
    .hero {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 48px;
      padding: 60px 0 80px 0;
    }

    .hero-content {
      flex: 1;
      min-width: 280px;
    }

    .hero-badge {
      background: #eef2ff;
      color: #1e40af;
      padding: 6px 14px;
      border-radius: 40px;
      font-size: 0.85rem;
      font-weight: 600;
      display: inline-block;
      margin-bottom: 24px;
    }

    .hero-content h1 {
      font-size: 3.5rem;
      font-weight: 800;
      line-height: 1.2;
      letter-spacing: -0.02em;
      margin-bottom: 24px;
      color: #0a2540;
    }

    .hero-highlight {
      background: linear-gradient(120deg, #e0e7ff 0%, #e0e7ff 40%, transparent 70%);
      padding: 0 6px;
    }

    .hero-desc {
      font-size: 1.2rem;
      color: #4b5563;
      max-width: 540px;
      margin-bottom: 32px;
    }

    .btn-group {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
    }

    .btn-primary {
      background: #1e3a8a;
      color: white;
      border: none;
      padding: 12px 28px;
      border-radius: 40px;
      font-weight: 600;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.2s;
      box-shadow: 0 4px 8px rgba(0,0,0,0.05);
      font-family: inherit;
    }

    .btn-primary:hover {
      background: #0f2b6d;
      transform: translateY(-2px);
    }

    .btn-secondary {
      background: white;
      border: 1px solid #cbd5e1;
      padding: 12px 28px;
      border-radius: 40px;
      font-weight: 600;
      cursor: pointer;
      transition: 0.2s;
      font-family: inherit;
    }

    .btn-secondary:hover {
      border-color: #1e3a8a;
      background: #f8fafc;
    }

    .hero-image {
      flex: 1;
      background: linear-gradient(145deg, #eef2ff, #ffffff);
      border-radius: 48px;
      padding: 20px;
      text-align: center;
      box-shadow: 0 20px 35px -12px rgba(0,0,0,0.08);
    }

    .hero-image svg {
      max-width: 100%;
      height: auto;
    }

    /* features section */
    .section {
      padding: 80px 0;
    }

    .section-title {
      text-align: center;
      font-size: 2.2rem;
      font-weight: 700;
      margin-bottom: 16px;
      letter-spacing: -0.01em;
    }

    .section-sub {
      text-align: center;
      color: #5b6e8c;
      max-width: 680px;
      margin: 0 auto 56px auto;
      font-size: 1.1rem;
    }

    .features-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 32px;
      justify-content: center;
    }

    .feature-card {
      background: white;
      border-radius: 32px;
      padding: 32px 24px;
      flex: 1;
      min-width: 240px;
      max-width: 320px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.02), 0 2px 6px rgba(0,0,0,0.05);
      transition: all 0.25s ease;
      border: 1px solid #edf2f7;
    }

    .feature-card:hover {
      transform: translateY(-6px);
      border-color: #cddff7;
      box-shadow: 0 20px 30px -12px rgba(0,0,0,0.1);
    }

    .feature-icon {
      background: #eef3ff;
      width: 56px;
      height: 56px;
      border-radius: 24px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 24px;
    }

    .feature-card h3 {
      font-size: 1.5rem;
      font-weight: 700;
      margin-bottom: 12px;
    }

    .feature-card p {
      color: #4b5563;
      line-height: 1.5;
    }

    /* stats row */
    .stats-row {
      background: #0f172a;
      border-radius: 56px;
      padding: 48px 32px;
      margin: 40px 0;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 32px;
      color: white;
    }

    .stat-item {
      text-align: center;
      flex: 1;
    }

    .stat-number {
      font-size: 2.4rem;
      font-weight: 800;
    }

    .stat-label {
      color: #b9c7d9;
      margin-top: 8px;
    }

    /* cta */
    .cta-section {
      background: linear-gradient(115deg, #eef2ff 0%, #ffffff 100%);
      border-radius: 48px;
      padding: 64px 48px;
      text-align: center;
      margin: 40px 0 60px;
    }

    .cta-section h2 {
      font-size: 2rem;
      font-weight: 700;
      margin-bottom: 16px;
    }

    .cta-section p {
      font-size: 1.1rem;
      color: #2c3e66;
      max-width: 560px;
      margin: 0 auto 32px auto;
    }

    /* footer */
    footer {
      border-top: 1px solid #e2e8f0;
      padding: 48px 0 32px;
      margin-top: 40px;
    }

    .footer-content {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 24px;
    }

    .footer-links {
      display: flex;
      gap: 32px;
    }

    .footer-links a {
      text-decoration: none;
      color: #4b5563;
      transition: color 0.2s;
    }

    .footer-links a:hover {
      color: #1e3a8a;
    }

    .copyright {
      color: #6c757d;
      font-size: 0.85rem;
    }

    @media (max-width: 768px) {
      .container {
        padding: 0 24px;
      }
      .hero-content h1 {
        font-size: 2.4rem;
      }
      .navbar {
        flex-direction: column;
        align-items: flex-start;
      }
      .nav-links {
        flex-wrap: wrap;
        gap: 20px;
      }
      .hero {
        flex-direction: column;
      }
      .stats-row {
        flex-direction: column;
        text-align: center;
      }
      .cta-section {
        padding: 40px 24px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Navigation -->
    <nav class="navbar">
      <div class="logo">✦ NEXUS</div>
      <div class="nav-links">
        <a href="#">Home</a>
        <a href="#">Features</a>
        <a href="#">Solutions</a>
        <a href="#">Insights</a>
      </div>
      <button class="btn-outline" id="contactBtn">Contact us</button>
    </nav>

    <!-- Hero -->
    <div class="hero">
      <div class="hero-content">
        <span class="hero-badge">✨ AI-powered platform</span>
        <h1>Scale your vision<br>with <span class="hero-highlight">intelligent workflows</span></h1>
        <p class="hero-desc">Build, automate, and grow — Nexus brings next-gen collaboration and analytics into one unified workspace.</p>
        <div class="btn-group">
          <button class="btn-primary" id="getStartedBtn">Get started →</button>
          <button class="btn-secondary" id="demoBtn">Live demo</button>
        </div>
      </div>
      <div class="hero-image">
        <svg width="380" height="300" viewBox="0 0 400 320" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="40" y="40" width="320" height="240" rx="28" fill="url(#gradBg)" stroke="#CBD5E1" strokeWidth="1.5"/>
          <defs><linearGradient id="gradBg" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" stopColor="#F1F5F9"/><stop offset="100%" stopColor="#FFFFFF"/></linearGradient></defs>
          <circle cx="120" cy="110" r="18" fill="#2A5298" fill-opacity="0.15" stroke="#2A5298" strokeWidth="1.2"/>
          <circle cx="280" cy="190" r="22" fill="#1E3C72" fill-opacity="0.12" stroke="#1E3C72" strokeWidth="1.2"/>
          <path d="M150 160 L250 160 M200 120 L200 200" stroke="#1E3C72" strokeWidth="2" strokeLinecap="round" strokeDasharray="4 4"/>
          <rect x="180" y="80" width="40" height="40" rx="12" fill="#2A5298" fill-opacity="0.2" stroke="#2A5298" strokeWidth="1.2"/>
          <path d="M280 80 L320 80 M300 60 L300 100" stroke="#2A5298" strokeWidth="2" strokeLinecap="round"/>
          <path d="M70 240 L330 240" stroke="#94A3B8" strokeWidth="1.5" strokeDasharray="5 3"/>
        </svg>
      </div>
    </div>

    <!-- Features Section -->
    <div class="section" id="features">
      <div class="section-title">Designed for modern teams</div>
      <div class="section-sub">Everything you need to ship faster, stay aligned, and unlock insights.</div>
      <div class="features-grid">
        <div class="feature-card">
          <div class="feature-icon">⚡</div>
          <h3>Real-time sync</h3>
          <p>Collaborate across devices with instant updates and zero latency — always stay in flow.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">📊</div>
          <h3>Smart analytics</h3>
          <p>Turn data into decisions with AI-driven dashboards and predictive forecasting.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">🔒</div>
          <h3>Enterprise security</h3>
          <p>Bank-grade encryption, SSO, and granular roles to keep your assets protected.</p>
        </div>
      </div>
    </div>

    <!-- Stats Row (dynamic counters) -->
    <div class="stats-row" id="statsSection">
      <div class="stat-item">
        <div class="stat-number" id="stat1">0</div>
        <div class="stat-label">Active users</div>
      </div>
      <div class="stat-item">
        <div class="stat-number" id="stat2">0</div>
        <div class="stat-label">Tasks automated</div>
      </div>
      <div class="stat-item">
        <div class="stat-number" id="stat3">0</div>
        <div class="stat-label">Avg. efficiency ↑</div>
      </div>
    </div>

    <!-- CTA Section -->
    <div class="cta-section">
      <h2>Ready to accelerate your growth?</h2>
      <p>Join thousands of creators and businesses who trust Nexus to streamline operations.</p>
      <button class="btn-primary" id="ctaButton" style="background:#0f2b6d;">Start free trial →</button>
    </div>
  </div>
  
  <!-- Footer -->
  <footer>
    <div class="container">
      <div class="footer-content">
        <div class="logo" style="font-size: 22px;">✦ NEXUS</div>
        <div class="footer-links">
          <a href="#">About</a>
          <a href="#">Careers</a>
          <a href="#">Privacy</a>
          <a href="#">Terms</a>
        </div>
        <div class="copyright">© 2025 Nexus — built for the future</div>
      </div>
    </div>
  </footer>

  <!-- simple interactive JS: counters on scroll, alert modals for buttons -->
  <script>
    (function() {
      // Stats counters with intersection observer
      const statNumbers = {
        stat1: { element: document.getElementById('stat1'), current: 0, target: 12480, suffix: '+' },
        stat2: { element: document.getElementById('stat2'), current: 0, target: 35200, suffix: '+' },
        stat3: { element: document.getElementById('stat3'), current: 0, target: 47, suffix: '%' }
      };

      let animated = false;
      const statsContainer = document.getElementById('statsSection');

      function animateNumbers() {
        if (animated) return;
        animated = true;
        // animate each counter
        const duration = 1600; // ms
        const startTime = performance.now();
        
        function update(currentTime) {
          const elapsed = currentTime - startTime;
          const progress = Math.min(1, elapsed / duration);
          // ease out cubic
          const easeProgress = 1 - Math.pow(1 - progress, 3);
          
          for (let key in statNumbers) {
            const item = statNumbers[key];
            const targetVal = item.target;
            let val = Math.floor(easeProgress * targetVal);
            if (key === 'stat3') val = Math.floor(easeProgress * targetVal); // percent int
            if (progress >= 1) val = targetVal;
            let displayVal = val;
            if (key === 'stat3') displayVal = val;
            if (item.suffix) {
              item.element.innerText = displayVal + item.suffix;
            } else {
              item.element.innerText = displayVal.toLocaleString() + (item.suffix || '');
            }
          }
          
          if (progress < 1) {
            requestAnimationFrame(update);
          } else {
            // final precise values
            statNumbers.stat1.element.innerText = statNumbers.stat1.target.toLocaleString() + statNumbers.stat1.suffix;
            statNumbers.stat2.element.innerText = statNumbers.stat2.target.toLocaleString() + statNumbers.stat2.suffix;
            statNumbers.stat3.element.innerText = statNumbers.stat3.target + statNumbers.stat3.suffix;
          }
        }
        
        requestAnimationFrame(update);
      }

      // observer for stats
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting && !animated) {
            animateNumbers();
            observer.unobserve(statsContainer);
          }
        });
      }, { threshold: 0.3 });
      if (statsContainer) observer.observe(statsContainer);
      
      // button interactions: demo + get started + contact + cta
      const getStartedBtn = document.getElementById('getStartedBtn');
      const demoBtn = document.getElementById('demoBtn');
      const contactBtn = document.getElementById('contactBtn');
      const ctaButton = document.getElementById('ctaButton');
      
      function showMessage(action) {
        // create floating subtle toast (lightweight)
        const toast = document.createElement('div');
        toast.innerText = `✨ ${action} — welcome to the interactive experience!`;
        toast.style.position = 'fixed';
        toast.style.bottom = '24px';
        toast.style.left = '50%';
        toast.style.transform = 'translateX(-50%)';
        toast.style.backgroundColor = '#1f2937';
        toast.style.color = 'white';
        toast.style.padding = '12px 24px';
        toast.style.borderRadius = '48px';
        toast.style.fontSize = '0.9rem';
        toast.style.fontWeight = '500';
        toast.style.zIndex = '999';
        toast.style.boxShadow = '0 8px 20px rgba(0,0,0,0.2)';
        toast.style.backdropFilter = 'blur(4px)';
        toast.style.fontFamily = 'inherit';
        document.body.appendChild(toast);
        setTimeout(() => {
          toast.style.opacity = '0';
          toast.style.transition = 'opacity 0.3s';
          setTimeout(() => toast.remove(), 400);
        }, 2300);
      }
      
      if (getStartedBtn) {
        getStartedBtn.addEventListener('click', () => showMessage('🚀 Get started — explore Nexus features'));
      }
      if (demoBtn) {
        demoBtn.addEventListener('click', () => showMessage('🎥 Live demo: intelligent dashboard preview'));
      }
      if (contactBtn) {
        contactBtn.addEventListener('click', () => showMessage('📬 Thanks for reaching out! Our team will reply shortly.'));
      }
      if (ctaButton) {
        ctaButton.addEventListener('click', () => showMessage('🎉 14-day free trial activated (demo mode)'));
      }
      
      // optional: smooth nav highlight (fake but gives feel)
      const navLinks = document.querySelectorAll('.nav-links a');
      navLinks.forEach(link => {
        link.addEventListener('click', (e) => {
          e.preventDefault();
          const sectionId = link.getAttribute('href') === '#' ? 'features' : null;
          if (link.innerText === 'Features') {
            document.getElementById('features')?.scrollIntoView({ behavior: 'smooth' });
          } else if (link.innerText === 'Solutions' || link.innerText === 'Insights') {
            showMessage(`📌 ${link.innerText} section — more content coming soon`);
          } else if (link.innerText === 'Home') {
            window.scrollTo({ top: 0, behavior: 'smooth' });
          } else {
            showMessage(`✨ Navigate to ${link.innerText}`);
          }
        });
      });
      
      // Optional: preload counter if stats visible on load (just in case)
      if (statsContainer && window.IntersectionObserver) {
        // already observed
      } else if (statsContainer) {
        // fallback: trigger after short delay if no observer
        setTimeout(() => {
          const rect = statsContainer.getBoundingClientRect();
          if (rect.top < window.innerHeight - 100 && !animated) animateNumbers();
        }, 600);
      }
      
      // tiny interactive: style on hero button hover
      console.log('Website ready — Nexus UI');
    })();
  </script>
</body>
</html>
