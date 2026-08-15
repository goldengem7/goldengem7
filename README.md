<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500" width="100%" height="100%">
  <defs>
    <style>
      @keyframes swingAction {
        0% { transform: rotate(-22deg); }
        50% { transform: rotate(22deg); }
        100% { transform: rotate(-22deg); }
      }
      @keyframes eyeGlint {
        0%, 90%, 100% { filter: drop-shadow(0 0 4px #FFFFFF); }
        95% { filter: drop-shadow(0 0 12px #38BDF8); }
      }
      @keyframes starTwinkle {
        0%, 100% { opacity: 0.3; }
        50% { opacity: 1; }
      }
      @keyframes webPulse {
        0%, 100% { stroke-opacity: 0.7; stroke-width: 2.5; }
        50% { stroke-opacity: 1; stroke-width: 3.5; }
      }
      .spider-rig {
        transform-origin: 400px 0px;
        animation: swingAction 3.8s ease-in-out infinite;
      }
      .spider-eyes {
        animation: eyeGlint 3s ease-in-out infinite;
      }
      .star-1 { animation: starTwinkle 2s infinite ease-in-out; }
      .star-2 { animation: starTwinkle 3s infinite ease-in-out 1s; }
      .star-3 { animation: starTwinkle 2.5s infinite ease-in-out 0.5s; }
      .web-thread { animation: webPulse 2s infinite ease-in-out; }
    </style>

    <linearGradient id="skyGrad" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#050814" />
      <stop offset="70%" stop-color="#0B132B" />
      <stop offset="100%" stop-color="#1C2541" />
    </linearGradient>

    <linearGradient id="suitRed" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#FF2A42" />
      <stop offset="60%" stop-color="#D90429" />
      <stop offset="100%" stop-color="#7A0012" />
    </linearGradient>

    <linearGradient id="suitBlue" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0066FF" />
      <stop offset="70%" stop-color="#003594" />
      <stop offset="100%" stop-color="#001740" />
    </linearGradient>

    <linearGradient id="buildingGrad1" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#0D1527" />
      <stop offset="100%" stop-color="#050811" />
    </linearGradient>

    <linearGradient id="buildingGrad2" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#152238" />
      <stop offset="100%" stop-color="#090E17" />
    </linearGradient>

    <linearGradient id="moonGlow" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#FFFFFF" />
      <stop offset="100%" stop-color="#E2E8F0" />
    </linearGradient>

    <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="4" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>
  </defs>

  <!-- Sky -->
  <rect width="800" height="500" rx="16" fill="url(#skyGrad)" />

  <!-- Moon & Stars -->
  <g>
    <circle cx="680" cy="110" r="48" fill="url(#moonGlow)" opacity="0.9" filter="url(#glow)" />
    <circle cx="665" cy="100" r="40" fill="#050814" opacity="0.08" />
    <circle cx="120" cy="60" r="2" fill="#FFF" class="star-1" />
    <circle cx="280" cy="40" r="1.5" fill="#38BDF8" class="star-2" />
    <circle cx="480" cy="70" r="2" fill="#FFF" class="star-3" />
    <circle cx="580" cy="35" r="1.5" fill="#FFF" class="star-1" />
    <circle cx="750" cy="50" r="2" fill="#F43F5E" class="star-2" />
    <circle cx="60" cy="120" r="1.5" fill="#FFF" class="star-3" />
  </g>

  <!-- City Skyline -->
  <g>
    <rect x="40" y="240" width="90" height="260" fill="#070C18" />
    <rect x="150" y="200" width="110" height="300" fill="#080F1E" />
    <rect x="280" y="260" width="80" height="240" fill="#070C18" />
    <rect x="520" y="220" width="100" height="280" fill="#080F1E" />
    <rect x="640" y="180" width="120" height="320" fill="#060A14" />

    <path d="M 0 160 L 110 140 L 110 500 L 0 500 Z" fill="url(#buildingGrad1)" stroke="#1E293B" stroke-width="1.5" />
    <line x1="55" y1="148" x2="55" y2="100" stroke="#E23636" stroke-width="2" />
    <circle cx="55" cy="98" r="3" fill="#E23636" filter="url(#glow)" />

    <g fill="#FDE047" opacity="0.7">
      <rect x="20" y="180" width="14" height="22" rx="2" />
      <rect x="45" y="180" width="14" height="22" rx="2" opacity="0.2" />
      <rect x="70" y="180" width="14" height="22" rx="2" />
      <rect x="20" y="220" width="14" height="22" rx="2" />
      <rect x="45" y="220" width="14" height="22" rx="2" />
      <rect x="70" y="220" width="14" height="22" rx="2" opacity="0.3" />
      <rect x="20" y="260" width="14" height="22" rx="2" opacity="0.2" />
      <rect x="45" y="260" width="14" height="22" rx="2" />
      <rect x="70" y="260" width="14" height="22" rx="2" />
    </g>

    <path d="M 690 120 L 800 100 L 800 500 L 690 500 Z" fill="url(#buildingGrad2)" stroke="#1E293B" stroke-width="1.5" />
    <line x1="745" y1="110" x2="745" y2="60" stroke="#38BDF8" stroke-width="2" />
    <circle cx="745" cy="58" r="3" fill="#38BDF8" filter="url(#glow)" />

    <g fill="#38BDF8" opacity="0.65">
      <rect x="710" y="150" width="16" height="24" rx="2" />
      <rect x="740" y="150" width="16" height="24" rx="2" />
      <rect x="770" y="150" width="16" height="24" rx="2" opacity="0.2" />
      <rect x="710" y="195" width="16" height="24" rx="2" opacity="0.3" />
      <rect x="740" y="195" width="16" height="24" rx="2" />
      <rect x="770" y="195" width="16" height="24" rx="2" />
      <rect x="710" y="240" width="16" height="24" rx="2" />
      <rect x="740" y="240" width="16" height="24" rx="2" opacity="0.2" />
      <rect x="770" y="240" width="16" height="24" rx="2" />
    </g>
  </g>

  <!-- Swinging Full Body Spider-Man -->
  <g class="spider-rig">
    <path d="M 400 0 Q 395 120 400 240" stroke="#FFFFFF" stroke-width="3" fill="none" class="web-thread" filter="url(#glow)" />

    <g transform="translate(400, 270)">
      <!-- Right Arm Gripping Web -->
      <path d="M 10 -40 Q 8 -75 2 -110" stroke="url(#suitRed)" stroke-width="15" stroke-linecap="round" fill="none" />
      <path d="M 10 -40 Q 8 -75 2 -110" stroke="#000" stroke-width="2" stroke-linecap="round" fill="none" opacity="0.6" />
      <circle cx="2" cy="-110" r="9" fill="url(#suitRed)" stroke="#000" stroke-width="2" />

      <!-- Left Arm Shooting Web -->
      <path d="M -16 -35 Q -45 -30 -68 -10" stroke="url(#suitRed)" stroke-width="14" stroke-linecap="round" fill="none" />
      <path d="M -16 -35 Q -45 -30 -68 -10" stroke="#000" stroke-width="2" stroke-linecap="round" fill="none" opacity="0.6" />
      <path d="M -68 -10 Q -78 -6 -82 0 Q -74 8 -66 2 Z" fill="url(#suitRed)" stroke="#000" stroke-width="2" />

      <!-- Left Leg (Folded Knee) -->
      <path d="M -12 18 Q -40 28 -45 58 Q -50 88 -32 110" stroke="url(#suitBlue)" stroke-width="16" stroke-linecap="round" fill="none" />
      <path d="M -45 58 Q -50 88 -32 110" stroke="url(#suitRed)" stroke-width="15" stroke-linecap="round" fill="none" />
      <path d="M -32 110 L -20 122 L -36 128 Z" fill="url(#suitRed)" stroke="#000" stroke-width="2" />

      <!-- Right Leg (Extended Swing) -->
      <path d="M 14 18 Q 38 45 52 82 Q 62 115 75 140" stroke="url(#suitBlue)" stroke-width="16" stroke-linecap="round" fill="none" />
      <path d="M 52 82 Q 62 115 75 140" stroke="url(#suitRed)" stroke-width="15" stroke-linecap="round" fill="none" />
      <path d="M 75 140 L 92 148 L 78 156 Z" fill="url(#suitRed)" stroke="#000" stroke-width="2" />

      <!-- Torso -->
      <path d="M -20 -42 Q 0 -48 20 -42 Q 22 -10 16 22 Q 0 28 -16 22 Q -22 -10 -20 -42 Z" fill="url(#suitRed)" stroke="#000" stroke-width="2.5" />
      <path d="M -20 -38 Q -14 -10 -15 18 Q -21 12 -21 -25 Z" fill="url(#suitBlue)" />
      <path d="M 20 -38 Q 14 -10 15 18 Q 21 12 21 -25 Z" fill="url(#suitBlue)" />

      <!-- Spider Emblem -->
      <g transform="translate(0, -15) scale(0.85)">
        <ellipse cx="0" cy="0" rx="3.5" ry="6" fill="#000" />
        <path d="M -2 -3 Q -12 -12 -15 -18 M -2 -1 Q -14 -4 -18 2 M -2 2 Q -14 6 -16 14 M -2 4 Q -10 12 -10 20" stroke="#000" stroke-width="2" fill="none" stroke-linecap="round" />
        <path d="M 2 -3 Q 12 -12 15 -18 M 2 -1 Q 14 -4 18 2 M 2 2 Q 14 6 16 14 M 2 4 Q 10 12 10 20" stroke="#000" stroke-width="2" fill="none" stroke-linecap="round" />
      </g>

      <!-- Mask & Eyes -->
      <g transform="translate(0, -58)">
        <ellipse cx="0" cy="0" rx="22" ry="26" fill="url(#suitRed)" stroke="#000" stroke-width="2.5" />
        <g class="spider-eyes">
          <path d="M -4 -8 Q -18 -8 -20 6 Q -10 10 -4 0 Z" fill="#000" />
          <path d="M -5 -6 Q -16 -6 -17 4 Q -10 7 -5 0 Z" fill="#FFFFFF" />
          <path d="M 4 -8 Q 18 -8 20 6 Q 10 10 4 0 Z" fill="#000" />
          <path d="M 5 -6 Q 16 -6 17 4 Q 10 7 5 0 Z" fill="#FFFFFF" />
        </g>
      </g>
    </g>
  </g>
</svg>
