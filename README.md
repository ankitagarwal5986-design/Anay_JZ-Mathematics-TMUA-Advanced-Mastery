<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JZ Mathematics • TMUA Mastery Workshop: Mock Set A Paper 1</title>

  <!-- MathJax Configuration & Loader -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)'], ['$', '$']],
        displayMath: [['\\[', '\\]'], ['$$', '$$']],
        processEscapes: true
      },
      svg: { fontCache: 'global' }
    };
  </script>
  <script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>

  <style>
    :root {
      --navy-dark: #0f172a;
      --brand-blue: #2563eb;
      --accent-cyan: #0284c7;
      --bg-tint: #f8fafc;
      --card-surf: #ffffff;
      --border-accent: #93c5fd;
      --border-soft: #cbd5e1;
      --green-ok: #059669;
      --green-surf: #d1fae5;
      --red-fail: #dc2626;
      --red-surf: #fee2e2;
      --brand-gold: #f59e0b;
      --gold-dark: #d97706;
      --gold-surf: #fef3c7;
      --text-main: #0f172a;
      --text-muted: #475569;

      /* High-Contrast Clear Light Yellow Options Palette */
      --opt-yellow-bg: #fefce8;
      --opt-yellow-border: #fef08a;
      --opt-yellow-hover: #fef9c3;
      --opt-yellow-active: #fde047;
      --opt-yellow-text: #713f12;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-tint);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 12px rgba(15, 23, 42, 0.2);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .brand-wrap {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .logo-badge {
      width: 44px;
      height: 44px;
      background: #ffffff;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.25);
    }

    .brand-title h1 {
      font-size: 1.15rem;
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .brand-title p {
      font-size: 0.78rem;
      color: #38bdf8;
      font-weight: 500;
    }

    .header-controls {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .chip {
      background: rgba(255, 255, 255, 0.12);
      border: 1px solid rgba(255, 255, 255, 0.25);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.88rem;
      color: #ffffff;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .chip strong {
      color: #ffffff;
      font-weight: 800;
      letter-spacing: 0.3px;
    }

    .btn-icon {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.3);
      color: #fff;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
    }

    nav {
      background: #ffffff;
      border-bottom: 1px solid var(--border-soft);
      display: flex;
      justify-content: center;
      gap: 8px;
      padding: 8px 16px;
    }

    nav button {
      background: none;
      border: none;
      outline: none;
      padding: 10px 20px;
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.2s;
    }

    nav button.active {
      background: #eff6ff;
      color: var(--brand-blue);
      border-bottom: 3px solid var(--brand-blue);
    }

    main {
      flex: 1;
      padding: 24px;
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
    }

    .view {
      display: none;
    }

    .view.active {
      display: block;
    }

    #loginGateView {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(15, 23, 42, 0.94);
      backdrop-filter: blur(6px);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .login-box {
      background: #fff;
      padding: 36px;
      border-radius: 16px;
      width: 100%;
      max-width: 480px;
      text-align: center;
      box-shadow: 0 14px 35px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      font-size: 1.45rem;
      color: var(--navy-dark);
      margin-bottom: 6px;
    }

    .login-box p {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-bottom: 20px;
      line-height: 1.5;
    }

    .resume-alert {
      display: none;
      background: #eff6ff;
      border: 1px solid var(--border-accent);
      border-radius: 8px;
      padding: 10px 14px;
      margin-bottom: 16px;
      font-size: 0.86rem;
      color: var(--navy-dark);
      text-align: left;
    }

    .login-box input {
      width: 100%;
      padding: 12px 16px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      font-size: 1rem;
      margin-bottom: 16px;
      outline: none;
    }

    .btn-primary {
      background: var(--brand-blue);
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
      width: 100%;
      transition: background 0.2s;
    }

    .btn-primary:hover {
      background: #1d4ed8;
    }

    .btn-secondary {
      background: transparent;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 9px 18px;
      font-size: 0.88rem;
      font-weight: 600;
      border-radius: 6px;
      cursor: pointer;
      width: 100%;
      margin-top: 10px;
    }

    .btn-secondary:hover {
      background: var(--bg-tint);
    }

    .theory-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      margin-bottom: 24px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.02);
    }

    .theory-card h3 {
      color: var(--navy-dark);
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 1.25rem;
    }

    .theory-intro-text {
      color: var(--text-main);
      line-height: 1.65;
      margin-bottom: 18px;
      font-size: 0.95rem;
    }

    .compendium-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      margin: 16px 0;
    }

    .comp-card {
      background: #ffffff;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      padding: 18px;
      display: flex;
      flex-direction: column;
      box-shadow: 0 2px 6px rgba(15, 23, 42, 0.04);
    }

    .comp-card h4 {
      color: var(--navy-dark);
      border-bottom: 2px solid var(--border-soft);
      padding-bottom: 8px;
      margin-bottom: 12px;
      font-size: 1.05rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .recap-body {
      font-size: 0.92rem;
      line-height: 1.65;
      color: var(--text-main);
    }

    .formula-box {
      background: #f8fafc;
      border-left: 4px solid var(--brand-blue);
      border-radius: 0 6px 6px 0;
      padding: 10px 14px;
      margin-top: 10px;
    }

    .sheet-grid {
      display: grid;
      grid-template-columns: 1fr 340px;
      gap: 24px;
    }

    @media (max-width: 990px) {
      .sheet-grid {
        grid-template-columns: 1fr;
      }
    }

    .question-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 26px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .concept-tag {
      display: inline-block;
      padding: 4px 10px;
      border-radius: 14px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      margin-bottom: 8px;
      background: #e0f2fe;
      color: #0369a1;
      border: 1px solid #7dd3fc;
    }

    .mcq-container {
      display: grid;
      grid-template-columns: 1fr;
      gap: 12px;
      margin: 20px 0;
    }

    /* Light Yellow Clear Options */
    .mcq-option-btn {
      background: var(--opt-yellow-bg);
      border: 2px solid var(--opt-yellow-border);
      border-radius: 10px;
      padding: 14px 18px;
      text-align: left;
      font-size: 0.98rem;
      color: var(--opt-yellow-text);
      cursor: pointer;
      transition: all 0.15s ease;
      display: flex;
      align-items: center;
      gap: 14px;
      box-shadow: 0 2px 5px rgba(254, 240, 138, 0.25);
    }

    .mcq-option-btn:hover:not(:disabled) {
      background: var(--opt-yellow-hover);
      border-color: var(--opt-yellow-active);
      transform: translateY(-1px);
    }

    .mcq-option-btn.selected-correct {
      background: var(--green-surf) !important;
      border-color: var(--green-ok) !important;
      color: var(--green-ok) !important;
      font-weight: 700;
      box-shadow: none;
    }

    .mcq-option-btn.selected-wrong {
      background: var(--red-surf) !important;
      border-color: var(--red-fail) !important;
      color: var(--red-fail) !important;
      box-shadow: none;
    }

    .opt-letter {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 32px;
      height: 32px;
      border-radius: 50%;
      background: #ffffff;
      border: 2px solid var(--opt-yellow-active);
      font-weight: 800;
      color: var(--opt-yellow-text);
      flex-shrink: 0;
    }

    .attempts-badge {
      font-size: 0.8rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 12px;
      background: #f1f5f9;
      color: #64748b;
      margin-left: 6px;
    }

    .btn-reveal {
      background: var(--brand-gold);
      color: #fff;
      border: none;
      padding: 6px 14px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      margin-left: 8px;
    }

    .btn-reveal:hover {
      background: var(--gold-dark);
    }

    .feedback-box {
      margin-top: 16px;
      padding: 16px;
      border-radius: 8px;
      font-size: 0.95rem;
      line-height: 1.65;
      display: block;
      animation: fadeIn 0.25s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(4px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .feedback-box.correct {
      background: #ecfdf5;
      border-left: 5px solid var(--green-ok);
      color: #065f46;
    }

    .feedback-box.incorrect {
      background: #fef2f2;
      border-left: 5px solid var(--red-fail);
      color: #991b1b;
    }

    .svg-container {
      display: flex;
      justify-content: center;
      margin: 16px 0;
      padding: 16px;
      background: var(--bg-tint);
      border-radius: 8px;
      border: 1px solid var(--border-soft);
      overflow-x: auto;
    }

    .nav-toolbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid var(--border-soft);
    }

    .nav-btn-group {
      display: flex;
      gap: 10px;
    }

    .btn-nav-action {
      background: #f8fafc;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 8px 18px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s;
    }

    .btn-nav-action:hover:not(:disabled) {
      background: var(--bg-tint);
      border-color: var(--brand-blue);
    }

    .btn-nav-action:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    .btn-skip {
      border-color: var(--brand-gold);
      color: var(--gold-dark);
      background: var(--gold-surf);
    }

    .btn-skip:hover {
      background: #fde68a;
    }

    .palette-box {
      background: #fff;
      border: 1px solid var(--border-soft);
      border-radius: 12px;
      padding: 16px;
      margin-bottom: 20px;
    }

    .palette-legend {
      display: flex;
      justify-content: space-between;
      font-size: 0.75rem;
      margin: 8px 0 12px 0;
      padding: 6px 8px;
      background: var(--bg-tint);
      border-radius: 6px;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 4px;
      font-weight: 600;
    }

    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
    }

    .palette-grid {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 6px;
      margin-bottom: 12px;
    }

    .palette-btn {
      aspect-ratio: 1;
      border: 1px solid var(--border-soft);
      background: var(--bg-tint);
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.15s;
      font-size: 0.85rem;
      color: var(--navy-dark);
    }

    .palette-btn.active {
      border: 2px solid var(--navy-dark) !important;
      background: #bfdbfe;
      color: #1e3a8a;
      font-weight: 800;
    }

    .palette-btn.completed {
      background: var(--green-ok) !important;
      color: #fff !important;
      border-color: var(--green-ok) !important;
    }

    .palette-btn.skipped {
      background: var(--brand-gold) !important;
      color: #fff !important;
      border-color: var(--gold-dark) !important;
    }

    .hero-score-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 28px;
      text-align: center;
      margin-bottom: 24px;
      box-shadow: 0 4px 14px rgba(0,0,0,0.03);
    }

    .student-badge {
      display: inline-block;
      background: var(--bg-tint);
      border: 1px solid var(--border-accent);
      padding: 6px 18px;
      border-radius: 20px;
      font-size: 1rem;
      margin-bottom: 14px;
      color: var(--navy-dark);
    }

    .student-badge strong {
      color: var(--brand-blue);
    }

    .score-badge {
      font-size: 3rem;
      font-weight: 800;
      color: var(--brand-blue);
      margin: 8px 0;
    }

    .progress-bar-wrap {
      width: 100%;
      height: 12px;
      background: #e2e8f0;
      border-radius: 6px;
      overflow: hidden;
      margin: 16px 0;
    }

    .progress-bar-fill {
      height: 100%;
      background: var(--green-ok);
      width: 0%;
      transition: width 0.3s ease;
    }

    .toast {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 20px;
      border-radius: 8px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.2);
      display: none;
      z-index: 1000;
    }

    @media print {
      header, nav, .palette-box, .btn-primary, #loginGateView, .nav-toolbar {
        display: none !important;
      }
      body { background: #fff; }
      main { width: 100%; max-width: 100%; padding: 0; }
      .sheet-grid { display: block; }
      .view { display: block !important; }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="brand-wrap">
      <div class="logo-badge">
        <svg width="34" height="34" viewBox="0 0 100 100" fill="none">
          <circle cx="50" cy="50" r="44" stroke="#2563eb" stroke-width="7"/>
          <path d="M 30 70 L 70 30" stroke="#0284c7" stroke-width="7" stroke-linecap="round"/>
          <path d="M 35 35 L 65 35 L 40 65 L 65 65" stroke="#f59e0b" stroke-width="6" fill="none" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <div class="brand-title">
        <h1>JZ Mathematics • TMUA Advanced Mastery</h1>
        <p>Mock Set A Paper 1 • Complete 20-Problem Interactive Learning Sheet</p>
      </div>
    </div>
    <div class="header-controls">
      <div class="chip" id="timerChip">⏱️ 00:00</div>
      <div class="chip" id="userPill"><strong>Candidate: Guest</strong></div>
      <button class="btn-icon" id="audioToggleBtn" title="Toggle Audio">🔊</button>
    </div>
  </header>

  <!-- Navigation Bar -->
  <nav>
    <button class="tab-btn active" id="tabPracticeBtn" onclick="switchView('practiceView')">✍️ Interactive Workstation</button>
    <button class="tab-btn" id="tabTheoryBtn" onclick="switchView('theoryView')">📖 TMUA Foundations &amp; Methods</button>
    <button class="tab-btn" id="tabResultsBtn" onclick="switchView('resultsView')">📋 Mark Scheme &amp; Full Derivations</button>
  </nav>

  <!-- Candidate Authentication Modal with Session Persistence -->
  <div id="loginGateView">
    <div class="login-box">
      <h2>JZ Mock Set A Paper 1 Portal</h2>
      <p>Test of Mathematics for University Admission • 20 Multiple-Choice Questions</p>
      
      <div id="resumeAlertBox" class="resume-alert">
        <strong>Saved Session Found!</strong><br>
        <span id="savedSessionDetails"></span>
      </div>

      <input type="text" id="studentNameInput" placeholder="Enter Candidate Name" />
      <button class="btn-primary" id="startSessionBtn" onclick="initDirectLogin(false)">Start Practice Session</button>
      <button class="btn-secondary" id="resumeSessionBtn" style="display:none;" onclick="initDirectLogin(true)">Resume Saved Progress</button>
    </div>
  </div>

  <main>
    <!-- View 1: Interactive Workstation (2 Attempts + Reveal Solution) -->
    <div id="practiceView" class="view active">
      <div class="sheet-grid">
        <div class="question-card" id="activeQuestionCard"></div>

        <aside>
          <div class="palette-box">
            <div style="display: flex; justify-content: space-between; align-items: center;">
              <h4>Abhyas Palette</h4>
              <span style="font-size:0.8rem; color:var(--text-muted);" id="paletteCount">0 / 20 Completed</span>
            </div>

            <div class="palette-legend">
              <div class="legend-item"><span class="legend-dot" style="background:var(--green-ok);"></span> Solved</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f59e0b;"></span> Skipped</div>
              <div class="legend-item"><span class="legend-dot" style="background:#7dd3fc;"></span> Active</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f0f9ff; border:1px solid #bae6fd;"></span> Unseen</div>
            </div>
            
            <div class="palette-grid" id="paletteGrid"></div>
            
            <button class="btn-primary" style="margin-top: 10px; background: var(--navy-dark);" onclick="switchView('resultsView')">
              📊 View Evaluation Scorecard
            </button>
            <button class="btn-secondary" style="margin-top: 8px; border-color: #cbd5e1;" onclick="resetStudentProgress()">
              🔄 Reset Progress
            </button>
          </div>

          <div class="palette-box" style="background: #f8fafc;">
            <h4 style="font-size: 0.92rem; margin-bottom: 8px; color: var(--navy-dark);">Workstation Scaffolding</h4>
            <p style="font-size: 0.82rem; line-height: 1.6; color: var(--text-muted);">
              • All 20 questions numbered sequentially 1 to 20.<br/>
              • High-visibility light yellow options cards.<br/>
              • <strong>2 attempts</strong> per problem before the <strong>Reveal Solution</strong> button unlocks.<br/>
              • Custom scaled SVG diagrams for geometry, piecewise, and calculus questions.
            </p>
          </div>
        </aside>
      </div>
    </div>

    <!-- View 2: TMUA Mathematical Methods Guide -->
    <div id="theoryView" class="view">
      <div class="theory-card">
        <h3>📐 Mathematical Principles &amp; Problem Solving Compendium</h3>
        <p class="theory-intro-text">
          High-yield theorems, algebra tools, and geometric principles required for TMUA Paper 1:
        </p>

        <div class="compendium-grid">
          <div class="comp-card">
            <h4>1. Piecewise &amp; Absolute Value Area</h4>
            <div class="recap-body">
              <p>For curves involving absolute values, identify critical kink points:</p>
              <div class="formula-box">
                \[|x^2 - 1| = \begin{cases} 1 - x^2 & |x| \le 1 \\ x^2 - 1 & |x| \ge 1 \end{cases}\]
                <p>Split integrals across critical points or use symmetry to avoid sign errors.</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>2. Vieta's Formulas &amp; Root Ratios</h4>
            <div class="recap-body">
              <p>For a quadratic \(A x^2 + B x + C = 0\) with roots in ratio \(1 : k\):</p>
              <div class="formula-box">
                \[r_1 = r, \quad r_2 = kr \implies r^2 = \frac{C}{kA}, \quad B^2 = \frac{(k+1)^2}{k} AC\]
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>3. Geometry of Circle Homothety</h4>
            <div class="recap-body">
              <p>The intersection \(P\) of common external tangents is the external center of similitude:</p>
              <div class="formula-box">
                \[\vec{P} = \frac{R_1 \vec{B} - R_2 \vec{A}}{R_1 - R_2}\]
                <p>Divides the line of centers externally in the ratio of the radii \(R_1 : R_2\).</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>4. Ambiguous Case of the Sine Rule</h4>
            <div class="recap-body">
              <p>Given angle \(A\), adjacent side \(b\), and opposite side \(a\):</p>
              <div class="formula-box">
                \[b \sin A < a < b\]
                <p>Two non-congruent triangles exist if and only if the opposite side exceeds the altitude but is strictly shorter than the adjacent side.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- View 3: Complete Solutions & Final Results -->
    <div id="resultsView" class="view">
      <div class="hero-score-card">
        <h2>JZ Mock Set A Paper 1 Evaluation Scorecard</h2>
        <div class="student-badge" id="reportStudentBadge"><strong>Candidate: Guest</strong></div>
        <div class="score-badge" id="scoreValue">0 / 20</div>
        <div class="progress-bar-wrap">
          <div class="progress-bar-fill" id="progressBarFill"></div>
        </div>
        <p id="scoreSubtitle" style="font-size:1.02rem; font-weight:600; color:var(--navy-dark); margin-top:8px;">
          Review all problem solutions, worked derivations, and diagrams below.
        </p>
        <button class="btn-primary" style="margin-top: 14px; max-width: 240px;" onclick="window.print()">🖨️ Print Final Scorecard</button>
      </div>

      <div id="completeSolutionsContainer"></div>
    </div>
  </main>

  <div class="toast" id="toastMessage"></div>

  <script>
    /* ==========================================================================
       COMPLETE 20-QUESTION DATASET (JZ MOCK SET A PAPER 1)
       ========================================================================== */
    const CHAPTER_QUESTIONS = [
      // ---------- QUESTION 1 ----------
      {
        id: 1,
        section: "Calculus & Absolute Values",
        title: "Area Enclosed by |x² - 1| and y = 3",
        prompt: "Find the finite area enclosed between the curve \\(y = |x^2 - 1|\\) and the line \\(y = 3\\).",
        svg: `<svg width="100%" height="220" viewBox="0 0 380 200" style="max-width:380px;">
          <rect width="380" height="200" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <!-- Axes: Origin at (190, 150), Scale: 1 unit x = 50px, 1 unit y = 30px -->
          <line x1="20" y1="150" x2="360" y2="150" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="185" stroke="#64748b" stroke-width="1.5"/>
          <text x="350" y="165" font-size="11" fill="#475569">x</text><text x="196" y="25" font-size="11" fill="#475569">y</text>
          
          <!-- Line y = 3 (150 - 3*30 = 60) -->
          <line x1="20" y1="60" x2="360" y2="60" stroke="#dc2626" stroke-width="2"/>
          <text x="30" y="52" font-size="10" font-weight="bold" fill="#dc2626">y = 3</text>
          
          <!-- Shaded enclosed region -->
          <path d="M 90,60 Q 115,150 140,150 Q 165,110 190,120 Q 215,110 240,150 Q 265,150 290,60 Z" fill="rgba(254, 240, 138, 0.45)"/>
          
          <!-- Curve y = |x^2 - 1| -->
          <path d="M 70,10 Q 110,135 140,150 Q 165,110 190,120 Q 215,110 240,150 Q 270,135 310,10" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          
          <!-- Intersections at (-2, 3) -> (90, 60) and (2, 3) -> (290, 60) -->
          <circle cx="90" cy="60" r="4.5" fill="#0284c7"/>
          <circle cx="290" cy="60" r="4.5" fill="#0284c7"/>
          <text x="75" y="78" font-size="10" fill="#0284c7">(−2, 3)</text>
          <text x="280" y="78" font-size="10" fill="#0284c7">(2, 3)</text>
          
          <circle cx="190" cy="120" r="3.5" fill="#0284c7"/><text x="195" y="115" font-size="9">(0, 1)</text>
          <circle cx="140" cy="150" r="3.5" fill="#0284c7"/><text x="130" y="165" font-size="9">−1</text>
          <circle cx="240" cy="150" r="3.5" fill="#0284c7"/><text x="238" y="165" font-size="9">1</text>
        </svg>`,
        options: [
          { label: "A", text: "13/3" },
          { label: "B", text: "4" },
          { label: "C", text: "8" },
          { label: "D", text: "25/3" },
          { label: "E", text: "23/3" },
          { label: "F", text: "11/3" }
        ],
        correctIndex: 2,
        explanation: "Find the intersection points of \\(|x^2 - 1| = 3\\):<br>\\[x^2 - 1 = 3 \\implies x^2 = 4 \\implies x = \\pm 2\\]<br>By reflectional symmetry about the \\(y\\)-axis, the area is:<br>\\[\\text{Area} = 2 \\int_0^2 (3 - |x^2 - 1|) \\, dx\\]<br>Split the integral at \\(x = 1\\):<br>• For \\(0 \\le x \\le 1\\), \\(|x^2 - 1| = 1 - x^2\\):<br>\\[\\int_0^1 [3 - (1 - x^2)] \\, dx = \\int_0^1 (2 + x^2) \\, dx = \\left[ 2x + \\frac{x^3}{3} \\right]_0^1 = 2 + \\frac{1}{3} = \\frac{7}{3}\\]<br>• For \\(1 \\le x \\le 2\\), \\(|x^2 - 1| = x^2 - 1\\):<br>\\[\\int_1^2 [3 - (x^2 - 1)] \\, dx = \\int_1^2 (4 - x^2) \\, dx = \\left[ 4x - \\frac{x^3}{3} \\right]_1^2 = \\left(8 - \\frac{8}{3}\\right) - \\left(4 - \\frac{1}{3}\\right) = \\frac{16}{3} - \\frac{11}{3} = \\frac{5}{3}\\]<br>Total Area = \\(2 \\left(\\frac{7}{3} + \\frac{5}{3}\\right) = 2 \\left(\\frac{12}{3}\\right) = 2 \\times 4 = 8\\) (Option C)."
      },

      // ---------- QUESTION 2 ----------
      {
        id: 2,
        section: "Quadratics & Root Properties",
        title: "Roots in Ratio 1:3",
        prompt: "The equation \\(2x^2 + px + 24 = 0\\) has two real roots in the ratio \\(1 : 3\\). Find the value of \\(p^2\\).",
        options: [
          { label: "A", text: "256" },
          { label: "B", text: "128" },
          { label: "C", text: "512" },
          { label: "D", text: "64" },
          { label: "E", text: "192" }
        ],
        correctIndex: 0,
        explanation: "Let the roots be \\(r\\) and \\(3r\\).<br>By Vieta's formulas for \\(2x^2 + px + 24 = 0\\):<br>• Product of roots: \\(r \\cdot (3r) = \\frac{24}{2} = 12 \\implies 3r^2 = 12 \\implies r^2 = 4 \\implies r = \\pm 2\\).<br>• Sum of roots: \\(r + 3r = 4r = -\\frac{p}{2} \\implies p = -8r\\).<br>Squaring both sides:<br>\\[p^2 = (-8r)^2 = 64r^2 = 64(4) = 256 \\quad \\text{(Option A)}\\]"
      },

      // ---------- QUESTION 3 ----------
      {
        id: 3,
        section: "Optimization & Piecewise Linear",
        title: "Minimum of Sum of Absolute Differences",
        prompt: "Find the minimum value of \\(|x - 1| + |x - 2| + |x - 3| + |x - 4|\\) over all real \\(x\\).",
        svg: `<svg width="100%" height="200" viewBox="0 0 380 180" style="max-width:380px;">
          <rect width="380" height="180" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <!-- Scale: 1 unit x = 50px, 1 unit y = 15px; Origin at (40, 150) -->
          <line x1="20" y1="150" x2="360" y2="150" stroke="#64748b" stroke-width="1.5"/>
          <line x1="40" y1="15" x2="40" y2="165" stroke="#64748b" stroke-width="1.5"/>
          <text x="350" y="165" font-size="11">x</text><text x="46" y="25" font-size="11">f(x)</text>
          
          <!-- Critical vertices: (1, 6), (2, 4), (3, 4), (4, 6) -->
          <!-- y = 4 is at 150 - 4*15 = 90; y = 6 is at 150 - 6*15 = 60 -->
          <line x1="20" y1="140" x2="90" y2="60" stroke="#0284c7" stroke-width="2.5"/>
          <line x1="90" y1="60" x2="140" y2="90" stroke="#0284c7" stroke-width="2.5"/>
          <!-- Flat minimum on [2, 3] -->
          <line x1="140" y1="90" x2="190" y2="90" stroke="#059669" stroke-width="3.5"/>
          <line x1="190" y1="90" x2="240" y2="60" stroke="#0284c7" stroke-width="2.5"/>
          <line x1="240" y1="60" x2="310" y2="140" stroke="#0284c7" stroke-width="2.5"/>
          
          <circle cx="140" cy="90" r="4.5" fill="#059669"/>
          <circle cx="190" cy="90" r="4.5" fill="#059669"/>
          <text x="145" y="80" font-size="10" font-weight="bold" fill="#059669">Flat Min = 4 on [2, 3]</text>
          
          <line x1="40" y1="90" x2="140" y2="90" stroke="#059669" stroke-dasharray="3"/>
          <text x="25" y="93" font-size="9" fill="#059669">4</text>
        </svg>`,
        options: [
          { label: "A", text: "2" },
          { label: "B", text: "3" },
          { label: "C", text: "4" },
          { label: "D", text: "5" },
          { label: "E", text: "6" },
          { label: "F", text: "8" },
          { label: "G", text: "10" }
        ],
        correctIndex: 2,
        explanation: "Pair the terms using the triangle inequality \\(|a| + |b| \\ge |a - b|\\):<br>• \\(|x - 1| + |x - 4| \\ge |(x - 1) - (x - 4)| = 3\\), with equality for all \\(1 \\le x \\le 4\\).<br>• \\(|x - 2| + |x - 3| \\ge |(x - 2) - (x - 3)| = 1\\), with equality for all \\(2 \\le x \\le 3\\).<br>Adding these inequalities:<br>\\[f(x) \\ge 3 + 1 = 4\\]<br>Equality holds simultaneously on the intersection of the two equality intervals, namely for any \\(x \\in [2, 3]\\). Thus, the minimum value is \\(4\\) (Option C)."
      },

      // ---------- QUESTION 4 ----------
      {
        id: 4,
        section: "Logarithmic Equations",
        title: "Simultaneous System in Three Logarithms",
        prompt: "Find the sum of all real values of \\(z\\) for which there exist positive real numbers \\(x\\) and \\(y\\) satisfying:\\[\\log_2(x^2 y z) = 3, \\quad \\log_2(x z) = 1, \\quad (\\log_2 y)(\\log_2 z) = 2\\]",
        options: [
          { label: "A", text: "3" },
          { label: "B", text: "9/4" },
          { label: "C", text: "9/2" },
          { label: "D", text: "7" },
          { label: "E", text: "8" },
          { label: "F", text: "9" },
          { label: "G", text: "63/4" }
        ],
        correctIndex: 1,
        explanation: "Let \\(X = \\log_2 x\\), \\(Y = \\log_2 y\\), \\(Z = \\log_2 z\\).<br>1. \\(2X + Y + Z = 3\\)<br>2. \\(X + Z = 1 \\implies X = 1 - Z\\)<br>3. \\(Y Z = 2\\)<br><br>Substitute \\(X = 1 - Z\\) into (1):<br>\\[2(1 - Z) + Y + Z = 3 \\implies 2 - Z + Y = 3 \\implies Y = Z + 1\\]<br>Substitute \\(Y = Z + 1\\) into (3):<br>\\[(Z + 1)Z = 2 \\implies Z^2 + Z - 2 = 0 \\implies (Z + 2)(Z - 1) = 0\\]<br>• If \\(Z = 1\\): \\(z = 2^1 = 2\\) (yields \\(X = 0 \\implies x = 1 > 0\\), \\(Y = 2 \\implies y = 4 > 0\\)).<br>• If \\(Z = -2\\): \\(z = 2^{-2} = \\frac{1}{4}\\) (yields \\(X = 3 \\implies x = 8 > 0\\), \\(Y = -1 \\implies y = 1/2 > 0\\)).<br>Sum of values of \\(z = 2 + \\frac{1}{4} = \\frac{9}{4}\\) (Option B)."
      },

      // ---------- QUESTION 5 ----------
      {
        id: 5,
        section: "Coordinate Geometry & Absolute Values",
        title: "Region Enclosed by 2|x - 1| and 6 - |x + 2|",
        prompt: "Find the area of the region enclosed between the curves \\(y = 2|x - 1|\\) and \\(y = 6 - |x + 2|\\).",
        svg: `<svg width="100%" height="220" viewBox="0 0 380 200" style="max-width:380px;">
          <rect width="380" height="200" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <!-- Scale: 1 unit x = 40px, 1 unit y = 20px; Origin at (150, 160) -->
          <line x1="20" y1="160" x2="360" y2="160" stroke="#64748b" stroke-width="1.5"/>
          <line x1="150" y1="15" x2="150" y2="185" stroke="#64748b" stroke-width="1.5"/>
          <text x="350" y="175" font-size="11">x</text><text x="156" y="25" font-size="11">y</text>
          
          <!-- Vertices: A(-2, 6) -> (70, 40), B(1, 0) -> (190, 160), C(2, 2) -> (230, 120) -->
          <polygon points="70,40 190,160 230,120" fill="rgba(254, 240, 138, 0.5)" stroke="#0c4a6e" stroke-width="2"/>
          
          <circle cx="70" cy="40" r="4.5" fill="#dc2626"/><text x="25" y="38" font-size="10" font-weight="bold" fill="#dc2626">(−2, 6)</text>
          <circle cx="190" cy="160" r="4.5" fill="#0284c7"/><text x="180" y="180" font-size="10" font-weight="bold" fill="#0284c7">(1, 0)</text>
          <circle cx="230" cy="120" r="4.5" fill="#059669"/><text x="238" y="122" font-size="10" font-weight="bold" fill="#059669">(2, 2)</text>
          
          <text x="135" y="105" font-size="12" font-weight="bold" fill="#713f12">Area = 6</text>
        </svg>`,
        options: [
          { label: "A", text: "11/2" },
          { label: "B", text: "20/3" },
          { label: "C", text: "17/3" },
          { label: "D", text: "6" },
          { label: "E", text: "13/2" }
        ],
        correctIndex: 3,
        explanation: "Find the intersection points of \\(y_1 = 2|x - 1|\\) and \\(y_2 = 6 - |x + 2|\\):<br>• For \\(x \\le -2\\): \\(2(1 - x) = 6 - (-x - 2) = 8 + x \\implies 2 - 2x = 8 + x \\implies x = -2\\), with \\(y = 6\\). Intersection at \\((-2, 6)\\).<br>• For \\(x \\ge 1\\): \\(2(x - 1) = 6 - (x + 2) = 4 - x \\implies 2x - 2 = 4 - x \\implies 3x = 6 \\implies x = 2\\), with \\(y = 2\\). Intersection at \\((2, 2)\\).<br>The lower boundary consists of two straight segments meeting at vertex \\((1, 0)\\). The upper boundary between \\(x = -2\\) and \\(x = 2\\) is the line segment \\(y = 4 - x\\).<br>The enclosed region is a triangle with vertices \\(A(-2, 6)\\), \\(B(1, 0)\\), and \\(C(2, 2)\\).<br>By the shoelace formula:<br>\\[\\text{Area} = \\frac{1}{2} |(-2)(0 - 2) + 1(2 - 6) + 2(6 - 0)| = \\frac{1}{2} |4 - 4 + 12| = 6 \\quad \\text{(Option D)}\\]"
      },

      // ---------- QUESTION 6 ----------
      {
        id: 6,
        section: "Trigonometry & Optimization",
        title: "Product of Extremes of Quadratic in g(x)",
        prompt: "Given \\[g(x) = \\frac{3}{4}\\left(\\sin\\left(\\frac{3}{2}x + \\frac{\\pi}{6}\\right) + \\cos\\left(\\frac{\\pi}{3} - \\frac{3}{2}x\\right) + 2\\right)\\] find the product of the maximum and minimum value of \\(4g(x) - (g(x))^2 - 3\\).",
        options: [
          { label: "A", text: "-3" },
          { label: "B", text: "0" },
          { label: "C", text: "1" },
          { label: "D", text: "3" },
          { label: "E", text: "2" },
          { label: "F", text: "-1" },
          { label: "G", text: "6" }
        ],
        correctIndex: 0,
        explanation: "Use the identity \\(\\cos(\\frac{\\pi}{3} - \\theta) = \\sin(\\frac{\\pi}{2} - (\\frac{\\pi}{3} - \\theta)) = \\sin(\\theta + \\frac{\\pi}{6})\\).<br>Thus:<br>\\[g(x) = \\frac{3}{4}\\left(2\\sin\\left(\\frac{3}{2}x + \\frac{\\pi}{6}\\right) + 2\\right) = \\frac{3}{2}\\left(\\sin\\left(\\frac{3}{2}x + \\frac{\\pi}{6}\\right) + 1\\right)\\]<br>Since \\(-1 \\le \\sin(\\dots) \\le 1\\), we have \\(g(x) \\in [0, 3]\\).<br>Let \\(u = g(x) \\in [0, 3]\\). We optimize \\(H(u) = 4u - u^2 - 3 = 1 - (u - 2)^2\\):<br>• The vertex is at \\(u = 2 \\in [0, 3]\\), giving the maximum value \\(H(2) = 1\\).<br>• The minimum on \\([0, 3]\\) occurs at the boundary furthest from the vertex: \\(H(0) = -3\\).<br>Product of maximum and minimum = \\(1 \\times (-3) = -3\\) (Option A)."
      },

      // ---------- QUESTION 7 ----------
      {
        id: 7,
        section: "Polynomials & Discriminants",
        title: "Cubic Equation with Exactly Two Real Roots",
        prompt: "Find the product of all distinct values of \\(p\\) for which \\[(x - p)(x^2 + px + p) = 0\\] is satisfied by exactly two distinct values of \\(x\\).",
        options: [
          { label: "A", text: "0" },
          { label: "B", text: "-2" },
          { label: "C", text: "7/2" },
          { label: "D", text: "-4" },
          { label: "E", text: "-7/2" },
          { label: "F", text: "2" }
        ],
        correctIndex: 1,
        explanation: "The solutions are \\(x = p\\) and the roots of \\(x^2 + px + p = 0\\). Exactly two distinct solutions occur in two cases:<br>1. **Quadratic has a repeated root (\\(\\Delta = 0\\)) distinct from \\(p\\)**:<br>\\(\\Delta = p^2 - 4p = p(p - 4) = 0 \\implies p = 0\\) or \\(p = 4\\).<br>• For \\(p = 0\\): equation becomes \\(x^3 = 0 \\implies x = 0\\) (only 1 distinct root, invalid).<br>• For \\(p = 4\\): \\((x - 4)(x + 2)^2 = 0 \\implies x = 4, -2\\) (2 distinct roots, valid).<br>2. **Quadratic has two distinct roots (\\(\\Delta > 0\\)), but one root equals \\(p\\)**:<br>Substituting \\(x = p\\): \\(p^2 + p^2 + p = 2p^2 + p = p(2p + 1) = 0 \\implies p = 0\\) or \\(p = -1/2\\).<br>• \\(p = 0\\) gives 1 root.<br>• For \\(p = -1/2\\): quadratic is \\(x^2 - \\frac{1}{2}x - \\frac{1}{2} = 0 \\implies (x - 1)(x + 1/2) = 0\\). Total roots are \\(\\{-1/2, 1\\}\\) (2 distinct roots, valid).<br>The valid values are \\(p = 4\\) and \\(p = -1/2\\). Their product is \\(4 \\times (-1/2) = -2\\) (Option B)."
      },

      // ---------- QUESTION 8 ----------
      {
        id: 8,
        section: "Number Theory & Exponent Laws",
        title: "Prime Factorization Exponent System",
        prompt: "Let \\(a, b,\\) and \\(c\\) be positive integers satisfying: \\[18^{a+c} 6^{a+b+5} = 12^{b-2} 18^5 6^{c+2}\\] Find the value of \\(a + b + c\\).",
        options: [
          { label: "A", text: "5" },
          { label: "B", text: "6" },
          { label: "C", text: "7" },
          { label: "D", text: "8" },
          { label: "E", text: "9" },
          { label: "F", text: "10" }
        ],
        correctIndex: 2,
        explanation: "Factor into primes \\(2\\) and \\(3\\): \\(18 = 2 \\cdot 3^2\\), \\(6 = 2 \\cdot 3\\), \\(12 = 2^2 \\cdot 3\\).<br>• Power of 2 on LHS: \\((a + c) + (a + b + 5) = 2a + b + c + 5\\).<br>• Power of 2 on RHS: \\(2(b - 2) + 5 + (c + 2) = 2b + c + 3\\).<br>Equating: \\(2a + b + c + 5 = 2b + c + 3 \\implies b = 2a + 2\\).<br><br>• Power of 3 on LHS: \\(2(a + c) + (a + b + 5) = 3a + b + 2c + 5\\).<br>• Power of 3 on RHS: \\((b - 2) + 2(5) + (c + 2) = b + c + 10\\).<br>Equating: \\(3a + b + 2c + 5 = b + c + 10 \\implies 3a + c = 5\\).<br><br>Since \\(a, c \\ge 1\\) are positive integers, \\(3a < 5 \\implies a = 1\\).<br>Then \\(c = 5 - 3(1) = 2\\) and \\(b = 2(1) + 2 = 4\\).<br>Sum = \\(a + b + c = 1 + 4 + 2 = 7\\) (Option C)."
      },

      // ---------- QUESTION 9 ----------
      {
        id: 9,
        section: "Circles & Tangents",
        title: "Common External Tangents and Homothetic Center",
        prompt: "The circles \\(C_1\\) and \\(C_2\\) have equations \\(x^2 + y^2 - 8y - 64 = 0\\) and \\(x^2 + y^2 - 6x - 11 = 0\\). The two common external tangents meet at \\(P\\), and one of them has equation \\(y = 2x - 16\\). Let \\(A\\) be the centre of \\(C_1\\) and \\(B\\) be the centre of \\(C_2\\). Find the distance \\(AP\\).",
        svg: `<svg width="100%" height="220" viewBox="0 0 380 200" style="max-width:380px;">
          <rect width="380" height="200" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <!-- Scale: 1 unit = 15px; Origin at (100, 110) -->
          <line x1="20" y1="110" x2="360" y2="110" stroke="#64748b" stroke-width="1.5"/>
          <line x1="100" y1="15" x2="100" y2="185" stroke="#64748b" stroke-width="1.5"/>
          
          <!-- C1: Centre A(0, 4) -> (100, 50), Radius R1 = 4*sqrt(5) ≈ 8.94 -> 134px -->
          <circle cx="100" cy="50" r="55" fill="none" stroke="#0284c7" stroke-width="2"/>
          <circle cx="100" cy="50" r="4" fill="#0284c7"/><text x="75" y="45" font-size="9" font-weight="bold" fill="#0284c7">A(0, 4)</text>
          
          <!-- C2: Centre B(3, 0) -> (145, 110), Radius R2 = 2*sqrt(5) ≈ 4.47 -> 67px -->
          <circle cx="145" cy="110" r="28" fill="none" stroke="#0284c7" stroke-width="2"/>
          <circle cx="145" cy="110" r="4" fill="#0284c7"/><text x="148" y="125" font-size="9" font-weight="bold" fill="#0284c7">B(3, 0)</text>
          
          <!-- Homothetic Center P(6, -4) -> (190, 170) -->
          <line x1="100" y1="50" x2="190" y2="170" stroke="#64748b" stroke-width="1.5" stroke-dasharray="3"/>
          <circle cx="190" cy="170" r="4.5" fill="#dc2626"/><text x="198" y="172" font-size="10" font-weight="bold" fill="#dc2626">P(6, −4)</text>
          
          <!-- Tangent line y = 2x - 16 -->
          <line x1="135" y1="60" x2="215" y2="220" stroke="#ea580c" stroke-width="2"/>
          <text x="215" y="190" font-size="9" fill="#ea580c">y = 2x − 16</text>
        </svg>`,
        options: [
          { label: "A", text: "12" },
          { label: "B", text: "10" },
          { label: "C", text: "15" },
          { label: "D", text: "3√5" },
          { label: "E", text: "4√5" }
        ],
        correctIndex: 1,
        explanation: "Rewrite circle equations by completing the square:<br>• \\(C_1: x^2 + (y - 4)^2 = 80\\), so centre \\(A = (0, 4)\\) and radius \\(R_1 = \\sqrt{80} = 4\\sqrt{5}\\).<br>• \\(C_2: (x - 3)^2 + y^2 = 20\\), so centre \\(B = (3, 0)\\) and radius \\(R_2 = \\sqrt{20} = 2\\sqrt{5}\\).<br>The intersection of the common external tangents \\(P\\) divides the segment \\(AB\\) externally in the ratio \\(R_1 : R_2 = 2 : 1\\).<br>Hence, \\(B\\) is the midpoint of \\(AP\\), so \\(AP = 2 \\times AB\\).<br>The distance between the centers is:<br>\\[AB = \\sqrt{(3 - 0)^2 + (0 - 4)^2} = \\sqrt{9 + 16} = 5\\]<br>Therefore, \\(AP = 2 \\times 5 = 10\\) (Option B)."
      },

      // ---------- QUESTION 10 ----------
      {
        id: 10,
        section: "Calculus & Rational Powers",
        title: "Intervals where f(x) is Increasing",
        prompt: "The function \\[f(x) = \\frac{1}{4}x^{4/3} + \\sqrt[3]{x} + \\frac{3}{\\sqrt[3]{x^2}}\\] is defined for all real \\(x \\ne 0\\). What is the complete set of values of \\(x\\) for which \\(f\\) is increasing (\\(f'(x) \\ge 0\\))?",
        options: [
          { label: "A", text: "-3 ≤ x < 0, x ≥ 2" },
          { label: "B", text: "x ≤ -3, 0 < x ≤ 2" },
          { label: "C", text: "x ≥ 2" },
          { label: "D", text: "-3 < x < 0, x > 2" },
          { label: "E", text: "-3 ≤ x ≤ 2, x ≠ 0" },
          { label: "F", text: "-3 ≤ x ≤ 0, x ≥ 2" }
        ],
        correctIndex: 0,
        explanation: "Write with rational exponents: \\(f(x) = \\frac{1}{4}x^{4/3} + x^{1/3} + 3x^{-2/3}\\).<br>Differentiating:<br>\\[f'(x) = \\frac{1}{3}x^{1/3} + \\frac{1}{3}x^{-2/3} - 2x^{-5/3} = \\frac{x^2 + x - 6}{3x^{5/3}} = \\frac{(x + 3)(x - 2)}{3x^{5/3}}\\]<br>Set up a sign chart for \\(x = -3, 0, 2\\):<br>• For \\(x < -3\\): \\((-)(-)/(-) = - < 0\\).<br>• For \\(-3 \\le x < 0\\): \\((+)(-)/(-) = + \\ge 0\\).<br>• For \\(0 < x < 2\\): \\((+)(-)/(+) = - < 0\\).<br>• For \\(x \\ge 2\\): \\((+)(+)/(+) = + \\ge 0\\).<br>Hence, \\(f'(x) \\ge 0\\) on \\(-3 \\le x < 0\\) and \\(x \\ge 2\\) (Option A)."
      },

      // ---------- QUESTION 11 ----------
      {
        id: 11,
        section: "Binomial Expansion",
        title: "Minimum Product of Coefficients in (a + bx)⁷",
        prompt: "In the expansion of \\((a + bx)^7\\), the coefficient of \\(x^5\\) plus twice the coefficient of \\(x^4\\) equals five times the coefficient of \\(x^3\\). Given positive integers \\(a\\) and \\(b\\), find the smallest possible value of \\(ab\\).",
        options: [
          { label: "A", text: "3" },
          { label: "B", text: "5" },
          { label: "C", text: "6" },
          { label: "D", text: "10" },
          { label: "E", text: "15" },
          { label: "F", text: "16" },
          { label: "G", text: "9" }
        ],
        correctIndex: 4,
        explanation: "Binomial coefficient of \\(x^k\\) is \\(\\binom{7}{k} a^{7-k} b^k\\):<br>• \\(x^5\\): \\(\\binom{7}{5} a^2 b^5 = 21 a^2 b^5\\)<br>• \\(x^4\\): \\(\\binom{7}{4} a^3 b^4 = 35 a^3 b^4\\)<br>• \\(x^3\\): \\(\\binom{7}{3} a^4 b^3 = 35 a^4 b^3\\)<br><br>The condition states:<br>\\[21 a^2 b^5 + 2(35 a^3 b^4) = 5(35 a^4 b^3) \\implies 21 a^2 b^5 + 70 a^3 b^4 = 175 a^4 b^3\\]<br>Divide by \\(7 a^2 b^3 > 0\\):<br>\\[3b^2 + 10ab = 25a^2 \\implies 25a^2 - 10ab - 3b^2 = 0\\]<br>Factoring gives \\((5a - 3b)(5a + b) = 0\\). Since \\(a, b > 0\\), \\(5a = 3b \\implies \\frac{a}{b} = \\frac{3}{5}\\).<br>The smallest positive integers are \\(a = 3, b = 5\\), giving \\(ab = 15\\) (Option E)."
      },

      // ---------- QUESTION 12 ----------
      {
        id: 12,
        section: "Geometric Progressions",
        title: "Alternating Geometric Series Sum",
        prompt: "The sum to infinity of a geometric sequence \\((u_n)\\) is \\(\\sqrt{3}\\), and the sum to infinity of the sequence obtained by squaring each term is \\(\\sqrt{6}\\). Define \\(v_n = (-1)^{n+1} u_n\\). What is the sum to infinity of \\((v_n)\\)?",
        options: [
          { label: "A", text: "√3" },
          { label: "B", text: "2√2 / 3" },
          { label: "C", text: "√2" },
          { label: "D", text: "infinity" },
          { label: "E", text: "√3 / 2" },
          { label: "F", text: "√2 / 2" }
        ],
        correctIndex: 2,
        explanation: "Let \\(u_n = a r^{n-1}\\) with \\(|r| < 1\\):<br>1. \\(\\frac{a}{1 - r} = \\sqrt{3}\\)<br>2. \\(\\sum u_n^2 = \\frac{a^2}{1 - r^2} = \\frac{a}{1 - r} \\cdot \\frac{a}{1 + r} = \\sqrt{6}\\)<br>Substituting (1) into (2):<br>\\[\\sqrt{3} \\cdot \\frac{a}{1 + r} = \\sqrt{6} \\implies \\frac{a}{1 + r} = \\frac{\\sqrt{6}}{\\sqrt{3}} = \\sqrt{2}\\]<br>The sequence \\(v_n\\) is \\(a, -ar, ar^2, -ar^3, \\dots\\), which is a geometric series with initial term \\(a\\) and common ratio \\(-r\\). Its sum to infinity is:<br>\\[\\sum_{n=1}^\\infty v_n = \\frac{a}{1 - (-r)} = \\frac{a}{1 + r} = \\sqrt{2} \\quad \\text{(Option C)}\\]"
      },

      // ---------- QUESTION 13 ----------
      {
        id: 13,
        section: "Polynomial Equations",
        title: "Exact Condition for 4 Real Solutions",
        prompt: "Find the set of values of \\(a\\) for which \\[x^4 - 4ax^3 + 4a^2 x^2 - a = 0\\] has exactly 4 distinct real solutions.",
        svg: `<svg width="100%" height="200" viewBox="0 0 380 180" style="max-width:380px;">
          <rect width="380" height="180" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <line x1="20" y1="130" x2="360" y2="130" stroke="#64748b" stroke-width="1.5"/>
          <line x1="60" y1="15" x2="60" y2="165" stroke="#64748b" stroke-width="1.5"/>
          <text x="350" y="145" font-size="11">x</text><text x="66" y="25" font-size="11">y</text>
          
          <!-- W-shaped curve y = (x(x - 2a))^2 with roots at 0 and 2a -->
          <path d="M 40,30 Q 70,130 90,130 Q 110,130 135,70 Q 160,130 180,130 Q 200,130 230,30" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <line x1="20" y1="90" x2="360" y2="90" stroke="#dc2626" stroke-width="1.5" stroke-dasharray="3"/>
          <text x="240" y="85" font-size="10" font-weight="bold" fill="#dc2626">Line y = a (4 cuts when a &gt; 1)</text>
          
          <circle cx="90" cy="130" r="3.5" fill="#0284c7"/><text x="85" y="145" font-size="9">0</text>
          <circle cx="180" cy="130" r="3.5" fill="#0284c7"/><text x="175" y="145" font-size="9">2a</text>
          <circle cx="135" cy="70" r="3.5" fill="#0284c7"/><text x="140" y="68" font-size="9">Local Max = a⁴</text>
        </svg>`,
        options: [
          { label: "A", text: "a > 1" },
          { label: "B", text: "|a| > 2" },
          { label: "C", text: "a > 2" },
          { label: "D", text: "a > 1/2" },
          { label: "E", text: "a > 3/2" }
        ],
        correctIndex: 0,
        explanation: "Notice that \\(x^4 - 4ax^3 + 4a^2 x^2 = (x^2 - 2ax)^2\\). The equation is:<br>\\[(x^2 - 2ax)^2 = a\\]<br>For real solutions, we must have \\(a > 0\\). Taking square roots:<br>1. \\(x^2 - 2ax - \\sqrt{a} = 0\\), with discriminant \\(\\Delta_1 = 4a^2 + 4\\sqrt{a} > 0\\) (always 2 real roots for \\(a > 0\\)).<br>2. \\(x^2 - 2ax + \\sqrt{a} = 0\\), with discriminant \\(\\Delta_2 = 4a^2 - 4\\sqrt{a} = 4\\sqrt{a}(a^{3/2} - 1)\\).<br>For this second quadratic to also have 2 distinct real roots, we need \\(\\Delta_2 > 0\\):<br>\\[a^{3/2} - 1 > 0 \\implies a > 1\\]<br>When \\(a > 1\\), the two quadratics have no shared roots, giving exactly \\(2 + 2 = 4\\) distinct solutions (Option A)."
      },

      // ---------- QUESTION 14 ----------
      {
        id: 14,
        section: "Transformations of Graphs",
        title: "Composition of Three Transformations",
        prompt: "The following sequence of transformations is applied, in order, to \\(y = 2x^2 - 3x + 1\\):<br>(1) translation by \\(\\binom{-1}{4}\\)<br>(2) reflection in the line \\(y = 2\\)<br>(3) stretch parallel to the \\(x\\)-axis with scale factor \\(1/2\\)<br>What is the equation of the resulting curve?",
        options: [
          { label: "A", text: "y = -8x² - 2x" },
          { label: "B", text: "y = -8x² + 2x" },
          { label: "C", text: "y = -2x² - x" },
          { label: "D", text: "y = -(1/2)x² - x" },
          { label: "E", text: "y = -(1/2)x² + x" },
          { label: "F", text: "y = -8x² - 4x" },
          { label: "G", text: "y = 8x² + 2x" }
        ],
        correctIndex: 0,
        explanation: "1. Translation by \\(\\binom{-1}{4}\\): replace \\(x \\to x + 1\\) and \\(y \\to y - 4\\):<br>\\[y - 4 = 2(x + 1)^2 - 3(x + 1) + 1 = 2x^2 + x \\implies y = 2x^2 + x + 4\\]<br>2. Reflection in \\(y = 2\\): replace \\(y \\to 4 - y\\):<br>\\[4 - y = 2x^2 + x + 4 \\implies -y = 2x^2 + x \\implies y = -2x^2 - x\\]<br>3. Stretch parallel to the \\(x\\)-axis by scale factor \\(1/2\\): replace \\(x \\to 2x\\):<br>\\[y = -2(2x)^2 - (2x) = -8x^2 - 2x \\quad \\text{(Option A)}\\]"
      },

      // ---------- QUESTION 15 ----------
      {
        id: 15,
        section: "Trigonometric Equations",
        title: "Sum of Solutions of Radical Trig Equation",
        prompt: "Find the sum of the solutions of \\[\\sqrt{1 - \\sin^2 x} = 2\\sin^2 x - \\cos x\\] on \\(0 \\le x \\le 360^\\circ\\).",
        options: [
          { label: "A", text: "180°" },
          { label: "B", text: "360°" },
          { label: "C", text: "540°" },
          { label: "D", text: "720°" },
          { label: "E", text: "900°" }
        ],
        correctIndex: 2,
        explanation: "Note that \\(\\sqrt{1 - \\sin^2 x} = |\\cos x|\\) and \\(2\\sin^2 x = 2(1 - \\cos^2 x)\\).<br>Let \\(c = \\cos x\\): \\(|c| = 2 - 2c^2 - c\\).<br>• Case 1: \\(c \\ge 0 \\implies c = 2 - 2c^2 - c \\implies 2c^2 + 2c - 2 = 0 \\implies c^2 + c - 1 = 0\\).<br>Since \\(c \\ge 0\\), \\(c = \\frac{\\sqrt{5} - 1}{2}\\). This gives two symmetric solutions in quadrants 1 and 4 summing to \\(360^\\circ\\).<br>• Case 2: \\(c < 0 \\implies -c = 2 - 2c^2 - c \\implies 2c^2 = 2 \\implies c = -1\\).<br>This gives \\(x = 180^\\circ\\).<br>Sum of all solutions = \\(360^\\circ + 180^\\circ = 540^\\circ\\) (Option C)."
      },

      // ---------- QUESTION 16 ----------
      {
        id: 16,
        section: "Exponential Optimization",
        title: "Maximum of Exponential Reciprocal Function",
        prompt: "Find the maximum value of \\[f(x) = \\frac{1}{4^x + 4^{-x} - 2(2^x + 2^{-x}) + 8}\\]",
        options: [
          { label: "A", text: "1/8" },
          { label: "B", text: "1/6" },
          { label: "C", text: "1/5" },
          { label: "D", text: "1/4" },
          { label: "E", text: "5" },
          { label: "F", text: "6" }
        ],
        correctIndex: 1,
        explanation: "Let \\(u = 2^x + 2^{-x}\\). By AM-GM, \\(u \\ge 2\\), with equality at \\(x = 0\\).<br>Note that \\(4^x + 4^{-x} = u^2 - 2\\). The denominator is:<br>\\[D(u) = (u^2 - 2) - 2u + 8 = u^2 - 2u + 6 = (u - 1)^2 + 5\\]<br>To maximize \\(f(x) = 1/D(u)\\), we must minimize \\(D(u)\\) for \\(u \\ge 2\\).<br>The parabola \\((u - 1)^2 + 5\\) has its vertex at \\(u = 1\\) and is strictly increasing for \\(u \\ge 2\\).<br>Hence, the minimum occurs at \\(u = 2\\):<br>\\[D(2) = (2 - 1)^2 + 5 = 6 \\implies f_{\\max} = \\frac{1}{6} \\quad \\text{(Option B)}\\]"
      },

      // ---------- QUESTION 17 ----------
      {
        id: 17,
        section: "Trigonometric Inequalities",
        title: "Total Interval Length for sin(7x) ≥ cos(14x)",
        prompt: "For \\(0 \\le x \\le 2\\pi\\), find the total length of the intervals on which \\(\\sin(7x) \\ge \\cos(14x)\\).",
        options: [
          { label: "A", text: "π/12" },
          { label: "B", text: "π/6" },
          { label: "C", text: "π/3" },
          { label: "D", text: "2π/3" },
          { label: "E", text: "5π/12" },
          { label: "F", text: "π/2" },
          { label: "G", text: "7π/12" },
          { label: "H", text: "4π/3" }
        ],
        correctIndex: 3,
        explanation: "Let \\(\\theta = 7x\\). As \\(x\\) ranges from \\(0\\) to \\(2\\pi\\), \\(\\theta\\) covers 7 full periods of \\(2\\pi\\) (from \\(0\\) to \\(14\\pi\\)).<br>The inequality is \\(\\sin\\theta \\ge \\cos(2\\theta) = 1 - 2\\sin^2\\theta\\):<br>\\[2\\sin^2\\theta + \\sin\\theta - 1 \\ge 0 \\implies (2\\sin\\theta - 1)(\\sin\\theta + 1) \\ge 0\\]<br>Since \\(\\sin\\theta \\ge -1\\) always, this holds whenever \\(\\sin\\theta \\ge 1/2\\).<br>In each single period of \\(2\\pi\\), \\(\\sin\\theta \\ge 1/2\\) on \\([\\pi/6, 5\\pi/6]\\), an interval of length \\(\\frac{5\\pi}{6} - \\frac{\\pi}{6} = \\frac{2\\pi}{3}\\).<br>Across 7 periods, the total length in \\(\\theta\\) is \\(7 \\times \\frac{2\\pi}{3} = \\frac{14\\pi}{3}\\).<br>Since \\(x = \\theta / 7\\), the total length in \\(x\\) is \\(\\frac{14\\pi / 3}{7} = \\frac{2\\pi}{3}\\) (Option D)."
      },

      // ---------- QUESTION 18 ----------
      {
        id: 18,
        section: "Definite Integrals & Transformations",
        title: "Decomposition of Definite Integrals",
        prompt: "A function \\(f\\) satisfies \\[\\int_0^2 f(x + 1) \\, dx = 1, \\quad \\int_0^2 f(2 - x) \\, dx = 2, \\quad \\int_0^{3/2} f(2x) \\, dx = 3\\] Find the value of \\(\\int_1^2 f(x) \\, dx\\).",
        options: [
          { label: "A", text: "-6" },
          { label: "B", text: "-3" },
          { label: "C", text: "0" },
          { label: "D", text: "1" },
          { label: "E", text: "3" },
          { label: "F", text: "4" },
          { label: "G", text: "5" },
          { label: "H", text: "6" }
        ],
        correctIndex: 1,
        explanation: "Transform each integral by substitution:<br>1. \\(u = x + 1 \\implies \\int_1^3 f(u) \\, du = 1\\).<br>2. \\(u = 2 - x \\implies \\int_0^2 f(u) \\, du = 2\\).<br>3. \\(u = 2x \\implies \\frac{1}{2} \\int_0^3 f(u) \\, du = 3 \\implies \\int_0^3 f(u) \\, du = 6\\).<br><br>From (2) and (3):<br>\\[\\int_2^3 f(u) \\, du = \\int_0^3 f(u) \\, du - \\int_0^2 f(u) \\, du = 6 - 2 = 4\\]<br>From (1):<br>\\[\\int_1^2 f(u) \\, du = \\int_1^3 f(u) \\, du - \\int_2^3 f(u) \\, du = 1 - 4 = -3 \\quad \\text{(Option B)}\\]"
      },

      // ---------- QUESTION 19 ----------
      {
        id: 19,
        section: "Trigonometry & Geometry",
        title: "Ambiguous Triangle Construction",
        prompt: "In a triangle \\(ABC\\), the angle at \\(A\\) is \\(30^\\circ\\). The side \\(BC\\) has length \\(a = (x - 2)(x - 3)\\) and the side \\(AC\\) has length \\(b = (3 - x)(x - 8)\\). Find the complete set of values of \\(x\\) for which there are two non-congruent triangles.",
        svg: `<svg width="100%" height="220" viewBox="0 0 380 200" style="max-width:380px;">
          <rect width="380" height="200" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <!-- Triangle construction showing ambiguous case -->
          <line x1="40" y1="160" x2="340" y2="160" stroke="#64748b" stroke-width="1.5"/>
          <!-- Vertex A at (40, 160) with 30 deg line -->
          <line x1="40" y1="160" x2="250" y2="38" stroke="#0284c7" stroke-width="2.5"/>
          <text x="55" y="152" font-size="10" font-weight="bold" fill="#0284c7">30°</text>
          <circle cx="40" cy="160" r="4" fill="#0284c7"/><text x="25" y="165" font-size="10" font-weight="bold">A</text>
          
          <!-- Vertex C at (250, 38) -->
          <circle cx="250" cy="38" r="4" fill="#0284c7"/><text x="255" y="32" font-size="10" font-weight="bold">C</text>
          <text x="130" y="90" font-size="10" fill="#0284c7">b = AC</text>
          
          <!-- Altitude h = b sin 30 = b/2 down to line AB -->
          <line x1="250" y1="38" x2="250" y2="160" stroke="#94a3b8" stroke-dasharray="3"/>
          <text x="255" y="105" font-size="9" fill="#94a3b8">h = b/2</text>
          
          <!-- Two positions B1 and B2 -->
          <line x1="250" y1="38" x2="200" y2="160" stroke="#059669" stroke-width="2"/>
          <line x1="250" y1="38" x2="300" y2="160" stroke="#059669" stroke-width="2"/>
          <circle cx="200" cy="160" r="4" fill="#059669"/><text x="190" y="175" font-size="10" font-weight="bold" fill="#059669">B₁</text>
          <circle cx="300" cy="160" r="4" fill="#059669"/><text x="302" y="175" font-size="10" font-weight="bold" fill="#059669">B₂</text>
          
          <path d="M 200,160 Q 250,185 300,160" fill="none" stroke="#ea580c" stroke-dasharray="3"/>
        </svg>`,
        options: [
          { label: "A", text: "3 < x < 4" },
          { label: "B", text: "3 < x < 5" },
          { label: "C", text: "3 < x < 8" },
          { label: "D", text: "4 < x < 5" },
          { label: "E", text: "4 < x < 8" },
          { label: "F", text: "5 < x < 8" }
        ],
        correctIndex: 3,
        explanation: "1. For positive side lengths: \\(b = (3 - x)(x - 8) > 0 \\implies 3 < x < 8\\). For \\(x > 3\\), \\(a = (x - 2)(x - 3) > 0\\) automatically.<br>2. In the ambiguous case with angle \\(A = 30^\\circ\\), two distinct triangles exist if and only if the altitude \\(h = b \\sin(30^\\circ) = \\frac{1}{2}b\\) is strictly less than \\(a\\), and \\(a < b\\):<br>\\[\\frac{1}{2}b < a < b\\]<br>• \\(a < b \\implies (x - 2)(x - 3) < -(x - 3)(x - 8)\\). Since \\(x - 3 > 0\\), divide through: \\(x - 2 < -x + 8 \\implies 2x < 10 \\implies x < 5\\).<br>• \\(a > \\frac{1}{2}b \\implies x - 2 > -\\frac{1}{2}(x - 8) = -\\frac{1}{2}x + 4 \\implies \\frac{3}{2}x > 6 \\implies x > 4\\).<br>Combining these yields \\(4 < x < 5\\) (Option D)."
      },

      // ---------- QUESTION 20 ----------
      {
        id: 20,
        section: "Sequences & Infinite Series",
        title: "Sum of Shifted Geometric Recurrence",
        prompt: "A sequence of real numbers \\((a_n)\\) is defined by \\(a_1 = 2\\) and the recurrence \\[a_{n+1}(a_n - 1) = \\frac{1}{2}a_n^2 - a_n + \\frac{1}{2} \\quad (n \\ge 1)\\] Find the value of \\(\\sum_{n=1}^\\infty (a_n + 1)\\).",
        options: [
          { label: "A", text: "0" },
          { label: "B", text: "4" },
          { label: "C", text: "6" },
          { label: "D", text: "8" },
          { label: "E", text: "9" },
          { label: "F", text: "5" },
          { label: "G", text: "18" }
        ],
        correctIndex: 2,
        explanation: "Rewrite the right-hand side of the recurrence:<br>\\[\\frac{1}{2}a_n^2 - a_n + \\frac{1}{2} = \\frac{1}{2}(a_n - 1)^2\\]<br>Thus: \\(a_{n+1}(a_n - 1) = \\frac{1}{2}(a_n - 1)^2\\).<br>For \\(a_n \\ne 1\\), divide by \\(a_n - 1\\):<br>\\[a_{n+1} = \\frac{1}{2}(a_n - 1) = \\frac{1}{2}a_n - \\frac{1}{2}\\]<br>Add 1 to both sides:<br>\\[a_{n+1} + 1 = \\frac{1}{2}a_n + \\frac{1}{2} = \\frac{1}{2}(a_n + 1)\\]<br>Let \\(b_n = a_n + 1\\). Then \\(b_{n+1} = \\frac{1}{2}b_n\\), which is a geometric progression with common ratio \\(r = 1/2\\).<br>The first term is \\(b_1 = a_1 + 1 = 2 + 1 = 3\\).<br>The sum to infinity is:<br>\\[\\sum_{n=1}^\\infty (a_n + 1) = \\sum_{n=1}^\\infty b_n = \\frac{b_1}{1 - r} = \\frac{3}{1 - 1/2} = 6 \\quad \\text{(Option C)}\\]"
      }
    ];

    /* ==========================================================================
       PERSISTENCE & INTERACTIVE TEST ENGINE
       ========================================================================== */
    const STORAGE_KEY = "jz_mock_set_a_p1_v1";

    let currentStudentName = "Guest";
    let currentQuestionIndex = 0;
    
    let questionStates = CHAPTER_QUESTIONS.map(q => ({
      id: q.id,
      attempts: 0,
      selectedIndex: null,
      isResolved: false,
      isCorrect: false,
      status: "unseen"
    }));

    let audioMuted = false;
    let totalSeconds = 0;
    let timerInterval = null;

    function saveSessionProgress() {
      try {
        const payload = {
          studentName: currentStudentName,
          currentQuestionIndex: currentQuestionIndex,
          totalSeconds: totalSeconds,
          questionStates: questionStates
        };
        localStorage.setItem(STORAGE_KEY, JSON.stringify(payload));
      } catch (e) {
        console.warn("Storage save error", e);
      }
    }

    function checkSavedSession() {
      try {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (!raw) return;
        const data = JSON.parse(raw);
        if (data && data.studentName) {
          const alertBox = document.getElementById('resumeAlertBox');
          const detailsSpan = document.getElementById('savedSessionDetails');
          const resumeBtn = document.getElementById('resumeSessionBtn');
          const startBtn = document.getElementById('startSessionBtn');
          const input = document.getElementById('studentNameInput');

          input.value = data.studentName;
          const completed = data.questionStates.filter(q => q.isResolved).length;
          detailsSpan.innerText = `Candidate: ${data.studentName} • ${completed}/20 Completed • Time: ${Math.floor(data.totalSeconds / 60)}m ${data.totalSeconds % 60}s`;
          alertBox.style.display = 'block';
          resumeBtn.style.display = 'inline-block';
          startBtn.innerText = 'Start Fresh Session';
        }
      } catch (e) {
        console.warn("Session check error", e);
      }
    }

    const AudioEngine = {
      ctx: null,
      init() {
        if (!this.ctx) {
          this.ctx = new (window.AudioContext || window.webkitAudioContext)();
        }
      },
      playTone(freq, type, duration, delay = 0) {
        if (audioMuted || !this.ctx) return;
        setTimeout(() => {
          try {
            const osc = this.ctx.createOscillator();
            const gain = this.ctx.createGain();
            osc.type = type;
            osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
            gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + duration);
            osc.connect(gain);
            gain.connect(this.ctx.destination);
            osc.start();
            osc.stop(this.ctx.currentTime + duration);
          } catch (e) {
            console.warn(e);
          }
        }, delay * 1000);
      },
      correct() {
        this.init();
        this.playTone(659.25, 'sine', 0.15, 0);
        this.playTone(880.00, 'sine', 0.25, 0.12);
      },
      incorrect() {
        this.init();
        this.playTone(196.00, 'triangle', 0.2, 0);
        this.playTone(146.83, 'triangle', 0.3, 0.12);
      }
    };

    function startTimer() {
      if (timerInterval) clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        totalSeconds++;
        const mins = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const secs = String(totalSeconds % 60).padStart(2, '0');
        document.getElementById('timerChip').innerText = `⏱️ ${mins}:${secs}`;
        saveSessionProgress();
      }, 1000);
    }

    function showToast(msg) {
      const t = document.getElementById('toastMessage');
      t.innerText = msg;
      t.style.display = 'block';
      setTimeout(() => { t.style.display = 'none'; }, 2600);
    }

    function initDirectLogin(isResume = false) {
      const nameInput = document.getElementById('studentNameInput').value.trim() || 'Candidate';
      
      if (isResume) {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (raw) {
          const data = JSON.parse(raw);
          currentStudentName = data.studentName || nameInput;
          currentQuestionIndex = data.currentQuestionIndex || 0;
          totalSeconds = data.totalSeconds || 0;
          if (Array.isArray(data.questionStates)) {
            questionStates = data.questionStates;
          }
          showToast(`Welcome back, ${currentStudentName}!`);
        }
      } else {
        currentStudentName = nameInput;
        totalSeconds = 0;
        currentQuestionIndex = 0;
        questionStates = CHAPTER_QUESTIONS.map(q => ({
          id: q.id,
          attempts: 0,
          selectedIndex: null,
          isResolved: false,
          isCorrect: false,
          status: "unseen"
        }));
        saveSessionProgress();
      }

      document.getElementById('userPill').innerHTML = `<strong>Candidate: ${currentStudentName}</strong>`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Candidate: ${currentStudentName}</strong>`;
      document.getElementById('loginGateView').style.display = 'none';
      
      AudioEngine.init();
      startTimer();
      renderPalette();
      loadQuestion(currentQuestionIndex);
      renderSolutions();
    }

    function resetStudentProgress() {
      if (confirm("Reset this test session and clear all saved progress?")) {
        localStorage.removeItem(STORAGE_KEY);
        location.reload();
      }
    }

    function switchView(viewId) {
      document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
      document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
      document.getElementById(viewId).classList.add('active');

      if (viewId === 'practiceView') document.getElementById('tabPracticeBtn').classList.add('active');
      if (viewId === 'theoryView') document.getElementById('tabTheoryBtn').classList.add('active');
      if (viewId === 'resultsView') {
        document.getElementById('tabResultsBtn').classList.add('active');
        renderSolutions();
      }

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function renderPalette() {
      const grid = document.getElementById('paletteGrid');
      grid.innerHTML = '';

      let solvedCount = 0;
      CHAPTER_QUESTIONS.forEach((q, idx) => {
        const state = questionStates[idx];
        if (state.isResolved) solvedCount++;

        const btn = document.createElement('button');
        let stateClass = '';
        if (idx === currentQuestionIndex) {
          stateClass = 'active';
        } else if (state.isResolved) {
          stateClass = 'completed';
        } else if (state.status === 'skipped') {
          stateClass = 'skipped';
        }

        btn.className = `palette-btn ${stateClass}`;
        btn.innerText = q.id;
        btn.title = `Question ${q.id}: ${q.title}`;
        btn.onclick = () => loadQuestion(idx);
        grid.appendChild(btn);
      });

      document.getElementById('paletteCount').innerText = `${solvedCount} / ${CHAPTER_QUESTIONS.length} Solved`;
    }

    function loadQuestion(idx) {
      currentQuestionIndex = idx;
      saveSessionProgress();
      renderPalette();
      const q = CHAPTER_QUESTIONS[idx];
      const state = questionStates[idx];
      const card = document.getElementById('activeQuestionCard');

      let optionsHtml = '';
      q.options.forEach((opt, optIdx) => {
        let optClass = '';
        if (state.isResolved) {
          if (optIdx === q.correctIndex) {
            optClass = 'selected-correct';
          } else if (state.selectedIndex === optIdx) {
            optClass = 'selected-wrong';
          }
        }

        optionsHtml += `
          <button class="mcq-option-btn ${optClass}" 
            onclick="handleOptionSelect(${idx}, ${optIdx})" 
            ${state.isResolved ? 'disabled' : ''}>
            <span class="opt-letter">${opt.label}</span>
            <span>\\(${opt.text}\\)</span>
          </button>
        `;
      });

      let feedbackHtml = '';
      if (state.isResolved) {
        feedbackHtml = `
          <div class="feedback-box ${state.isCorrect ? 'correct' : 'incorrect'}">
            <strong>${state.isCorrect ? '✓ Correct Solution' : '✗ Solution Revealed'}</strong> (Option ${q.options[q.correctIndex].label})<br/>
            <div style="margin-top: 8px;">${q.explanation}</div>
          </div>
        `;
      }

      const prevDisabled = idx === 0 ? 'disabled' : '';
      const nextDisabled = idx === CHAPTER_QUESTIONS.length - 1 ? 'disabled' : '';

      card.innerHTML = `
        <span class="concept-tag">${q.section}</span>
        <h2 style="color:var(--navy-dark); margin: 6px 0 10px 0;">Question ${q.id}: ${q.title}</h2>
        <div style="margin-top: 8px; line-height: 1.65; font-size:1.02rem;">${q.prompt}</div>
        ${q.svg ? `<div class="svg-container">${q.svg}</div>` : ''}
        <div class="mcq-container">${optionsHtml}</div>
        
        <div style="display:flex; align-items:center; margin-top:12px;">
          <span class="attempts-badge">Attempts: ${state.attempts}/2</span>
          ${!state.isResolved && state.attempts >= 2 ? `
            <button class="btn-reveal" onclick="revealSolution(${idx})">Reveal Solution</button>
          ` : ''}
        </div>

        ${feedbackHtml}

        <div class="nav-toolbar">
          <button class="btn-nav-action" onclick="navigateQuestion(-1)" ${prevDisabled}>
            ⏮ Previous
          </button>
          <div class="nav-btn-group">
            <button class="btn-nav-action btn-skip" onclick="skipQuestion()">
              ⏭ Skip
            </button>
            <button class="btn-nav-action" onclick="navigateQuestion(1)" ${nextDisabled}>
              Next ❯
            </button>
          </div>
        </div>
      `;

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function handleOptionSelect(qIdx, optIdx) {
      const q = CHAPTER_QUESTIONS[qIdx];
      const state = questionStates[qIdx];
      if (state.isResolved) return;

      state.selectedIndex = optIdx;
      state.attempts++;

      if (optIdx === q.correctIndex) {
        state.isResolved = true;
        state.isCorrect = true;
        state.status = 'completed';
        AudioEngine.correct();
        showToast("Correct! Answer registered.");
      } else {
        AudioEngine.incorrect();
        if (state.attempts >= 2) {
          showToast("2 attempts reached. You can retry or click 'Reveal Solution'.");
        } else {
          showToast("Incorrect option. You have 1 attempt remaining!");
        }
      }

      saveSessionProgress();
      renderPalette();
      loadQuestion(qIdx);
      renderSolutions();
    }

    function revealSolution(qIdx) {
      const state = questionStates[qIdx];
      state.isResolved = true;
      state.status = 'completed';
      AudioEngine.incorrect();
      showToast("Solution revealed.");
      saveSessionProgress();
      renderPalette();
      loadQuestion(qIdx);
      renderSolutions();
    }

    function navigateQuestion(delta) {
      const target = currentQuestionIndex + delta;
      if (target >= 0 && target < CHAPTER_QUESTIONS.length) {
        loadQuestion(target);
      }
    }

    function skipQuestion() {
      const state = questionStates[currentQuestionIndex];
      if (!state.isResolved) {
        state.status = 'skipped';
      }
      showToast(`Question ${CHAPTER_QUESTIONS[currentQuestionIndex].id} marked as skipped.`);
      saveSessionProgress();
      renderPalette();
      navigateQuestion(1);
    }

    function renderSolutions() {
      const container = document.getElementById('completeSolutionsContainer');
      let score = 0;

      CHAPTER_QUESTIONS.forEach((q, idx) => {
        if (questionStates[idx].isCorrect) score++;
      });

      const total = CHAPTER_QUESTIONS.length;
      const percentage = Math.round((score / total) * 100);

      document.getElementById('scoreValue').innerText = `${score} / ${total}`;
      document.getElementById('progressBarFill').style.width = `${percentage}%`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Candidate: ${currentStudentName}</strong> (${percentage}% Score)`;

      let html = '';
      CHAPTER_QUESTIONS.forEach((q, idx) => {
        const state = questionStates[idx];
        let statusBadge = `<span style="color:var(--text-muted); font-weight:bold;">Unattempted</span>`;

        if (state.isResolved) {
          statusBadge = state.isCorrect
            ? `<span style="color:var(--green-ok); font-weight:bold;">✓ Correct (1/1)</span>`
            : `<span style="color:var(--red-fail); font-weight:bold;">✗ Solution Revealed (0/1)</span>`;
        }

        const studentChoiceLabel = (state.selectedIndex !== null && q.options[state.selectedIndex])
          ? `[${q.options[state.selectedIndex].label}] \\(${q.options[state.selectedIndex].text}\\)`
          : 'None';

        html += `
          <div class="theory-card">
            <div style="display:flex; justify-content:space-between; align-items:center;">
              <span class="concept-tag">${q.section}</span>
              ${statusBadge}
            </div>
            <h3 style="margin-top:6px;">Question ${q.id}: ${q.title}</h3>
            <div style="margin: 8px 0; font-size:0.95rem;">${q.prompt}</div>
            ${q.svg ? `<div class="svg-container" style="max-width:320px; margin:12px 0;">${q.svg}</div>` : ''}
            
            <div style="background:#f8fafc; border-left:4px solid var(--brand-blue); padding:14px; margin-top:12px; border-radius:0 6px 6px 0;">
              <strong>Correct Option:</strong> [${q.options[q.correctIndex].label}] \\(${q.options[q.correctIndex].text}\\)<br/>
              <strong>Your Choice:</strong> ${studentChoiceLabel}<br/>
              <div style="margin-top:8px;"><strong>Full Worked Derivation:</strong><br/>${q.explanation}</div>
            </div>
          </div>
        `;
      });

      container.innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    document.getElementById('audioToggleBtn').onclick = () => {
      audioMuted = !audioMuted;
      document.getElementById('audioToggleBtn').innerText = audioMuted ? '🔇' : '🔊';
    };

    window.addEventListener('DOMContentLoaded', checkSavedSession);
  </script>
</body>
</html>
