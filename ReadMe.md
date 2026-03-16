<div align="center">

<!--═══════════════════════ HERO BANNER ═══════════════════════-->

<svg width="900" height="320" viewBox="0 0 900 320" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Deep space background gradient -->
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#020408"/>
      <stop offset="50%" stop-color="#060b18"/>
      <stop offset="100%" stop-color="#030612"/>
    </linearGradient>
    <!-- Aurora layers -->
    <radialGradient id="a1" cx="15%" cy="40%" r="55%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#7c3aed" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="a2" cx="85%" cy="25%" r="50%">
      <stop offset="0%" stop-color="#1e40af" stop-opacity="0.45"/>
      <stop offset="100%" stop-color="#1e40af" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="a3" cx="50%" cy="90%" r="45%">
      <stop offset="0%" stop-color="#064e3b" stop-opacity="0.35"/>
      <stop offset="100%" stop-color="#064e3b" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="a4" cx="60%" cy="10%" r="40%">
      <stop offset="0%" stop-color="#9f1239" stop-opacity="0.2"/>
      <stop offset="100%" stop-color="#9f1239" stop-opacity="0"/>
    </radialGradient>
    <!-- Name text gradient -->
    <linearGradient id="nameGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#c084fc"/>
      <stop offset="30%"  stop-color="#818cf8"/>
      <stop offset="60%"  stop-color="#38bdf8"/>
      <stop offset="85%"  stop-color="#34d399"/>
      <stop offset="100%" stop-color="#fb7185"/>
    </linearGradient>
    <!-- Subtitle gradient -->
    <linearGradient id="subGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#a78bfa"/>
      <stop offset="50%"  stop-color="#60a5fa"/>
      <stop offset="100%" stop-color="#4ade80"/>
    </linearGradient>
    <!-- Meteor trails -->
    <linearGradient id="met1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#c4b5fd" stop-opacity="0"/>
      <stop offset="60%" stop-color="#c4b5fd" stop-opacity="0.7"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="1"/>
    </linearGradient>
    <linearGradient id="met2" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7dd3fc" stop-opacity="0"/>
      <stop offset="60%" stop-color="#7dd3fc" stop-opacity="0.65"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="1"/>
    </linearGradient>
    <linearGradient id="met3" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#f9a8d4" stop-opacity="0"/>
      <stop offset="60%" stop-color="#f9a8d4" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="1"/>
    </linearGradient>
    <linearGradient id="met4" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#6ee7b7" stop-opacity="0"/>
      <stop offset="60%" stop-color="#6ee7b7" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="1"/>
    </linearGradient>
    <!-- Glow filters -->
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="2.5" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="bigGlow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="8" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="nameGlow" x="-10%" y="-40%" width="120%" height="180%">
      <feGaussianBlur stdDeviation="12" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <!-- Clip for meteors -->
    <clipPath id="clip"><rect width="900" height="320"/></clipPath>
  </defs>

  <!-- Background -->
  <rect width="900" height="320" fill="url(#bg)"/>

  <!-- Aurora blobs -->
  <rect width="900" height="320" fill="url(#a1)">
    <animate attributeName="opacity" values="0.8;1;0.8" dur="7s" repeatCount="indefinite"/>
  </rect>
  <rect width="900" height="320" fill="url(#a2)">
    <animate attributeName="opacity" values="1;0.5;1" dur="9s" repeatCount="indefinite"/>
  </rect>
  <rect width="900" height="320" fill="url(#a3)">
    <animate attributeName="opacity" values="0.5;1;0.5" dur="11s" repeatCount="indefinite"/>
  </rect>
  <rect width="900" height="320" fill="url(#a4)">
    <animate attributeName="opacity" values="0.6;1;0.6" dur="6s" repeatCount="indefinite"/>
  </rect>

  <!-- ── STAR FIELD ── -->
  <g clip-path="url(#clip)">
    <!-- White stars -->
    <g fill="white">
      <circle cx="34"  cy="14"  r="1.1"><animate attributeName="opacity" values="0.9;0.1;0.9" dur="2.3s" repeatCount="indefinite"/></circle>
      <circle cx="112" cy="38"  r="0.8"><animate attributeName="opacity" values="0.3;1;0.3"   dur="3.7s" repeatCount="indefinite"/></circle>
      <circle cx="195" cy="11"  r="1.3"><animate attributeName="opacity" values="1;0.2;1"     dur="1.9s" repeatCount="indefinite"/></circle>
      <circle cx="258" cy="52"  r="0.7"><animate attributeName="opacity" values="0.2;0.9;0.2" dur="4.1s" repeatCount="indefinite"/></circle>
      <circle cx="333" cy="19"  r="1.0"><animate attributeName="opacity" values="0.8;0.2;0.8" dur="2.8s" repeatCount="indefinite"/></circle>
      <circle cx="415" cy="37"  r="1.2"><animate attributeName="opacity" values="0.1;1;0.1"   dur="1.6s" repeatCount="indefinite"/></circle>
      <circle cx="492" cy="13"  r="0.9"><animate attributeName="opacity" values="1;0.3;1"     dur="3.2s" repeatCount="indefinite"/></circle>
      <circle cx="568" cy="48"  r="1.1"><animate attributeName="opacity" values="0.4;1;0.4"   dur="2.5s" repeatCount="indefinite"/></circle>
      <circle cx="634" cy="17"  r="0.8"><animate attributeName="opacity" values="0.9;0.2;0.9" dur="3.9s" repeatCount="indefinite"/></circle>
      <circle cx="705" cy="42"  r="1.3"><animate attributeName="opacity" values="0.2;0.9;0.2" dur="2.1s" repeatCount="indefinite"/></circle>
      <circle cx="774" cy="16"  r="0.7"><animate attributeName="opacity" values="1;0.1;1"     dur="4.6s" repeatCount="indefinite"/></circle>
      <circle cx="843" cy="35"  r="1.1"><animate attributeName="opacity" values="0.5;1;0.5"   dur="2.0s" repeatCount="indefinite"/></circle>
      <circle cx="876" cy="10"  r="0.9"><animate attributeName="opacity" values="0.1;0.9;0.1" dur="3.4s" repeatCount="indefinite"/></circle>
      <circle cx="28"  cy="68"  r="0.8"><animate attributeName="opacity" values="0.7;0.1;0.7" dur="2.7s" repeatCount="indefinite"/></circle>
      <circle cx="84"  cy="88"  r="1.0"><animate attributeName="opacity" values="0.2;1;0.2"   dur="1.8s" repeatCount="indefinite"/></circle>
      <circle cx="148" cy="72"  r="0.7"><animate attributeName="opacity" values="0.9;0.3;0.9" dur="4.3s" repeatCount="indefinite"/></circle>
      <circle cx="222" cy="93"  r="1.2"><animate attributeName="opacity" values="0.1;0.8;0.1" dur="2.4s" repeatCount="indefinite"/></circle>
      <circle cx="302" cy="77"  r="0.9"><animate attributeName="opacity" values="1;0.3;1"     dur="3.1s" repeatCount="indefinite"/></circle>
      <circle cx="378" cy="97"  r="0.7"><animate attributeName="opacity" values="0.4;1;0.4"   dur="2.6s" repeatCount="indefinite"/></circle>
      <circle cx="454" cy="69"  r="1.1"><animate attributeName="opacity" values="0.8;0.1;0.8" dur="1.7s" repeatCount="indefinite"/></circle>
      <circle cx="533" cy="85"  r="0.8"><animate attributeName="opacity" values="0.1;0.9;0.1" dur="3.5s" repeatCount="indefinite"/></circle>
      <circle cx="608" cy="67"  r="0.9"><animate attributeName="opacity" values="0.6;1;0.6"   dur="2.2s" repeatCount="indefinite"/></circle>
      <circle cx="682" cy="90"  r="0.7"><animate attributeName="opacity" values="0.9;0.1;0.9" dur="4.0s" repeatCount="indefinite"/></circle>
      <circle cx="752" cy="73"  r="1.2"><animate attributeName="opacity" values="0.2;0.8;0.2" dur="3.0s" repeatCount="indefinite"/></circle>
      <circle cx="822" cy="92"  r="0.8"><animate attributeName="opacity" values="1;0.2;1"     dur="1.8s" repeatCount="indefinite"/></circle>
      <circle cx="55"  cy="280" r="0.9"><animate attributeName="opacity" values="0.4;0.9;0.4" dur="3.3s" repeatCount="indefinite"/></circle>
      <circle cx="145" cy="295" r="1.0"><animate attributeName="opacity" values="0.9;0.1;0.9" dur="2.6s" repeatCount="indefinite"/></circle>
      <circle cx="745" cy="290" r="1.1"><animate attributeName="opacity" values="0.6;0.1;0.6" dur="2.3s" repeatCount="indefinite"/></circle>
      <circle cx="835" cy="280" r="0.8"><animate attributeName="opacity" values="0.2;1;0.2"   dur="3.8s" repeatCount="indefinite"/></circle>
      <circle cx="885" cy="300" r="1.0"><animate attributeName="opacity" values="0.8;0.1;0.8" dur="2.0s" repeatCount="indefinite"/></circle>
    </g>
    <!-- Violet stars -->
    <g fill="#c4b5fd">
      <circle cx="70"  cy="28"  r="1.0"><animate attributeName="opacity" values="0.5;1;0.5" dur="2.4s" repeatCount="indefinite"/></circle>
      <circle cx="176" cy="57"  r="0.8"><animate attributeName="opacity" values="1;0.2;1"   dur="3.6s" repeatCount="indefinite"/></circle>
      <circle cx="454" cy="27"  r="1.1"><animate attributeName="opacity" values="0.3;1;0.3" dur="2.0s" repeatCount="indefinite"/></circle>
      <circle cx="654" cy="57"  r="0.9"><animate attributeName="opacity" values="0.8;0.1;0.8" dur="4.4s" repeatCount="indefinite"/></circle>
      <circle cx="815" cy="28"  r="1.0"><animate attributeName="opacity" values="0.1;0.9;0.1" dur="2.9s" repeatCount="indefinite"/></circle>
    </g>
    <!-- Blue stars -->
    <g fill="#7dd3fc">
      <circle cx="127" cy="23"  r="0.9"><animate attributeName="opacity" values="0.7;0.1;0.7" dur="3.1s" repeatCount="indefinite"/></circle>
      <circle cx="354" cy="62"  r="1.1"><animate attributeName="opacity" values="0.2;1;0.2"   dur="2.5s" repeatCount="indefinite"/></circle>
      <circle cx="594" cy="33"  r="0.8"><animate attributeName="opacity" values="1;0.3;1"     dur="1.8s" repeatCount="indefinite"/></circle>
      <circle cx="744" cy="63"  r="1.2"><animate attributeName="opacity" values="0.4;0.9;0.4" dur="4.0s" repeatCount="indefinite"/></circle>
    </g>
    <!-- Green stars -->
    <g fill="#6ee7b7">
      <circle cx="290" cy="30"  r="0.8"><animate attributeName="opacity" values="0.3;0.9;0.3" dur="3.8s" repeatCount="indefinite"/></circle>
      <circle cx="530" cy="20"  r="1.0"><animate attributeName="opacity" values="0.8;0.1;0.8" dur="2.2s" repeatCount="indefinite"/></circle>
      <circle cx="860" cy="55"  r="0.7"><animate attributeName="opacity" values="0.2;0.8;0.2" dur="4.7s" repeatCount="indefinite"/></circle>
    </g>

    <!-- ── METEORS ── -->
    <!-- Meteor 1: violet -->
    <g opacity="0" clip-path="url(#clip)">
      <animateTransform attributeName="transform" type="translate" values="-180,-20; 1080,290" dur="2.6s" begin="1s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.04;0.1;0.8;1" dur="2.6s" begin="1s" repeatCount="indefinite"/>
      <line x1="-150" y1="0" x2="0" y2="0" stroke="url(#met1)" stroke-width="1.8" transform="rotate(27)"/>
      <circle cx="0" cy="0" r="2.2" fill="white" filter="url(#glow)"/>
    </g>
    <!-- Meteor 2: blue -->
    <g opacity="0" clip-path="url(#clip)">
      <animateTransform attributeName="transform" type="translate" values="-140,30; 1040,295" dur="2.3s" begin="4.5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.05;0.12;0.78;1" dur="2.3s" begin="4.5s" repeatCount="indefinite"/>
      <line x1="-120" y1="0" x2="0" y2="0" stroke="url(#met2)" stroke-width="1.5" transform="rotate(25)"/>
      <circle cx="0" cy="0" r="1.8" fill="white" filter="url(#glow)"/>
    </g>
    <!-- Meteor 3: pink -->
    <g opacity="0" clip-path="url(#clip)">
      <animateTransform attributeName="transform" type="translate" values="80,-15; 1060,230" dur="2.0s" begin="8s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.05;0.12;0.75;1" dur="2.0s" begin="8s" repeatCount="indefinite"/>
      <line x1="-110" y1="0" x2="0" y2="0" stroke="url(#met3)" stroke-width="1.4" transform="rotate(24)"/>
      <circle cx="0" cy="0" r="1.7" fill="white" filter="url(#glow)"/>
    </g>
    <!-- Meteor 4: green, fast -->
    <g opacity="0" clip-path="url(#clip)">
      <animateTransform attributeName="transform" type="translate" values="250,-5; 980,200" dur="1.7s" begin="12s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0;0.9;0.9;0" keyTimes="0;0.06;0.14;0.72;1" dur="1.7s" begin="12s" repeatCount="indefinite"/>
      <line x1="-90" y1="0" x2="0" y2="0" stroke="url(#met4)" stroke-width="1.3" transform="rotate(23)"/>
      <circle cx="0" cy="0" r="1.5" fill="#d1fae5" filter="url(#glow)"/>
    </g>
    <!-- Meteor 5: small violet, offset timing -->
    <g opacity="0" clip-path="url(#clip)">
      <animateTransform attributeName="transform" type="translate" values="-60,10; 920,260" dur="1.9s" begin="16s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0;0.8;0.8;0" keyTimes="0;0.06;0.14;0.70;1" dur="1.9s" begin="16s" repeatCount="indefinite"/>
      <line x1="-100" y1="0" x2="0" y2="0" stroke="url(#met1)" stroke-width="1.2" transform="rotate(26)"/>
      <circle cx="0" cy="0" r="1.4" fill="#ede9fe"/>
    </g>
  </g>

  <!-- ── DECORATIVE ORBIT RING ── -->
  <ellipse cx="450" cy="166" rx="310" ry="30" fill="none" stroke="url(#subGrad)" stroke-width="0.4" opacity="0.15"/>
  <ellipse cx="450" cy="166" rx="380" ry="20" fill="none" stroke="url(#nameGrad)" stroke-width="0.3" opacity="0.10"/>

  <!-- ── GLOW HALO behind name ── -->
  <text x="450" y="158" text-anchor="middle"
    font-family="'Trebuchet MS','Segoe UI',Georgia,sans-serif"
    font-size="56" font-weight="900" letter-spacing="-1.5"
    fill="#a78bfa" opacity="0.18" filter="url(#nameGlow)">
    Ritesh Gangurde
  </text>

  <!-- ── MAIN NAME ── -->
  <text x="450" y="158" text-anchor="middle"
    font-family="'Trebuchet MS','Segoe UI',Georgia,sans-serif"
    font-size="56" font-weight="900" letter-spacing="-1.5"
    fill="url(#nameGrad)" filter="url(#glow)">
    <animate attributeName="opacity" values="0;0;1" keyTimes="0;0.3;1" dur="1.5s" fill="freeze"/>
    Ritesh Gangurde
  </text>

  <!-- ── SUBTITLE ── -->
  <text x="450" y="197" text-anchor="middle"
    font-family="'JetBrains Mono','Courier New',monospace"
    font-size="13.5" font-weight="600" letter-spacing="3.5"
    fill="url(#subGrad)" opacity="0.9">
    <animate attributeName="opacity" values="0;0;0.9" keyTimes="0;0.4;1" dur="2.0s" fill="freeze"/>
    FRONT-END  ·  REACT NATIVE  ·  UI/UX  ·  CYBER FORENSICS
  </text>

  <!-- ── TAGLINE ── -->
  <text x="450" y="234" text-anchor="middle"
    font-family="'Trebuchet MS','Segoe UI',sans-serif"
    font-size="10.5" letter-spacing="5.5"
    fill="#6ee7b7" opacity="0">
    <animate attributeName="opacity" values="0;0.55" dur="3s" begin="0.8s" fill="freeze"/>
    ✦  TURNING IDEAS INTO IMPACTFUL SOFTWARE  ✦
  </text>

  <!-- ── DIVIDER LINE ── -->
  <line x1="450" y1="172" x2="450" y2="172" stroke="url(#nameGrad)" stroke-width="0.6" opacity="0.3">
    <animate attributeName="x1" values="450;160" dur="1.6s" begin="0.2s" fill="freeze"/>
    <animate attributeName="x2" values="450;740" dur="1.6s" begin="0.2s" fill="freeze"/>
  </line>

  <!-- ── FLOATING TECH ORBS ── -->
  <!-- Left cluster -->
  <circle cx="138" cy="166" r="3" fill="#c084fc" opacity="0" filter="url(#glow)">
    <animate attributeName="opacity" values="0;0.7;0.4;0.7;0" dur="4s" begin="1.5s" repeatCount="indefinite"/>
    <animate attributeName="cy" values="166;160;166;172;166" dur="4s" begin="1.5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="110" cy="155" r="2" fill="#818cf8" opacity="0" filter="url(#glow)">
    <animate attributeName="opacity" values="0;0.5;0.3;0.5;0" dur="5s" begin="2s" repeatCount="indefinite"/>
    <animate attributeName="cy" values="155;149;155;161;155" dur="5s" begin="2s" repeatCount="indefinite"/>
  </circle>
  <!-- Right cluster -->
  <circle cx="762" cy="166" r="3" fill="#38bdf8" opacity="0" filter="url(#glow)">
    <animate attributeName="opacity" values="0;0.7;0.4;0.7;0" dur="4.5s" begin="1.8s" repeatCount="indefinite"/>
    <animate attributeName="cy" values="166;160;166;172;166" dur="4.5s" begin="1.8s" repeatCount="indefinite"/>
  </circle>
  <circle cx="790" cy="152" r="2" fill="#34d399" opacity="0" filter="url(#glow)">
    <animate attributeName="opacity" values="0;0.5;0.3;0.5;0" dur="3.8s" begin="2.5s" repeatCount="indefinite"/>
    <animate attributeName="cy" values="152;146;152;158;152" dur="3.8s" begin="2.5s" repeatCount="indefinite"/>
  </circle>
</svg>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=20&duration=2800&pause=900&color=A78BFA&center=true&vCenter=true&multiline=false&width=640&lines=Hey+there!+I'm+Ritesh+%F0%9F%91%8B;Front-End+Developer+%F0%9F%9A%80;React+Native+Builder+%F0%9F%93%B1;Hackathon+Enthusiast+%F0%9F%8F%86;UI%2FUX+Craftsman+%F0%9F%8E%A8;Cyber+Forensics+Explorer+%F0%9F%94%90)](https://git.io/typing-svg)

<br/>

[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/Diablo6529)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ritesh-gangurde-7b93b9227)
[![GitHub](https://img.shields.io/badge/GitHub-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RiteshGangurde)

</div>

<!--═══════════════════════ WAVE DIVIDER ═══════════════════════-->

<div align="center">
<svg width="900" height="60" viewBox="0 0 900 60" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="waveGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#7c3aed" stop-opacity="0.8"/>
      <stop offset="25%"  stop-color="#2563eb" stop-opacity="0.7"/>
      <stop offset="50%"  stop-color="#0891b2" stop-opacity="0.8"/>
      <stop offset="75%"  stop-color="#059669" stop-opacity="0.7"/>
      <stop offset="100%" stop-color="#7c3aed" stop-opacity="0.8"/>
    </linearGradient>
    <linearGradient id="waveGrad2" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#a78bfa" stop-opacity="0.4"/>
      <stop offset="50%"  stop-color="#38bdf8" stop-opacity="0.5"/>
      <stop offset="100%" stop-color="#a78bfa" stop-opacity="0.4"/>
    </linearGradient>
  </defs>
  <path d="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30" fill="none" stroke="url(#waveGrad)" stroke-width="2">
    <animate attributeName="d"
      values="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30;
              M0,30 C150,50 300,10 450,30 C600,50 750,10 900,30;
              M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30"
      dur="5s" repeatCount="indefinite"/>
  </path>
  <path d="M0,38 C150,20 300,56 450,38 C600,20 750,56 900,38" fill="none" stroke="url(#waveGrad2)" stroke-width="1.2">
    <animate attributeName="d"
      values="M0,38 C150,20 300,56 450,38 C600,20 750,56 900,38;
              M0,38 C150,56 300,20 450,38 C600,56 750,20 900,38;
              M0,38 C150,20 300,56 450,38 C600,20 750,56 900,38"
      dur="4s" repeatCount="indefinite"/>
  </path>
</svg>
</div>

## ⚡ About Me

<img align="right" alt="Coding" width="280" src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif"/>

```yaml
╭──────────────────────────────────────╮
│          RITESH  GANGURDE            │
│  ────────────────────────────────    │
│  Role     :  Front-End Developer    │
│  Location :  India  🇮🇳             │
│  Focus    :  React Native + Cyber   │
│  Status   :  Open to Collaborate 🤝 │
│  Passion  :  Ideas → Software ⚡    │
╰──────────────────────────────────────╯
```

🛠 **Currently Building:** Cross-platform food ordering app with React Native  
🌱 **Currently Learning:** Advanced React Native & Cyber Forensics  
🤝 **Open to:** Front-end projects, hackathon teams & freelance  
🧩 **Seeking Help With:** iOS development & cyber forensics deep-dives  
💬 **Ask Me About:** Front-end dev, Smart India Hackathon & UI/UX projects  
⚡ **Fun Fact:** I Valorant main Sage and debug code at 3am simultaneously

<br clear="right"/>

<!--═══════════════════════ WAVE DIVIDER ═══════════════════════-->
<div align="center">
<svg width="900" height="60" viewBox="0 0 900 60" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="wg3" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#7c3aed" stop-opacity="0.8"/>
      <stop offset="50%"  stop-color="#0891b2" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#7c3aed" stop-opacity="0.8"/>
    </linearGradient>
  </defs>
  <path d="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30" fill="none" stroke="url(#wg3)" stroke-width="2">
    <animate attributeName="d"
      values="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30;M0,30 C150,50 300,10 450,30 C600,50 750,10 900,30;M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30"
      dur="5s" repeatCount="indefinite"/>
  </path>
</svg>
</div>

## 🧰 Tech Stack

<!--═══════════════════════ TECH STACK SVG ═══════════════════════-->
<div align="center">

<svg width="860" height="300" viewBox="0 0 860 300" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="cardBg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0f0f1a"/>
      <stop offset="100%" stop-color="#0a0a14"/>
    </linearGradient>
    <linearGradient id="cardBorder" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.6"/>
      <stop offset="50%" stop-color="#0891b2" stop-opacity="0.5"/>
      <stop offset="100%" stop-color="#059669" stop-opacity="0.4"/>
    </linearGradient>
    <linearGradient id="sectionLabel" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#a78bfa"/>
      <stop offset="100%" stop-color="#38bdf8"/>
    </linearGradient>
    <filter id="subtleGlow">
      <feGaussianBlur stdDeviation="1.5" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <!-- Card background -->
  <rect x="0" y="0" width="860" height="300" rx="16" fill="url(#cardBg)" stroke="url(#cardBorder)" stroke-width="1"/>

  <!-- Section: Languages -->
  <text x="30" y="36" font-family="'JetBrains Mono',monospace" font-size="11" font-weight="700" letter-spacing="2" fill="url(#sectionLabel)" filter="url(#subtleGlow)">LANGUAGES</text>
  <line x1="30" y1="42" x2="240" y2="42" stroke="url(#sectionLabel)" stroke-width="0.5" opacity="0.5"/>

  <!-- Language tags -->
  <!-- C -->
  <rect x="30" y="52" width="52" height="24" rx="6" fill="#00599C" opacity="0.85"/>
  <text x="56" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">C</text>
  <!-- C++ -->
  <rect x="90" y="52" width="52" height="24" rx="6" fill="#00599C" opacity="0.85"/>
  <text x="116" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">C++</text>
  <!-- C# -->
  <rect x="150" y="52" width="52" height="24" rx="6" fill="#239120" opacity="0.85"/>
  <text x="176" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">C#</text>
  <!-- JS -->
  <rect x="210" y="52" width="52" height="24" rx="6" fill="#F7DF1E" opacity="0.9"/>
  <text x="236" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#1a1a00">JS</text>
  <!-- Java -->
  <rect x="270" y="52" width="52" height="24" rx="6" fill="#ED8B00" opacity="0.85"/>
  <text x="296" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">Java</text>
  <!-- Kotlin -->
  <rect x="330" y="52" width="60" height="24" rx="6" fill="#7F52FF" opacity="0.85"/>
  <text x="360" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">Kotlin</text>
  <!-- PHP -->
  <rect x="398" y="52" width="52" height="24" rx="6" fill="#777BB4" opacity="0.85"/>
  <text x="424" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">PHP</text>
  <!-- HTML5 -->
  <rect x="458" y="52" width="60" height="24" rx="6" fill="#E34F26" opacity="0.85"/>
  <text x="488" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">HTML5</text>
  <!-- CSS3 -->
  <rect x="526" y="52" width="58" height="24" rx="6" fill="#1572B6" opacity="0.85"/>
  <text x="555" y="69" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="white">CSS3</text>

  <!-- Section: Frameworks -->
  <text x="30" y="104" font-family="'JetBrains Mono',monospace" font-size="11" font-weight="700" letter-spacing="2" fill="url(#sectionLabel)" filter="url(#subtleGlow)">FRAMEWORKS &amp; RUNTIMES</text>
  <line x1="30" y1="110" x2="340" y2="110" stroke="url(#sectionLabel)" stroke-width="0.5" opacity="0.5"/>

  <!-- React -->
  <rect x="30" y="120" width="70" height="24" rx="6" fill="#61DAFB" opacity="0.2" stroke="#61DAFB" stroke-width="0.8"/>
  <text x="65" y="137" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#61DAFB">React</text>
  <!-- React Native -->
  <rect x="108" y="120" width="104" height="24" rx="6" fill="#61DAFB" opacity="0.15" stroke="#61DAFB" stroke-width="0.8"/>
  <text x="160" y="137" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#61DAFB">React Native</text>
  <!-- Next.js -->
  <rect x="220" y="120" width="70" height="24" rx="6" fill="#ffffff" opacity="0.08" stroke="#ffffff" stroke-width="0.8"/>
  <text x="255" y="137" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#e2e8f0">Next.js</text>
  <!-- Node.js -->
  <rect x="298" y="120" width="70" height="24" rx="6" fill="#6DA55F" opacity="0.2" stroke="#6DA55F" stroke-width="0.8"/>
  <text x="333" y="137" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#86efac">Node.js</text>
  <!-- Flutter -->
  <rect x="376" y="120" width="66" height="24" rx="6" fill="#02569B" opacity="0.4" stroke="#54C5F8" stroke-width="0.8"/>
  <text x="409" y="137" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#7dd3fc">Flutter</text>
  <!-- Tailwind -->
  <rect x="450" y="120" width="76" height="24" rx="6" fill="#38B2AC" opacity="0.2" stroke="#38B2AC" stroke-width="0.8"/>
  <text x="488" y="137" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#5eead4">Tailwind</text>
  <!-- Firebase -->
  <rect x="534" y="120" width="74" height="24" rx="6" fill="#FFCA28" opacity="0.15" stroke="#FFCA28" stroke-width="0.8"/>
  <text x="571" y="137" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#fde68a">Firebase</text>

  <!-- Section: Databases -->
  <text x="30" y="172" font-family="'JetBrains Mono',monospace" font-size="11" font-weight="700" letter-spacing="2" fill="url(#sectionLabel)" filter="url(#subtleGlow)">DATABASES</text>
  <line x1="30" y1="178" x2="180" y2="178" stroke="url(#sectionLabel)" stroke-width="0.5" opacity="0.5"/>

  <rect x="30" y="188" width="68" height="24" rx="6" fill="#4479A1" opacity="0.3" stroke="#4479A1" stroke-width="0.8"/>
  <text x="64" y="205" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#93c5fd">MySQL</text>
  <rect x="106" y="188" width="80" height="24" rx="6" fill="#4ea94b" opacity="0.2" stroke="#4ea94b" stroke-width="0.8"/>
  <text x="146" y="205" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#86efac">MongoDB</text>
  <rect x="194" y="188" width="66" height="24" rx="6" fill="#07405e" opacity="0.5" stroke="#38bdf8" stroke-width="0.8"/>
  <text x="227" y="205" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#7dd3fc">SQLite</text>

  <!-- Section: Design -->
  <text x="30" y="238" font-family="'JetBrains Mono',monospace" font-size="11" font-weight="700" letter-spacing="2" fill="url(#sectionLabel)" filter="url(#subtleGlow)">DESIGN &amp; TOOLS</text>
  <line x1="30" y1="244" x2="220" y2="244" stroke="url(#sectionLabel)" stroke-width="0.5" opacity="0.5"/>

  <rect x="30" y="254" width="60" height="24" rx="6" fill="#F24E1E" opacity="0.2" stroke="#F24E1E" stroke-width="0.8"/>
  <text x="60" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#fb923c">Figma</text>
  <rect x="98" y="254" width="80" height="24" rx="6" fill="#31A8FF" opacity="0.2" stroke="#31A8FF" stroke-width="0.8"/>
  <text x="138" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#7dd3fc">Photoshop</text>
  <rect x="186" y="254" width="80" height="24" rx="6" fill="#FF9A00" opacity="0.2" stroke="#FF9A00" stroke-width="0.8"/>
  <text x="226" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#fde68a">Illustrator</text>
  <rect x="274" y="254" width="54" height="24" rx="6" fill="#F5792A" opacity="0.2" stroke="#F5792A" stroke-width="0.8"/>
  <text x="301" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#fed7aa">Blender</text>
  <rect x="336" y="254" width="60" height="24" rx="6" fill="#F05033" opacity="0.2" stroke="#F05033" stroke-width="0.8"/>
  <text x="366" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#fca5a5">Git</text>
  <rect x="404" y="254" width="66" height="24" rx="6" fill="#181717" opacity="0.6" stroke="#94a3b8" stroke-width="0.8"/>
  <text x="437" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#e2e8f0">GitHub</text>
  <rect x="478" y="254" width="66" height="24" rx="6" fill="#000000" opacity="0.5" stroke="#94a3b8" stroke-width="0.8"/>
  <text x="511" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#e2e8f0">Unity</text>
  <rect x="552" y="254" width="80" height="24" rx="6" fill="#313131" opacity="0.6" stroke="#94a3b8" stroke-width="0.8"/>
  <text x="592" y="271" text-anchor="middle" font-family="monospace" font-size="11" font-weight="700" fill="#e2e8f0">Unreal</text>
</svg>

</div>

<!--═══════════════════════ WAVE DIVIDER ═══════════════════════-->
<div align="center">
<svg width="900" height="60" viewBox="0 0 900 60" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="wg4" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#059669" stop-opacity="0.8"/>
      <stop offset="50%" stop-color="#7c3aed" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#059669" stop-opacity="0.8"/>
    </linearGradient>
  </defs>
  <path d="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30" fill="none" stroke="url(#wg4)" stroke-width="2">
    <animate attributeName="d"
      values="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30;M0,30 C150,50 300,10 450,30 C600,50 750,10 900,30;M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30"
      dur="6s" repeatCount="indefinite"/>
  </path>
</svg>
</div>

## 🚀 Featured Projects

<!--═══════════════════════ PROJECTS SVG ═══════════════════════-->
<div align="center">

<svg width="860" height="380" viewBox="0 0 860 380" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Card gradients -->
    <linearGradient id="card1" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1e1b4b"/>
      <stop offset="100%" stop-color="#0f0f1a"/>
    </linearGradient>
    <linearGradient id="card2" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1a1b2e"/>
      <stop offset="100%" stop-color="#0f0f1a"/>
    </linearGradient>
    <linearGradient id="card3" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0f1f1a"/>
      <stop offset="100%" stop-color="#0f0f1a"/>
    </linearGradient>
    <linearGradient id="card4" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1a0f1f"/>
      <stop offset="100%" stop-color="#0f0f1a"/>
    </linearGradient>
    <linearGradient id="border1" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#818cf8" stop-opacity="0.4"/>
    </linearGradient>
    <linearGradient id="border2" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#2563eb" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#38bdf8" stop-opacity="0.4"/>
    </linearGradient>
    <linearGradient id="border3" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#059669" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#34d399" stop-opacity="0.4"/>
    </linearGradient>
    <linearGradient id="border4" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#9f1239" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#f472b6" stop-opacity="0.4"/>
    </linearGradient>
    <filter id="cardGlow1">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <!-- ── CARD 1: Food App ── -->
  <rect x="10" y="10" width="400" height="170" rx="14" fill="url(#card1)" stroke="url(#border1)" stroke-width="1.2"/>
  <!-- Accent top bar -->
  <rect x="10" y="10" width="400" height="4" rx="2" fill="url(#border1)" opacity="0.8"/>
  <!-- Emoji -->
  <text x="34" y="48" font-size="22">🍔</text>
  <!-- Title -->
  <text x="64" y="46" font-family="'Trebuchet MS',sans-serif" font-size="15" font-weight="700" fill="#c4b5fd">Food Ordering App</text>
  <!-- Badges -->
  <rect x="34" y="56" width="84" height="18" rx="5" fill="#61DAFB" opacity="0.15" stroke="#61DAFB" stroke-width="0.7"/>
  <text x="76" y="69" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#7dd3fc">React Native</text>
  <rect x="124" y="56" width="62" height="18" rx="5" fill="#FFCA28" opacity="0.15" stroke="#FFCA28" stroke-width="0.7"/>
  <text x="155" y="69" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#fde68a">Firebase</text>
  <!-- Description -->
  <text x="34" y="96" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">Cross-platform app with real-time order tracking</text>
  <text x="34" y="112" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">and seamless UI/UX powered by Firebase.</text>
  <!-- Feature bullets -->
  <circle cx="42" cy="134" r="2.5" fill="#c084fc"/>
  <text x="52" y="138" font-family="monospace" font-size="10" fill="#e2e8f0">iOS &amp; Android cross-platform</text>
  <circle cx="42" cy="152" r="2.5" fill="#60a5fa"/>
  <text x="52" y="156" font-family="monospace" font-size="10" fill="#e2e8f0">Secure auth + real-time updates</text>

  <!-- ── CARD 2: Games ── -->
  <rect x="450" y="10" width="400" height="170" rx="14" fill="url(#card2)" stroke="url(#border2)" stroke-width="1.2"/>
  <rect x="450" y="10" width="400" height="4" rx="2" fill="url(#border2)" opacity="0.8"/>
  <text x="474" y="48" font-size="22">🎮</text>
  <text x="504" y="46" font-family="'Trebuchet MS',sans-serif" font-size="15" font-weight="700" fill="#93c5fd">Games Collection</text>
  <rect x="474" y="56" width="80" height="18" rx="5" fill="#F7DF1E" opacity="0.15" stroke="#F7DF1E" stroke-width="0.7"/>
  <text x="514" y="69" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#fef08a">JavaScript</text>
  <rect x="560" y="56" width="52" height="18" rx="5" fill="#E34F26" opacity="0.15" stroke="#E34F26" stroke-width="0.7"/>
  <text x="586" y="69" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#fca5a5">HTML5</text>
  <text x="474" y="96" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">Browser-based games built during internship —</text>
  <text x="474" y="112" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">DOM manipulation, game loops &amp; zero dependencies.</text>
  <circle cx="482" cy="134" r="2.5" fill="#38bdf8"/>
  <text x="492" y="138" font-family="monospace" font-size="10" fill="#e2e8f0">Score tracking + multiple game modes</text>
  <circle cx="482" cy="152" r="2.5" fill="#818cf8"/>
  <text x="492" y="156" font-family="monospace" font-size="10" fill="#e2e8f0">Mobile responsive, pure JS</text>

  <!-- ── CARD 3: Landing Pages ── -->
  <rect x="10" y="200" width="400" height="170" rx="14" fill="url(#card3)" stroke="url(#border3)" stroke-width="1.2"/>
  <rect x="10" y="200" width="400" height="4" rx="2" fill="url(#border3)" opacity="0.8"/>
  <text x="34" y="238" font-size="22">🌐</text>
  <text x="64" y="236" font-family="'Trebuchet MS',sans-serif" font-size="15" font-weight="700" fill="#6ee7b7">Landing Pages &amp; UI</text>
  <rect x="34" y="246" width="52" height="18" rx="5" fill="#61DAFB" opacity="0.15" stroke="#61DAFB" stroke-width="0.7"/>
  <text x="60" y="259" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#7dd3fc">React</text>
  <rect x="92" y="246" width="72" height="18" rx="5" fill="#38B2AC" opacity="0.15" stroke="#38B2AC" stroke-width="0.7"/>
  <text x="128" y="259" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#5eead4">Tailwind</text>
  <text x="34" y="286" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">Production-ready pages &amp; UI components from</text>
  <text x="34" y="302" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">internship, conversion-optimized &amp; pixel-perfect.</text>
  <circle cx="42" cy="324" r="2.5" fill="#34d399"/>
  <text x="52" y="328" font-family="monospace" font-size="10" fill="#e2e8f0">Figma → code, animated layouts</text>
  <circle cx="42" cy="342" r="2.5" fill="#4ade80"/>
  <text x="52" y="346" font-family="monospace" font-size="10" fill="#e2e8f0">Performance optimized builds</text>

  <!-- ── CARD 4: SIH ── -->
  <rect x="450" y="200" width="400" height="170" rx="14" fill="url(#card4)" stroke="url(#border4)" stroke-width="1.2"/>
  <rect x="450" y="200" width="400" height="4" rx="2" fill="url(#border4)" opacity="0.8"/>
  <text x="474" y="238" font-size="22">🏆</text>
  <text x="504" y="236" font-family="'Trebuchet MS',sans-serif" font-size="15" font-weight="700" fill="#f9a8d4">Smart India Hackathon</text>
  <rect x="474" y="246" width="62" height="18" rx="5" fill="#ffffff" opacity="0.08" stroke="#ffffff" stroke-width="0.7"/>
  <text x="505" y="259" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#e2e8f0">Next.js</text>
  <rect x="542" y="246" width="62" height="18" rx="5" fill="#6DA55F" opacity="0.15" stroke="#6DA55F" stroke-width="0.7"/>
  <text x="573" y="259" text-anchor="middle" font-family="monospace" font-size="9.5" fill="#86efac">Node.js</text>
  <text x="474" y="286" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">Hackathon project solving a real government</text>
  <text x="474" y="302" font-family="'Segoe UI',sans-serif" font-size="11" fill="#94a3b8">problem statement — built end-to-end in 36h.</text>
  <circle cx="482" cy="324" r="2.5" fill="#fb7185"/>
  <text x="492" y="328" font-family="monospace" font-size="10" fill="#e2e8f0">Full team collaboration, 36 hours</text>
  <circle cx="482" cy="342" r="2.5" fill="#f472b6"/>
  <text x="492" y="346" font-family="monospace" font-size="10" fill="#e2e8f0">Government problem statement 🇮🇳</text>
</svg>

</div>

<!--═══════════════════════ WAVE DIVIDER ═══════════════════════-->
<div align="center">
<svg width="900" height="60" viewBox="0 0 900 60" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="wg5" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#f59e0b" stop-opacity="0.7"/>
      <stop offset="50%" stop-color="#7c3aed" stop-opacity="0.7"/>
      <stop offset="100%" stop-color="#f59e0b" stop-opacity="0.7"/>
    </linearGradient>
  </defs>
  <path d="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30" fill="none" stroke="url(#wg5)" stroke-width="2">
    <animate attributeName="d"
      values="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30;M0,30 C150,50 300,10 450,30 C600,50 750,10 900,30;M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30"
      dur="5s" repeatCount="indefinite"/>
  </path>
</svg>
</div>

## 🎓 Education & Certifications

<div align="center">

<!--═══════════════════════ EDUCATION SVG ═══════════════════════-->
<svg width="860" height="200" viewBox="0 0 860 200" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="eduBg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0f0a1a"/>
      <stop offset="100%" stop-color="#0a0f1a"/>
    </linearGradient>
    <linearGradient id="eduBorder" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.7"/>
      <stop offset="50%" stop-color="#38bdf8" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#7c3aed" stop-opacity="0.7"/>
    </linearGradient>
    <linearGradient id="progressBar" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7c3aed"/>
      <stop offset="100%" stop-color="#38bdf8"/>
    </linearGradient>
    <linearGradient id="progressBar2" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#059669"/>
      <stop offset="100%" stop-color="#34d399"/>
    </linearGradient>
  </defs>

  <rect x="0" y="0" width="860" height="200" rx="16" fill="url(#eduBg)" stroke="url(#eduBorder)" stroke-width="1"/>

  <!-- Education block -->
  <text x="30" y="38" font-size="18">🎓</text>
  <text x="58" y="38" font-family="'Trebuchet MS',sans-serif" font-size="14" font-weight="700" fill="#c4b5fd">Bachelor of Engineering / B.Tech</text>
  <text x="58" y="56" font-family="'Segoe UI',sans-serif" font-size="12" fill="#94a3b8">Computer Science / Information Technology  ·  India 🇮🇳</text>

  <!-- Divider -->
  <line x1="30" y1="70" x2="830" y2="70" stroke="url(#eduBorder)" stroke-width="0.5" opacity="0.4"/>

  <!-- Cert rows -->
  <!-- Cisco -->
  <text x="30" y="96" font-size="14">📡</text>
  <text x="52" y="96" font-family="monospace" font-size="11" fill="#e2e8f0">Cisco Networking Basics</text>
  <rect x="560" y="82" width="170" height="16" rx="4" fill="#04424a" opacity="0.6"/>
  <rect x="560" y="82" width="170" height="16" rx="4" fill="url(#progressBar2)" opacity="0.7"/>
  <text x="645" y="94" text-anchor="middle" font-family="monospace" font-size="9" font-weight="700" fill="white">✅ COMPLETED</text>

  <!-- Meta -->
  <text x="30" y="122" font-size="14">🔵</text>
  <text x="52" y="122" font-family="monospace" font-size="11" fill="#e2e8f0">Meta Front-End Developer  (Coursera)</text>
  <rect x="560" y="108" width="170" height="16" rx="4" fill="#1e1b4b" opacity="0.6"/>
  <rect x="560" y="108" width="110" height="16" rx="4" fill="url(#progressBar)" opacity="0.7"/>
  <text x="645" y="120" text-anchor="middle" font-family="monospace" font-size="9" font-weight="700" fill="white">🔄 IN PROGRESS</text>

  <!-- Google -->
  <text x="30" y="148" font-size="14">🔐</text>
  <text x="52" y="148" font-family="monospace" font-size="11" fill="#e2e8f0">Google Cybersecurity Certificate</text>
  <rect x="560" y="134" width="170" height="16" rx="4" fill="#1e1b4b" opacity="0.6"/>
  <rect x="560" y="134" width="80" height="16" rx="4" fill="url(#progressBar)" opacity="0.7"/>
  <text x="645" y="146" text-anchor="middle" font-family="monospace" font-size="9" font-weight="700" fill="white">🔄 IN PROGRESS</text>

  <!-- SIH -->
  <text x="30" y="174" font-size="14">🏅</text>
  <text x="52" y="174" font-family="monospace" font-size="11" fill="#e2e8f0">Smart India Hackathon  (Govt. of India)</text>
  <rect x="560" y="160" width="170" height="16" rx="4" fill="#04424a" opacity="0.6"/>
  <rect x="560" y="160" width="170" height="16" rx="4" fill="url(#progressBar2)" opacity="0.7"/>
  <text x="645" y="172" text-anchor="middle" font-family="monospace" font-size="9" font-weight="700" fill="white">✅ PARTICIPATED</text>
</svg>

</div>

<!--═══════════════════════ WAVE DIVIDER ═══════════════════════-->
<div align="center">
<svg width="900" height="60" viewBox="0 0 900 60" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="wg6" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#2563eb" stop-opacity="0.8"/>
      <stop offset="50%" stop-color="#059669" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#2563eb" stop-opacity="0.8"/>
    </linearGradient>
  </defs>
  <path d="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30" fill="none" stroke="url(#wg6)" stroke-width="2">
    <animate attributeName="d"
      values="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30;M0,30 C150,50 300,10 450,30 C600,50 750,10 900,30;M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30"
      dur="7s" repeatCount="indefinite"/>
  </path>
</svg>
</div>

## 📊 GitHub Stats

<div align="center">

<img width="49%" src="https://github-readme-stats.vercel.app/api?username=RiteshGangurde&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=a78bfa&icon_color=60a5fa&text_color=94a3b8&ring_color=a78bfa&include_all_commits=true&count_private=true" />
<img width="49%" src="https://github-readme-streak-stats.herokuapp.com/?user=RiteshGangurde&theme=tokyonight&hide_border=true&background=0d1117&ring=a78bfa&fire=fb923c&currStreakLabel=60a5fa&sideLabels=94a3b8&dates=4e576b&stroke=1e293b" />

<br/><br/>

<img width="42%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=RiteshGangurde&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=a78bfa&text_color=94a3b8&layout=donut" />
<img width="54%" src="https://github-readme-activity-graph.vercel.app/graph?username=RiteshGangurde&bg_color=0d1117&color=a78bfa&line=60a5fa&point=f472b6&area=true&hide_border=true" />

<br/><br/>

![Trophies](https://github-profile-trophy.vercel.app/?username=RiteshGangurde&theme=tokyonight&no-frame=true&no-bg=true&margin-w=6&column=7)

</div>

## 🐍 Contribution Snake

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/RiteshGangurde/RiteshGangurde/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/RiteshGangurde/RiteshGangurde/output/github-snake.svg"/>
  <img alt="github-snake" src="https://raw.githubusercontent.com/RiteshGangurde/RiteshGangurde/output/github-snake-dark.svg"/>
</picture>
</div>

<details>
<summary><b>⚙️ One-time Snake Setup</b></summary>

Create `.github/workflows/snake.yml`:

```yaml
name: Generate Snake
on:
  schedule: [{ cron: "0 0 * * *" }]
  workflow_dispatch:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: RiteshGangurde
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
</details>

<!--═══════════════════════ WAVE DIVIDER ═══════════════════════-->
<div align="center">
<svg width="900" height="60" viewBox="0 0 900 60" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="wg7" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#f472b6" stop-opacity="0.7"/>
      <stop offset="50%" stop-color="#7c3aed" stop-opacity="0.7"/>
      <stop offset="100%" stop-color="#f472b6" stop-opacity="0.7"/>
    </linearGradient>
  </defs>
  <path d="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30" fill="none" stroke="url(#wg7)" stroke-width="2">
    <animate attributeName="d"
      values="M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30;M0,30 C150,50 300,10 450,30 C600,50 750,10 900,30;M0,30 C150,10 300,50 450,30 C600,10 750,50 900,30"
      dur="4.5s" repeatCount="indefinite"/>
  </path>
</svg>
</div>

## 🌐 Let's Connect

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=15&duration=3500&pause=1000&color=34D399&center=true&vCenter=true&width=640&lines=Always+open+to+exciting+projects+%F0%9F%9A%80;Let's+build+something+amazing+together+%F0%9F%A4%9D;Feel+free+to+reach+out+anytime+%F0%9F%91%87)](https://git.io/typing-svg)

<br/>

<a href="https://discord.gg/Diablo6529"><img src="https://img.shields.io/badge/Discord-Chat%20With%20Me-%235865F2?style=for-the-badge&logo=discord&logoColor=white"/></a>
&nbsp;
<a href="https://linkedin.com/in/ritesh-gangurde-7b93b9227"><img src="https://img.shields.io/badge/LinkedIn-Let's%20Connect-%230A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
&nbsp;
<a href="mailto:riteshgangurde@gmail.com"><img src="https://img.shields.io/badge/Gmail-Drop%20a%20Mail-%23EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
&nbsp;
<a href="https://github.com/RiteshGangurde"><img src="https://img.shields.io/badge/GitHub-Follow%20Me-%23181717?style=for-the-badge&logo=github&logoColor=white"/></a>

<br/><br/>

<!--═══════════════════════ CONNECT CARD SVG ═══════════════════════-->
<svg width="600" height="140" viewBox="0 0 600 140" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="connectBg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0f0f1a"/>
      <stop offset="100%" stop-color="#0a0a14"/>
    </linearGradient>
    <linearGradient id="connectBorder" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.6"/>
      <stop offset="50%" stop-color="#38bdf8" stop-opacity="0.5"/>
      <stop offset="100%" stop-color="#34d399" stop-opacity="0.5"/>
    </linearGradient>
  </defs>
  <rect x="0" y="0" width="600" height="140" rx="14" fill="url(#connectBg)" stroke="url(#connectBorder)" stroke-width="1"/>
  <text x="300" y="30" text-anchor="middle" font-family="'JetBrains Mono',monospace" font-size="11" font-weight="700" letter-spacing="3" fill="#a78bfa">OPEN TO</text>
  <circle cx="52" cy="62" r="4" fill="#c084fc" opacity="0.8"/>
  <text x="66" y="66" font-family="'Segoe UI',sans-serif" font-size="12" fill="#e2e8f0">💡 Freelance &amp; collaboration opportunities</text>
  <circle cx="52" cy="88" r="4" fill="#38bdf8" opacity="0.8"/>
  <text x="66" y="92" font-family="'Segoe UI',sans-serif" font-size="12" fill="#e2e8f0">🏆 Hackathon teammates — let's compete!</text>
  <circle cx="52" cy="114" r="4" fill="#34d399" opacity="0.8"/>
  <text x="66" y="118" font-family="'Segoe UI',sans-serif" font-size="12" fill="#e2e8f0">📱 React Native projects &amp; cyber forensics talks</text>
</svg>

<br/><br/>

![Profile Views](https://komarev.com/ghpvc/?username=RiteshGangurde&color=a78bfa&style=for-the-badge&label=PROFILE+VIEWS)
![GitHub followers](https://img.shields.io/github/followers/RiteshGangurde?style=for-the-badge&color=60a5fa&labelColor=0d1117&label=FOLLOWERS)
![GitHub stars](https://img.shields.io/github/stars/RiteshGangurde?style=for-the-badge&color=f472b6&labelColor=0d1117&label=TOTAL+STARS)

</div>

<!--═══════════════════════ FOOTER BANNER ═══════════════════════-->

<div align="center">

<!--  Quote  -->
<svg width="860" height="80" viewBox="0 0 860 80" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="quoteBg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0f0a1a"/>
      <stop offset="100%" stop-color="#0a0f14"/>
    </linearGradient>
    <linearGradient id="quoteGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#c084fc"/>
      <stop offset="50%" stop-color="#38bdf8"/>
      <stop offset="100%" stop-color="#34d399"/>
    </linearGradient>
  </defs>
  <rect x="0" y="0" width="860" height="80" rx="12" fill="url(#quoteBg)" stroke="url(#quoteGrad)" stroke-width="0.8" opacity="0.7"/>
  <text x="30" y="28" font-size="22" opacity="0.4" fill="#c084fc">"</text>
  <text x="430" y="36" text-anchor="middle" font-family="'Trebuchet MS','Segoe UI',sans-serif" font-size="13" fill="url(#quoteGrad)" font-style="italic">Passionate about solving real-world problems through technology and innovation —</text>
  <text x="430" y="56" text-anchor="middle" font-family="'Trebuchet MS','Segoe UI',sans-serif" font-size="13" fill="url(#quoteGrad)" font-style="italic">turning bold ideas into impactful, elegant software.</text>
  <text x="830" y="70" font-size="22" opacity="0.4" fill="#34d399">"</text>
</svg>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&animation=fadeIn" width="100%"/>

</div>
