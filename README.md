<img width="1000" height="320" alt="corvo-profile-animation-20s-matrix" src="https://github.com/user-attachments/assets/1e0b53a4-8a65-45ce-8968-9839a3d491cb" />

##  Core Technologies

<div align="center"><svg xmlns="http://www.w3.org/2000/svg" width="1000" height="320" viewBox="0 0 1000 320">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0d0f10"/>
      <stop offset="55%" stop-color="#151819"/>
      <stop offset="100%" stop-color="#0a0c0d"/>
    </linearGradient>

    <filter id="softGlow" x="-40%" y="-40%" width="180%" height="180%">
      <feGaussianBlur stdDeviation="1.6" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <style>
      .stroke {
        fill: none;
        stroke: #d7dbdc;
        stroke-width: 2.2;
        stroke-linecap: round;
        stroke-linejoin: round;
      }

      .logo-draw {
        stroke-dasharray: 600;
        stroke-dashoffset: 600;
        animation: draw 20s ease-in-out infinite;
      }

      .ray-draw {
        stroke-dasharray: 80;
        stroke-dashoffset: 80;
        animation: rays 20s ease-in-out infinite;
      }

      .fade-1, .fade-2, .fade-3, .fade-4 {
        opacity: 0;
        animation-duration: 20s;
        animation-iteration-count: infinite;
      }

      .fade-1 { animation-name: fade1; }
      .fade-2 { animation-name: fade2; }
      .fade-3 { animation-name: fade3; }
      .fade-4 { animation-name: fade4; }

      .cursor {
        opacity: 0;
        animation: cursor 1s steps(1,end) infinite;
      }

      .green {
        fill: #7fdc9a;
      }

      .text {
        fill: #d6d9da;
        font-family: "IBM Plex Mono", "JetBrains Mono", "DejaVu Sans Mono", monospace;
        letter-spacing: 0.8px;
      }

      .muted {
        fill: #8f979a;
      }

      @keyframes draw {
        0%, 8%   { stroke-dashoffset: 600; opacity: 0; }
        12%      { opacity: 1; }
        30%, 86% { stroke-dashoffset: 0; opacity: 1; }
        96%,100% { opacity: 0; }
      }

      @keyframes rays {
        0%, 14%  { stroke-dashoffset: 80; opacity: 0; }
        20%      { opacity: 1; }
        34%, 86% { stroke-dashoffset: 0; opacity: 1; }
        96%,100% { opacity: 0; }
      }

      @keyframes fade1 {
        0%, 28% { opacity: 0; transform: translateY(4px); }
        34%, 86% { opacity: 1; transform: translateY(0); }
        96%,100% { opacity: 0; }
      }

      @keyframes fade2 {
        0%, 38% { opacity: 0; transform: translateY(4px); }
        44%, 86% { opacity: 1; transform: translateY(0); }
        96%,100% { opacity: 0; }
      }

      @keyframes fade3 {
        0%, 48% { opacity: 0; transform: translateY(4px); }
        54%, 86% { opacity: 1; transform: translateY(0); }
        96%,100% { opacity: 0; }
      }

      @keyframes fade4 {
        0%, 58% { opacity: 0; transform: translateY(4px); }
        64%, 86% { opacity: 1; transform: translateY(0); }
        96%,100% { opacity: 0; }
      }

      @keyframes cursor {
        0%, 49% { opacity: 1; }
        50%,100% { opacity: 0; }
      }

      @keyframes pulse {
        0%, 35%, 86%,100% { opacity: 0.55; transform: scale(0.96); }
        48%, 70% { opacity: 1; transform: scale(1.04); }
      }

      .pupil {
        transform-origin: 220px 127px;
        animation: pulse 20s ease-in-out infinite;
      }

      .eye-pupil {
        transform-origin: 150px 101px;
        animation: pupilMove 20s ease-in-out infinite;
      }

      @keyframes pupilMove {
        0%, 30%   { transform: translate(0px,0px); }
        42%       { transform: translate(7px,-1px); }
        54%       { transform: translate(-6px,2px); }
        66%       { transform: translate(4px,1px); }
        78%,100%  { transform: translate(0px,0px); }
      }

      .matrix-error {
        opacity: 0;
        animation: matrixError 5s steps(1,end) infinite;
        pointer-events: none;
      }

      .matrix-code {
        fill: #55ff72;
        font-family: "IBM Plex Mono", "JetBrains Mono", "DejaVu Sans Mono", monospace;
        font-size: 11px;
        letter-spacing: 3px;
      }

      .matrix-scan {
        fill: #55ff72;
        opacity: .08;
      }

      .glitch-cut {
        fill: #55ff72;
        opacity: .12;
      }

      @keyframes matrixError {
        0%, 86% { opacity: 0; transform: translate(0,0) skewX(0deg); }
        87%     { opacity: .08; transform: translate(-7px,0) skewX(-2deg); }
        88%     { opacity: .24; transform: translate(10px,-1px) skewX(3deg); }
        89%     { opacity: .04; transform: translate(-3px,2px) skewX(0deg); }
        90%     { opacity: .18; transform: translate(6px,-2px) skewX(-1deg); }
        91%     { opacity: .28; transform: translate(-9px,1px) skewX(2deg); }
        92%     { opacity: .06; transform: translate(2px,0) skewX(0deg); }
        93%,100%{ opacity: 0; transform: translate(0,0) skewX(0deg); }
      }

    </style>
  </defs>

  <!-- Background -->
  <rect width="1000" height="320" rx="22" fill="url(#bg)"/>
  <rect x="1" y="1" width="998" height="318" rx="21" fill="none" stroke="#24292b" stroke-width="2"/>


  <!-- MATRIX ERROR overlay: brief full-canvas interference every 6 seconds -->
  <g class="matrix-error">
    <rect class="glitch-cut" x="0" y="92" width="1000" height="5"/>
    <rect class="glitch-cut" x="0" y="164" width="1000" height="3"/>
    <rect class="glitch-cut" x="0" y="251" width="1000" height="4"/>

    <rect class="matrix-scan" x="0" y="26" width="1000" height="2"/>
    <rect class="matrix-scan" x="0" y="71" width="1000" height="1"/>
    <rect class="matrix-scan" x="0" y="119" width="1000" height="3"/>
    <rect class="matrix-scan" x="0" y="176" width="1000" height="1"/>
    <rect class="matrix-scan" x="0" y="238" width="1000" height="2"/>
    <rect class="matrix-scan" x="0" y="289" width="1000" height="1"/>

    <text class="matrix-code" x="22" y="42">01 10 00 11 01 ERROR 0xC0RVO 101 00 11 0101</text>
    <text class="matrix-code" x="516" y="62">1100 01 101 0 NULL 11 0010 1</text>
    <text class="matrix-code" x="72" y="96">010101 11 0 SYS::FAULT 001 10110 00</text>
    <text class="matrix-code" x="600" y="116">1 00 11 MATRIX 010 101 00 1</text>
    <text class="matrix-code" x="18" y="154">101 0 0011 10 0xFF 0101 ERROR 11 00</text>
    <text class="matrix-code" x="544" y="181">001 1010 11 RETRY 0 0 101 011</text>
    <text class="matrix-code" x="88" y="216">10 001 111 0 SIGNAL_LOST 010 11 00</text>
    <text class="matrix-code" x="638" y="244">0110 1 00 101 ERROR 0101 11</text>
    <text class="matrix-code" x="24" y="279">10101 00 11 010 CORRUPT 1 001 110</text>
    <text class="matrix-code" x="534" y="305">00 101 11 0 0101 1 00 110</text>
  </g>


  <!-- LEFT: animated logo -->
  <g transform="translate(70,26)" filter="url(#softGlow)">
    <!-- Eye -->
    <path class="stroke logo-draw" d="M85 101 Q150 52 215 101 Q150 150 85 101 Z"/>
    <circle class="stroke logo-draw" cx="150" cy="101" r="18"/>
    <circle class="stroke pupil eye-pupil" cx="150" cy="101" r="5"
      style="stroke:#7fdc9a;fill:none"/>

    <!-- Rays -->
    <path class="stroke ray-draw" d="M150 12 L150 53"/>
    <path class="stroke ray-draw" d="M128 38 L136 58"/>
    <path class="stroke ray-draw" d="M172 38 L164 58"/>
    <path class="stroke ray-draw" d="M110 50 L122 66"/>
    <path class="stroke ray-draw" d="M190 50 L178 66"/>

    <!-- Hanging stems -->
    <path class="stroke logo-draw" d="M105 117 L105 157"/>
    <path class="stroke logo-draw" d="M150 126 L150 172"/>
    <path class="stroke logo-draw" d="M195 117 L195 157"/>

    <!-- Left feather -->
    <path class="stroke logo-draw" d="M105 157 C86 171 88 196 105 211 C122 196 124 171 105 157 Z"/>
    <path class="stroke logo-draw" d="M105 163 L105 205 M105 173 L96 184 M105 181 L114 191 M105 190 L97 198"/>

    <!-- Center feather -->
    <path class="stroke logo-draw" d="M150 172 C124 194 128 228 150 248 C172 228 176 194 150 172 Z"/>
    <path class="stroke logo-draw" d="M150 179 L150 239 M150 190 L137 205 M150 202 L163 216 M150 217 L138 229"/>

    <!-- Right feather -->
    <path class="stroke logo-draw" d="M195 157 C176 171 178 196 195 211 C212 196 214 171 195 157 Z"/>
    <path class="stroke logo-draw" d="M195 163 L195 205 M195 173 L186 184 M195 181 L204 191 M195 190 L187 198"/>
  </g>

  <!-- Divider -->
  <line x1="390" y1="58" x2="390" y2="262" stroke="#2b3032" stroke-width="1"/>

  <!-- RIGHT: terminal -->
  <g transform="translate(430,62)">
    <text class="text green fade-1" x="0" y="28" font-size="18">&gt; CORVO_</text>

    <text class="text muted fade-2" x="0" y="72" font-size="16">
      Initializing systems...
    </text>

    <text class="text fade-3" x="0" y="116" font-size="21">
      Software Developer | Robotics
    </text>

    <text class="text muted fade-4" x="0" y="158" font-size="15">
      C++ · Python · Rust
    </text>

    <text class="text muted fade-4" x="0" y="195" font-size="14">
      AUTOMATION / ROBOTICS / SIMULATION
    </text>

    <g class="fade-4">
      <rect class="cursor" x="0" y="212" width="10" height="22" rx="1" fill="#7fdc9a"/>
    </g>
  </g>
</svg>


![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2b%2b&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Julia](https://img.shields.io/badge/Julia-9558B2?style=flat-square&logo=julia&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)

</div>

<p align="center">
Simulation · Real-Time Rendering · Systems Automation · Data Processing
</p>

---

##  Featured Projects

Projects focused on **real-time systems, simulation, and scientific software tooling**.

| Project | Description | Tech |
|--------|-------------|------|
| [**UNION**](https://github.com/corvo001/UNION) | Modular ecosystem combining fractals, AI, and real-time rendering for visual and scientific exploration. | C++, Python, Rust, Julia |
| [**DysonSwarm**](https://github.com/corvo001/DysonSphere) | Real-time swarm simulation with visual interpolation and structured pattern export. | C++ |
| [**SoundCloud Downloader**](https://github.com/corvo001/soundcloud-downloader) | Utility tool to download full SoundCloud playlists in real audio. | Python |
| [**Raven**](https://github.com/corvo001/Raven) | Experimental AI environment focused on visual data processing and analysis pipelines. | Python |

---

##  GitHub Stats

<p align="center">
  <img src="https://github-readme-stats-two-beryl-10.vercel.app/api?username=corvo001&show_icons=true&hide_border=true&bg_color=00000000&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9" height="165"/>
  <img src="https://github-readme-stats-two-beryl-10.vercel.app/api/top-langs?username=corvo001&layout=compact&hide_border=true&bg_color=00000000&title_color=58a6ff&text_color=c9d1d9" height="165"/>
</p>

---

##  About Me

I’m Corvo — a systems-oriented developer focused on building **reliable automation and technical software**.

### Current Focus
• Automation of complex and repetitive workflows  
• Developer tooling and productivity systems  
• Systems thinking under real-world constraints  

Background in **simulation, mathematical experimentation, and low-level development**, applied to pragmatic and maintainable software engineering.
