<!-- ================== ULTRA PREMIUM COSMIC README ================== -->

<!--
  Paste this whole file into README.md
  Note: For exact custom fonts, host them or convert the header to an image.
-->

<!-- ================== COSMIC HEADER (SVG: stars, shooting-stars, orbit, planet) ================== -->
<p align="center">

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 380" width="100%" height="380" preserveAspectRatio="xMidYMid slice">

  <!-- defs -->
  <defs>
    <!-- gradients -->
    <linearGradient id="bgG" x1="0" x2="1">
      <stop offset="0" stop-color="#04030a"/>
      <stop offset="0.35" stop-color="#0b0920"/>
      <stop offset="1" stop-color="#1b1333"/>
    </linearGradient>

    <radialGradient id="planetGrad" cx="40%" cy="35%">
      <stop offset="0" stop-color="#ffd7ff"/>
      <stop offset="0.35" stop-color="#d293ff"/>
      <stop offset="1" stop-color="#6a2bd3"/>
    </radialGradient>

    <!-- glass blur effect -->
    <filter id="glass" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="6" result="b"/>
      <feColorMatrix in="b" type="matrix"
        values="1 0 0 0 0
                0 1 0 0 0
                0 0 1 0 0
                0 0 0 0.5 0" result="blur"/>
      <feBlend in="SourceGraphic" in2="blur" mode="screen"/>
    </filter>

    <!-- subtle star glow -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="1.8" result="g"/>
      <feMerge><feMergeNode in="g"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>

    <!-- ring stroke for planet -->
    <linearGradient id="ringGrad" x1="0" x2="1">
      <stop offset="0" stop-color="#d6a4ff"/>
      <stop offset="1" stop-color="#7b61ff"/>
    </linearGradient>
  </defs>

  <!-- background -->
  <rect width="1200" height="380" fill="url(#bgG)"/>

  <!-- twinkling stars field (repeated small circles) -->
  <g id="stars">
    <!-- some static stars -->
    <circle cx="60" cy="44" r="1.6" fill="#fff" opacity="0.95" filter="url(#glow)">
      <animate attributeName="opacity" values="0.9;0.2;0.9" dur="3.6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="140" cy="90" r="1.2" fill="#fff" opacity="0.9">
      <animate attributeName="opacity" values="0.8;0.3;0.8" dur="2.8s" repeatCount="indefinite"/>
    </circle>
    <circle cx="360" cy="26" r="1.8" fill="#fff" opacity="0.95">
      <animate attributeName="opacity" values="0.9;0.15;0.9" dur="4.2s" repeatCount="indefinite"/>
    </circle>
    <circle cx="520" cy="120" r="1.2" fill="#fff" opacity="0.85">
      <animate attributeName="opacity" values="0.9;0.2;0.9" dur="3.1s" repeatCount="indefinite"/>
    </circle>
    <circle cx="760" cy="62" r="1.4" fill="#fff" opacity="0.9">
      <animate attributeName="opacity" values="0.9;0.25;0.9" dur="3.8s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1020" cy="26" r="1.6" fill="#fff" opacity="0.9">
      <animate attributeName="opacity" values="0.95;0.2;0.95" dur="2.9s" repeatCount="indefinite"/>
    </circle>
    <!-- faint background specks -->
    <g opacity="0.4">
      <circle cx="940" cy="160" r="0.9" fill="#fff"/>
      <circle cx="1120" cy="99" r="0.8" fill="#fff"/>
      <circle cx="280" cy="160" r="0.7" fill="#fff"/>
      <circle cx="430" cy="210" r="0.7" fill="#fff"/>
      <circle cx="100" cy="180" r="0.7" fill="#fff"/>
    </g>
  </g>

  <!-- shooting stars -->
  <g id="shooters" stroke="#ffffff" stroke-linecap="round" stroke-width="1.6" opacity="0.95">
    <!-- star 1 -->
    <g transform="translate(-200,0)">
      <line x1="0" y1="80" x2="120" y2="20" stroke-opacity="0.7">
        <animateTransform attributeName="transform" type="translate"
          from="-400 20" to="1300 -20" dur="5s" repeatCount="indefinite"/>
        <animate attributeName="stroke-opacity" values="0;1;0" dur="5s" repeatCount="indefinite"/>
      </line>
    </g>
    <!-- star 2 -->
    <g transform="translate(-200,0)">
      <line x1="0" y1="40" x2="140" y2="0" stroke-opacity="0.9">
        <animateTransform attributeName="transform" type="translate"
          from="-200 40" to="1200 -30" dur="7s" repeatCount="indefinite" begin="1s"/>
        <animate attributeName="stroke-opacity" values="0;1;0" dur="7s" repeatCount="indefinite" begin="1s"/>
      </line>
    </g>
    <!-- star 3 -->
    <g transform="translate(-200,0)">
      <line x1="0" y1="120" x2="160" y2="40" stroke-opacity="0.85">
        <animateTransform attributeName="transform" type="translate"
          from="-400 120" to="1400 -60" dur="9s" repeatCount="indefinite" begin="2.2s"/>
        <animate attributeName="stroke-opacity" values="0;1;0" dur="9s" repeatCount="indefinite" begin="2.2s"/>
      </line>
    </g>
  </g>

  <!-- subtle horizon / glass plate -->
  <g transform="translate(0,0)">
    <rect x="60" y="48" rx="14" ry="14" width="1080" height="210" fill="rgba(255,255,255,0.02)" stroke="rgba(255,255,255,0.03)" />
  </g>

  <!-- planet group (3D illusion) -->
  <g id="planetGroup" transform="translate(920,220)">
    <!-- ring -->
    <ellipse rx="90" ry="26" fill="none" stroke="url(#ringGrad)" stroke-width="3" opacity="0.9" transform="rotate(-18)">
      <animateTransform attributeName="transform" type="rotate"
        values="-18;22;-18" dur="10s" repeatCount="indefinite"/>
    </ellipse>

    <!-- planet sphere -->
    <g>
      <circle cx="0" cy="0" r="55" fill="url(#planetGrad)" />
      <!-- slight shading using ellipse -->
      <ellipse cx="-8" cy="4" rx="28" ry="42" fill="rgba(0,0,0,0.08)">
        <animateTransform attributeName="transform" type="rotate"
          values="0 0 0;360 0 0" dur="18s" repeatCount="indefinite"/>
      </ellipse>
      <!-- glossy highlight -->
      <ellipse cx="-20" cy="-14" rx="12" ry="7" fill="rgba(255,255,255,0.55)"/>
    </g>

    <!-- planet rotation (parent rotate to mimic 3D spin) -->
    <animateTransform attributeName="transform" type="rotate"
        from="0 920 220" to="360 920 220" dur="24s" repeatCount="indefinite"/>
  </g>

  <!-- center name + satellite orbit -->
  <g id="center" transform="translate(300,150)">
    <!-- orbit path -->
    <ellipse cx="300" cy="70" rx="210" ry="80" fill="none" stroke="rgba(199,125,255,0.06)" stroke-width="1.25" />

    <!-- satellite orbiting -->
    <g transform="translate(300,70)">
      <!-- orbiting satellite body -->
      <g id="sat" transform="rotate(0)">
        <rect x="-6" y="-6" width="12" height="12" rx="2" fill="#c77dff" />
        <rect x="-18" y="-2" width="10" height="4" rx="1" fill="#9d4edd" transform="rotate(20)"/>
        <circle cx="-10" cy="-10" r="1.6" fill="#fff" opacity="0.9" />
      </g>
      <!-- rotate the satellite group around the center -->
      <animateTransform xlink:href="#sat" attributeName="transform" attributeType="XML"
        type="rotate" from="0" to="360" dur="9s" repeatCount="indefinite" />
    </g>

    <!-- name -->
    <text x="300" y="40" text-anchor="middle" font-family="'Orbitron', 'Montserrat', Inter, system-ui, -apple-system, sans-serif"
      font-weight="700" font-size="54" fill="#ffffff" letter-spacing="1">
      D I B Y X
    </text>

    <!-- subtitle -->
    <text x="300" y="80" text-anchor="middle" font-family="monospace" font-size="14" fill="#c8a8ff" opacity="0.95">
      Cosmic Code Architect  •  Astrophile • AI Explorer
    </text>

    <!-- decorative small rings near the name -->
    <g transform="translate(73,36)">
      <circle r="6" fill="none" stroke="#cbb3ff" stroke-width="1.2" opacity="0.65"/>
      <circle r="12" fill="none" stroke="#7b61ff" stroke-width="0.6" opacity="0.12"/>
    </g>
  </g>

  <!-- small watermark text (subtle) -->
  <text x="1150" y="375" fill="#ffffff" font-size="9" opacity="0.12" font-family="monospace" text-anchor="end">d i b y x</text>

</svg>

</p>

---

<!-- ================== MISSION CONTROL (Terminal Panel + Glass Cards) ================== -->

<div align="center">

<!-- glass terminal-like console (SVG) -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 180" width="100%" height="180" preserveAspectRatio="xMidYMid meet">
  <defs>
    <linearGradient id="termBG" x1="0" x2="1">
      <stop offset="0" stop-color="#07060b" />
      <stop offset="1" stop-color="#0f0c29" />
    </linearGradient>
  </defs>

  <!-- glass frame -->
  <rect x="28" y="18" rx="12" ry="12" width="944" height="144" fill="rgba(255,255,255,0.02)" stroke="rgba(255,255,255,0.04)"/>
  <g transform="translate(42,36)">

    <!-- top left control dots -->
    <g transform="translate(2,2)">
      <circle cx="8" cy="8" r="6" fill="#ff5f57"/>
      <circle cx="30" cy="8" r="6" fill="#ffbd2e"/>
      <circle cx="52" cy="8" r="6" fill="#27c93f"/>
    </g>

    <!-- terminal text block -->
    <g font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, 'Roboto Mono', 'Courier New', monospace" font-size="13" fill="#cfcff8" >
      <!-- command prompt label -->
      <text x="14" y="50" fill="#9d9df6" font-size="12">[mission-control ~ /workspace]</text>

      <!-- Animated lines: we use opacity animations to reveal sequential messages -->
      <text id="t1" x="14" y="80" opacity="0.0">➤ Initializing cosmic AI agent...</text>
      <animate xlink:href="#t1" attributeName="opacity" values="0;1" dur="0.6s" begin="0.4s" fill="freeze"/>

      <text id="t2" x="14" y="104" opacity="0.0">➤ Syncing orbital telemetry & datasets...</text>
      <animate xlink:href="#t2" attributeName="opacity" values="0;1" dur="0.6s" begin="1.2s" fill="freeze"/>

      <text id="t3" x="14" y="128" opacity="0.0">➤ Deploying micro-services to production nodes (🚀)...</text>
      <animate xlink:href="#t3" attributeName="opacity" values="0;1" dur="0.6s" begin="2.0s" fill="freeze"/>

      <!-- blinking cursor -->
      <rect x="10" y="136" width="8" height="12" fill="#c77dff" opacity="0.9">
        <animate attributeName="opacity" values="0;1;0" dur="1s" repeatCount="indefinite"/>
      </rect>
      <text x="26" y="146" fill="#9fb0ff" font-size="12" opacity="0.85">awaiting input...</text>
    </g>
  </g>
</svg>

</div>

---

<!-- ================== STYLIZED TECH BADGES (SVG inline) ================== -->
<p align="center">
  <!-- python -->
  <svg xmlns="http://www.w3.org/2000/svg" width="120" height="34" viewBox="0 0 120 34" style="margin:6px">
    <rect rx="6" width="120" height="34" fill="#0f0c29" stroke="#2a2347" />
    <text x="20" y="22" font-family="'Montserrat', Inter, system-ui, sans-serif" fill="#ffe9ff" font-size="13">🐍 Python</text>
    <rect x="78" y="6" rx="4" width="34" height="22" fill="#9d4edd"/>
    <text x="88" y="22" font-size="12" fill="#fff" font-family="monospace">Py</text>
  </svg>

  <!-- node -->
  <svg xmlns="http://www.w3.org/2000/svg" width="120" height="34" viewBox="0 0 120 34" style="margin:6px">
    <rect rx="6" width="120" height="34" fill="#0f0c29" stroke="#2a2347"/>
    <text x="20" y="22" font-family="'Montserrat', Inter, system-ui, sans-serif" fill="#c8f0d6" font-size="13">⚙️ Node.js</text>
    <rect x="78" y="6" rx="4" width="34" height="22" fill="#2b9f4a"/>
    <text x="88" y="22" font-size="12" fill="#fff" font-family="monospace">Nd</text>
  </svg>

  <!-- react -->
  <svg xmlns="http://www.w3.org/2000/svg" width="120" height="34" viewBox="0 0 120 34" style="margin:6px">
    <rect rx="6" width="120" height="34" fill="#0f0c29" stroke="#2a2347"/>
    <text x="20" y="22" font-family="'Montserrat', Inter, system-ui, sans-serif" fill="#9fe0ff" font-size="13">⚛ React</text>
    <rect x="78" y="6" rx="4" width="34" height="22" fill="#61dafb"/>
    <text x="88" y="22" font-size="12" fill="#030303" font-family="monospace">R</text>
  </svg>
</p>

---

<!-- ================== PERSONAL STATEMENT / CTA ================== -->
<p align="center" style="font-family:'Montserrat', Inter, system-ui, sans-serif; color:#d6c7ff;">
  <strong style="font-size:16px">I'm an astrophile building cosmic-grade systems ✨</strong><br/>
  <span style="color:#bdb0ff">Reach out for collabs, research, or a mission brief.</span>
</p>

<!-- contact badges (SVG buttons) -->
<p align="center">
  <a href="mailto:concealment960@gmail.com" style="text-decoration:none">
    <svg xmlns="http://www.w3.org/2000/svg" width="190" height="36" viewBox="0 0 190 36">
      <rect rx="8" width="190" height="36" fill="#9d4edd"/>
      <text x="96" y="23" text-anchor="middle" font-family="'Montserrat', Inter, system-ui, sans-serif" fill="#ffffff" font-size="13">✉️ Email — concealment960@gmail.com</text>
    </svg>
  </a>

  <a href="https://github.com/dibyx" style="text-decoration:none">
    <svg xmlns="http://www.w3.org/2000/svg" width="160" height="36" viewBox="0 0 160 36">
      <rect rx="8" width="160" height="36" fill="#0b0b0d"/>
      <text x="80" y="23" text-anchor="middle" font-family="'Montserrat', Inter, system-ui, sans-serif" fill="#c8c8ff" font-size="13">🐙 GitHub /dibyx</text>
    </svg>
  </a>
</p>

---

<!-- ================== FOOTER (glass - black hole vibe) ================== -->
<p align="center">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" width="100%" height="80">
    <defs>
      <radialGradient id="bh" cx="50%" cy="40%">
        <stop offset="0%" stop-color="#111018"/>
        <stop offset="60%" stop-color="#07060b"/>
        <stop offset="100%" stop-color="#04030a"/>
      </radialGradient>
    </defs>
    <rect width="1000" height="100" fill="url(#bh)"/>
    <text x="50%" y="55%" dominant-baseline="middle" text-anchor="middle" fill="#bca6ff" font-family="'Montserrat', Inter, system-ui, sans-serif" font-size="14">Code. Create. Conquer the Cosmos.</text>
  </svg>
</p>

<!-- ================== END README ================== -->
