<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
  <title>Decorate the Caring Cactus!</title>
  
  <!-- PWA Manifest Meta -->
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="theme-color" content="#e09f48">

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts for playful header -->
  <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&family=Bungee&display=swap" rel="stylesheet">

  <style>
    * {
      touch-action: manipulation;
      user-select: none;
      -webkit-user-select: none;
      -webkit-touch-callout: none;
    }
    body {
      font-family: 'Fredoka', cursive, sans-serif;
      background-color: #fce4b8;
      overflow: hidden;
      width: 100vw;
      height: 100vh;
      margin: 0;
      padding: 0;
    }

    .font-bungee {
      font-family: 'Bungee', cursive;
    }

    @keyframes vultureFly {
      0% { transform: translate(0, 0) scale(1); }
      50% { transform: translate(60px, -20px) scale(0.9); }
      100% { transform: translate(0, 0) scale(1); }
    }
    .vulture-1 { animation: vultureFly 8s ease-in-out infinite; }
    .vulture-2 { animation: vultureFly 10s ease-in-out infinite 1s; }
    .vulture-3 { animation: vultureFly 7s ease-in-out infinite 2s; }
    .vulture-4 { animation: vultureFly 9s ease-in-out infinite 3s; }

    @keyframes flyBuzz {
      0% { transform: translate(0, 0); }
      25% { transform: translate(3px, -4px); }
      50% { transform: translate(-2px, 3px); }
      75% { transform: translate(4px, 2px); }
      100% { transform: translate(0, 0); }
    }
    .fly-buzz { animation: flyBuzz 0.3s linear infinite; }
    .fly-buzz-1 { animation: flyBuzz 0.22s linear infinite; }
    .fly-buzz-2 { animation: flyBuzz 0.32s linear infinite reverse; }
    .fly-buzz-3 { animation: flyBuzz 0.28s linear infinite 0.1s; }

    @keyframes tumbleweedRoll {
      0% { transform: translateX(-100px) rotate(0deg); }
      50% { transform: translateX(calc(100vw + 100px)) rotate(720deg); }
      100% { transform: translateX(calc(100vw + 100px)) rotate(720deg); }
    }
    .tumbleweed-anim {
      animation: tumbleweedRoll 14s linear infinite;
    }

    @keyframes carcassVultureCircle {
      0% { transform: translate(0, 0) scale(1) rotate(0deg); }
      25% { transform: translate(25px, -15px) scale(1.05) rotate(10deg); }
      50% { transform: translate(40px, 10px) scale(0.9) rotate(0deg); }
      75% { transform: translate(15px, 20px) scale(0.8) rotate(-10deg); }
      100% { transform: translate(0, 0) scale(1) rotate(0deg); }
    }
    .vulture-carcass-1 { animation: carcassVultureCircle 6s ease-in-out infinite; }
    .vulture-carcass-2 { animation: carcassVultureCircle 8s ease-in-out infinite 1.5s; }
    .vulture-carcass-3 { animation: carcassVultureCircle 7s ease-in-out infinite 3s; }

    @keyframes camelDrink {
      0%, 100% { transform: rotate(0deg) translateY(0); }
      40%, 70% { transform: rotate(18deg) translateY(8px); }
    }
    .camel-drinking {
      transform-origin: bottom left;
      animation: camelDrink 5s ease-in-out infinite;
    }

    @keyframes elephantTrunkDip {
      0%, 100% { transform: rotate(0deg); }
      35%, 65% { transform: rotate(-14deg) translateY(6px); }
    }
    .elephant-drinking {
      transform-origin: bottom right;
      animation: elephantTrunkDip 6s ease-in-out infinite 1s;
    }

    @keyframes monkeyScoop {
      0%, 100% { transform: translateY(0) scale(1); }
      50% { transform: translateY(4px) scale(1.05); }
    }
    .monkey-drinking {
      animation: monkeyScoop 3s ease-in-out infinite;
    }

    @keyframes commandPulse {
      0%, 100% { transform: scale(1); box-shadow: 0 0 0px rgba(239, 68, 68, 0); }
      50% { transform: scale(1.05); box-shadow: 0 0 25px rgba(239, 68, 68, 0.9); }
    }
    .flash-command {
      animation: commandPulse 0.8s infinite;
      border: 4px solid #ef4444 !important;
    }

    @keyframes moonwalkAnim {
      0% { transform: translateX(0) scaleX(1); }
      25% { transform: translateX(120px) scaleX(1); }
      50% { transform: translateX(-120px) scaleX(1); }
      75% { transform: translateX(60px) scaleX(1); }
      100% { transform: translateX(0) scaleX(1); }
    }
    .cactus-moonwalk {
      animation: moonwalkAnim 6s ease-in-out infinite;
    }

    @keyframes precisionDiveAnim {
      0% { transform: translate(0, 0) rotate(0deg) scale(1); }
      25% { transform: translate(-140px, -140px) rotate(-35deg) scale(0.95); }
      60% { transform: translate(-280px, 60px) rotate(-80deg) scale(0.65); opacity: 0.9; }
      75% { transform: translate(-280px, 40px) rotate(-20deg) scale(0.85); opacity: 1; }
      100% { transform: translate(0, 0) rotate(0deg) scale(1); }
    }
    .cactus-dive {
      animation: precisionDiveAnim 3.8s cubic-bezier(0.25, 1, 0.5, 1) forwards;
    }

    .custom-scrollbar::-webkit-scrollbar {
      width: 8px;
    }
    .custom-scrollbar::-webkit-scrollbar-track {
      background: rgba(0,0,0,0.05);
      border-radius: 10px;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb {
      background: rgba(180, 83, 9, 0.5);
      border-radius: 10px;
    }

    .filter-instagram {
      filter: sepia(0.35) contrast(1.15) brightness(1.05) saturate(1.3);
    }
    .filter-funky {
      filter: hue-rotate(90deg) contrast(1.4) saturate(1.8);
    }

    @keyframes sunRayRotate {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    .sun-rays {
      animation: sunRayRotate 45s linear infinite;
      transform-origin: center center;
    }
    @keyframes sunPulse {
      0%, 100% { transform: scale(1); opacity: 0.95; }
      50% { transform: scale(1.08); opacity: 1; }
    }
    .sun-glow {
      animation: sunPulse 4s ease-in-out infinite;
      transform-origin: center center;
    }
  </style>
</head>
<body class="flex flex-col h-screen w-screen overflow-hidden select-none">

  <div id="stage" class="relative flex-1 w-full h-full overflow-hidden bg-gradient-to-b from-sky-400 via-amber-200 to-orange-300">
    
    <!-- Sun -->
    <div class="absolute top-2 left-1/2 -translate-x-1/2 w-64 h-64 pointer-events-none z-0 flex items-center justify-center">
      <div class="absolute w-56 h-56 bg-amber-300/50 rounded-full blur-3xl sun-glow"></div>
      <div class="absolute w-40 h-40 bg-yellow-200/70 rounded-full blur-xl"></div>
      <svg class="w-48 h-48 drop-shadow-[0_0_30px_rgba(251,191,36,0.95)]" viewBox="0 0 200 200" fill="none">
        <defs>
          <radialGradient id="sunGrad" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stop-color="#ffffff" />
            <stop offset="25%" stop-color="#fff7ed" />
            <stop offset="55%" stop-color="#fef08a" />
            <stop offset="80%" stop-color="#f59e0b" />
            <stop offset="100%" stop-color="#ea580c" />
          </radialGradient>
          <radialGradient id="coronaGrad" cx="50%" cy="50%" r="50%">
            <stop offset="60%" stop-color="#fef08a" stop-opacity="0.85" />
            <stop offset="100%" stop-color="#f97316" stop-opacity="0" />
          </radialGradient>
        </defs>
        <g class="sun-rays" opacity="0.8">
          <circle cx="100" cy="100" r="85" fill="url(#coronaGrad)" />
          <path d="M100,10 L100,190 M10,100 L190,100 M36,36 L164,164 M36,164 L164,36" stroke="#fde047" stroke-width="3" stroke-linecap="round" opacity="0.6"/>
        </g>
        <circle cx="100" cy="100" r="42" fill="url(#sunGrad)" />
      </svg>
    </div>

    <!-- Sky Vultures -->
    <div class="absolute top-3 left-48 sm:left-64 flex space-x-8 pointer-events-none z-10">
      <svg class="w-10 h-10 vulture-1 text-slate-800 opacity-80" viewBox="0 0 100 100" fill="currentColor">
        <path d="M10,50 Q30,20 50,50 Q70,20 90,50 Q70,40 50,60 Q30,40 10,50 Z"/>
      </svg>
      <svg class="w-8 h-8 vulture-2 text-slate-800 opacity-70" viewBox="0 0 100 100" fill="currentColor">
        <path d="M10,50 Q30,20 50,50 Q70,20 90,50 Q70,40 50,60 Q30,40 10,50 Z"/>
      </svg>
      <svg class="w-12 h-12 vulture-3 text-slate-800 opacity-75" viewBox="0 0 100 100" fill="currentColor">
        <path d="M10,50 Q30,20 50,50 Q70,20 90,50 Q70,40 50,60 Q30,40 10,50 Z"/>
      </svg>
    </div>

    <!-- Circling Vultures over Graveyard -->
    <div class="absolute top-4 right-52 sm:right-72 md:right-96 w-28 h-28 pointer-events-none z-10">
      <svg class="w-8 h-8 vulture-carcass-1 text-slate-900 opacity-80 absolute top-0 left-0" viewBox="0 0 100 100" fill="currentColor">
        <path d="M10,50 Q30,20 50,50 Q70,20 90,50 Q70,40 50,60 Q30,40 10,50 Z"/>
      </svg>
      <svg class="w-6 h-6 vulture-carcass-2 text-slate-800 opacity-70 absolute top-4 left-8" viewBox="0 0 100 100" fill="currentColor">
        <path d="M10,50 Q30,20 50,50 Q70,20 90,50 Q70,40 50,60 Q30,40 10,50 Z"/>
      </svg>
      <svg class="w-7 h-7 vulture-carcass-3 text-slate-900 opacity-75 absolute top-8 left-2" viewBox="0 0 100 100" fill="currentColor">
        <path d="M10,50 Q30,20 50,50 Q70,20 90,50 Q70,40 50,60 Q30,40 10,50 Z"/>
      </svg>
    </div>

    <!-- Timer Header Bar -->
    <div class="absolute top-3 left-1/2 -translate-x-1/2 z-20 flex items-center bg-amber-900/80 text-amber-100 backdrop-blur-md px-5 py-2 rounded-full border-2 border-amber-400 shadow-lg">
      <svg class="w-7 h-7 mr-2 text-amber-300 animate-spin" style="animation-duration: 8s;" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
      </svg>
      <span class="font-bold text-sm sm:text-base mr-2">Time Left:</span>
      <span id="timer" class="font-bungee text-lg sm:text-xl text-amber-300 tracking-wider">90</span>
      <span class="font-bold text-xs sm:text-sm ml-1">s</span>
    </div>

    <!-- Game Title -->
    <div class="absolute top-3 left-4 z-20 flex items-center space-x-2">
      <div class="bg-white/80 backdrop-blur-sm px-4 py-1.5 rounded-2xl shadow-md border border-amber-300 hidden xl:block">
        <h1 class="font-bungee text-xl text-emerald-800 tracking-wide">Decorate the Caring Cactus!</h1>
      </div>
    </div>

    <!-- Mountains and Dunes -->
    <svg class="absolute bottom-28 w-full h-48 pointer-events-none z-0 opacity-90" preserveAspectRatio="none" viewBox="0 0 1200 200">
      <path d="M0,200 L0,110 L80,130 L160,80 L280,140 L400,60 L520,110 L680,40 L820,120 L940,50 L1080,110 L1200,70 L1200,200 Z" fill="#2d4263" />
      <path d="M0,200 L0,140 L120,110 L240,150 L380,90 L500,130 L640,70 L780,130 L920,80 L1040,130 L1200,100 L1200,200 Z" fill="#1e2d42" />
    </svg>

    <!-- Rolling Tumbleweed -->
    <div class="absolute bottom-12 left-0 pointer-events-none z-10 tumbleweed-anim w-16 h-16 sm:w-20 sm:h-20">
      <svg class="w-full h-full drop-shadow-lg" viewBox="0 0 100 100" fill="none">
        <!-- Intertwined realistic tumbleweed branches -->
        <circle cx="50" cy="50" r="42" stroke="#78350f" stroke-width="3" stroke-dasharray="14,8,6,4"/>
        <circle cx="50" cy="50" r="32" stroke="#92400e" stroke-width="2.5" stroke-dasharray="10,6,8,5"/>
        <circle cx="50" cy="50" r="22" stroke="#b45309" stroke-width="2" stroke-dasharray="8,4"/>
        <path d="M15,35 Q50,75 85,35 M25,80 Q50,15 75,80 M10,50 Q90,50 50,90 M20,20 Q80,80 50,50" stroke="#78350f" stroke-width="2.5" stroke-linecap="round"/>
        <path d="M12,60 Q50,25 88,60 M30,15 Q75,85 20,85" stroke="#a16207" stroke-width="2" stroke-linecap="round"/>
        <!-- Cute Eyes and Smile on Tumbleweed -->
        <circle cx="40" cy="42" r="5" fill="#ffffff" stroke="#451a03" stroke-width="1.5"/>
        <circle cx="60" cy="42" r="5" fill="#ffffff" stroke="#451a03" stroke-width="1.5"/>
        <circle cx="41" cy="42" r="2.5" fill="#000000"/>
        <circle cx="61" cy="42" r="2.5" fill="#000000"/>
        <circle cx="42" cy="40" r="1" fill="#ffffff"/>
        <circle cx="62" cy="40" r="1" fill="#ffffff"/>
        <path d="M43,54 Q50,62 57,54" stroke="#451a03" stroke-width="2.5" stroke-linecap="round" fill="none"/>
      </svg>
    </div>

    <svg class="absolute bottom-0 w-full h-2/3 pointer-events-none z-0" preserveAspectRatio="none" viewBox="0 0 1200 500">
      <path d="M0,280 Q300,180 600,260 T1200,220 L1200,500 L0,500 Z" fill="#fbbf24" />
      <path d="M0,330 Q400,240 800,310 T1200,290 L1200,500 L0,500 Z" fill="#f59e0b" />
      <path d="M0,380 Q350,300 700,360 T1200,340 L1200,500 L0,500 Z" fill="#d97706" />
    </svg>

    <!-- Desert Skulls, Ribcage Carcass & Buzzing Flies -->
    <div class="absolute bottom-16 right-4 sm:right-12 md:right-20 lg:right-28 z-10 pointer-events-none flex flex-col items-center">
      <div class="relative w-36 sm:w-44 h-24">
        <svg class="w-full h-full drop-shadow-md" viewBox="0 0 160 100" fill="none">
          <!-- Steer Skull -->
          <g transform="translate(10, 45) rotate(-10) scale(0.85)">
            <path d="M10,15 Q-15,-10 -30,-5 M70,15 Q95,-10 110,-5" stroke="#e5e5e5" stroke-width="5" stroke-linecap="round" fill="none"/>
            <path d="M15,15 L65,15 L50,60 L30,60 Z" fill="#f5f5f4" stroke="#d6d3d1" stroke-width="2"/>
            <ellipse cx="28" cy="28" rx="6" ry="8" fill="#262626"/>
            <ellipse cx="52" cy="28" rx="6" ry="8" fill="#262626"/>
            <path d="M36,48 L44,48 L40,56 Z" fill="#262626"/>
          </g>

          <!-- Ribcage Skeleton -->
          <g transform="translate(70, 35)">
            <path d="M0,35 Q30,25 70,35" stroke="#f5f5f4" stroke-width="4" stroke-linecap="round"/>
            <path d="M10,33 Q12,10 25,12 M10,33 Q8,50 22,48" stroke="#f5f5f4" stroke-width="3" fill="none" stroke-linecap="round"/>
            <path d="M25,31 Q27,8 40,10 M25,31 Q23,52 37,50" stroke="#f5f5f4" stroke-width="3" fill="none" stroke-linecap="round"/>
            <path d="M40,31 Q42,10 53,12 M40,31 Q38,50 50,48" stroke="#f5f5f4" stroke-width="3" fill="none" stroke-linecap="round"/>
            <path d="M55,33 Q57,15 65,17 M55,33 Q53,46 62,45" stroke="#f5f5f4" stroke-width="3" fill="none" stroke-linecap="round"/>
          </g>

          <!-- Scattered Bones -->
          <rect x="25" y="82" width="16" height="4" rx="2" fill="#e7e5e4" transform="rotate(15 25 82)"/>
          <rect x="110" y="78" width="20" height="5" rx="2" fill="#e7e5e4" transform="rotate(-25 110 78)"/>
          <circle cx="132" cy="72" r="3" fill="#e7e5e4"/>
        </svg>

        <!-- Buzzing Flies -->
        <div class="absolute top-6 left-6 w-2 h-2 bg-black rounded-full fly-buzz-1 opacity-80"></div>
        <div class="absolute top-10 left-16 w-1.5 h-1.5 bg-black rounded-full fly-buzz-2 opacity-90"></div>
        <div class="absolute top-8 right-10 w-2 h-2 bg-black rounded-full fly-buzz-3 opacity-85"></div>
      </div>
    </div>

    <div id="oasis-container" class="absolute bottom-16 left-[180px] sm:left-[240px] md:left-[290px] lg:left-[330px] z-10 flex flex-col items-center scale-90 sm:scale-100 transition-all duration-300 pointer-events-none">
      <div class="relative w-80 h-44 -mb-12 z-0">
        <svg class="w-full h-full drop-shadow-lg" viewBox="0 0 320 180" fill="none">
          <ellipse cx="160" cy="145" rx="140" ry="25" fill="#15803d" />
          <ellipse cx="100" cy="140" rx="50" ry="20" fill="#166534" />
          <ellipse cx="220" cy="140" rx="55" ry="22" fill="#166534" />
          <ellipse cx="160" cy="135" rx="70" ry="22" fill="#22c55e" />

          <path d="M60,165 Q45,100 50,30" stroke="#78350f" stroke-width="10" stroke-linecap="round"/>
          <g stroke="#15803d" stroke-width="7" stroke-linecap="round">
            <path d="M50,30 Q20,10 -5,25 M50,30 Q35,-10 50,-5 M50,30 Q75,0 95,20 M50,30 Q70,50 30,55"/>
          </g>

          <path d="M240,165 Q255,100 245,25" stroke="#78350f" stroke-width="11" stroke-linecap="round"/>
          <g stroke="#15803d" stroke-width="8" stroke-linecap="round">
            <path d="M245,25 Q210,5 190,20 M245,25 Q235,-15 250,-10 M245,25 Q275,-5 295,15"/>
          </g>
        </svg>
      </div>

      <!-- Water Lagoon -->
      <div id="oasis-water" class="relative w-80 h-28 bg-gradient-to-r from-sky-500 via-cyan-400 to-blue-600 rounded-[100%] border-4 border-amber-300 shadow-2xl flex items-center justify-center z-10">
        <div class="absolute inset-2 border-2 border-cyan-200/60 rounded-[100%] pointer-events-none"></div>
        <span class="text-[10px] text-blue-100 font-black tracking-widest opacity-90 animate-pulse">🌴 OASIS LAGOON 🌴</span>
        
        <div id="splash-effect" class="hidden absolute -top-16 left-1/2 -translate-x-1/2 pointer-events-none z-30">
          <svg class="w-36 h-36 text-cyan-200 animate-ping" fill="currentColor" viewBox="0 0 100 100">
            <path d="M50,5 Q65,35 95,50 Q65,65 50,95 Q35,65 5,50 Q35,35 50,5 Z" />
          </svg>
        </div>
      </div>

      <!-- Drinking Animals -->
      <div class="absolute -bottom-2 left-0 right-0 z-20 flex justify-between items-end px-2">
        <div class="flex items-end -space-x-3 elephant-drinking">
          <svg class="w-16 h-16 text-slate-600 drop-shadow-md" viewBox="0 0 100 100" fill="currentColor">
            <circle cx="50" cy="45" r="28"/>
            <rect x="25" y="55" width="9" height="28" rx="3"/>
            <rect x="65" y="55" width="9" height="28" rx="3"/>
            <path d="M28,40 Q10,42 8,68 Q15,85 22,65" stroke="currentColor" stroke-width="7" fill="none" stroke-linecap="round"/>
            <circle cx="36" cy="38" r="3" fill="#fff"/>
          </svg>
        </div>

        <div class="monkey-drinking relative -mb-1">
          <svg class="w-10 h-10 text-amber-950 drop-shadow" viewBox="0 0 100 100" fill="currentColor">
            <circle cx="50" cy="45" r="18"/>
            <circle cx="36" cy="40" r="7" fill="#d97706"/>
            <circle cx="64" cy="40" r="7" fill="#d97706"/>
          </svg>
        </div>

        <div class="flex items-end space-x-1 camel-drinking">
          <svg class="w-14 h-14 text-amber-800 drop-shadow-md" viewBox="0 0 100 100" fill="currentColor">
            <path d="M20,55 Q20,25 40,25 Q50,40 60,25 Q70,20 80,40 L80,70 L20,70 Z"/>
            <rect x="25" y="65" width="6" height="22"/>
            <rect x="70" y="65" width="6" height="22"/>
          </svg>
        </div>
      </div>
    </div>

    <div id="cactus-container" class="absolute bottom-12 left-1/2 -translate-x-1/2 z-20 flex flex-col items-center transition-all duration-300">
      <div id="cactus-body" class="relative w-56 sm:w-72 h-[360px] sm:h-[440px] flex items-center justify-center">
        <svg class="w-full h-full drop-shadow-2xl" viewBox="0 0 200 320" fill="none">
          <!-- Main Stem -->
          <rect x="75" y="30" width="50" height="260" rx="25" fill="#15803d" stroke="#166534" stroke-width="4"/>
          <!-- Vertical Ridges -->
          <path d="M88,35 L88,285 M100,30 L100,290 M112,35 L112,285" stroke="#22c55e" stroke-width="3" stroke-linecap="round" opacity="0.6"/>
          
          <!-- Left Arm Branch -->
          <path d="M75,140 L40,140 Q25,140 25,120 L25,70" stroke="#15803d" stroke-width="26" stroke-linecap="round" stroke-linejoin="round"/>
          
          <!-- Right Arm Branch -->
          <path d="M125,170 L160,170 Q175,170 175,150 L175,90" stroke="#15803d" stroke-width="26" stroke-linecap="round" stroke-linejoin="round"/>

          <!-- Thorns -->
          <g stroke="#fef08a" stroke-width="3" stroke-linecap="round">
            <!-- Left Arm Thorns -->
            <line x1="25" y1="65" x2="15" y2="60" /><line x1="25" y1="85" x2="10" y2="85" />
            <line x1="25" y1="105" x2="12" y2="110" />

            <!-- Top Stem Thorns -->
            <line x1="80" y1="35" x2="70" y2="25" /><line x1="100" y1="30" x2="100" y2="15" />
            <line x1="120" y1="35" x2="130" y2="25" />

            <!-- Stem Thorns -->
            <line x1="75" y1="80" x2="62" y2="78" /><line x1="125" y1="80" x2="138" y2="78" />
            <line x1="75" y1="125" x2="60" y2="128" /><line x1="125" y1="125" x2="140" y2="128" />
            <line x1="75" y1="175" x2="62" y2="180" /><line x1="125" y1="175" x2="138" y2="180" />
            <line x1="75" y1="225" x2="60" y2="232" /><line x1="125" y1="225" x2="140" y2="232" />
            <line x1="75" y1="270" x2="62" y2="275" /><line x1="125" y1="270" x2="138" y2="275" />

            <!-- Right Arm Thorns -->
            <line x1="175" y1="85" x2="185" y2="80" /><line x1="175" y1="105" x2="190" y2="105" />
            <line x1="175" y1="125" x2="188" y2="130" />
          </g>
        </svg>

        <!-- Attached Items Container Layer -->
        <div id="attached-layer" class="absolute inset-0 pointer-events-auto overflow-visible z-30"></div>
      </div>
    </div>

    <!-- LEFT SIDE PANELS: CAPTION 1 & CAPTION 2 -->
    <div class="absolute top-16 bottom-4 left-2 z-30 flex flex-col space-y-2 w-40 sm:w-48 md:w-56 lg:w-60 max-h-[calc(100vh-80px)] pointer-events-auto transition-all">
      
      <!-- CAPTION 1: Limbs and facial features -->
      <div class="bg-amber-50/95 backdrop-blur-md border-2 border-amber-600 rounded-xl shadow-xl flex flex-col overflow-hidden flex-1">
        <div class="bg-gradient-to-r from-amber-600 to-amber-700 px-2.5 py-1.5 text-white shadow">
          <h2 class="text-xs sm:text-sm font-bold font-bungee tracking-wide truncate">1. Limbs & Features</h2>
        </div>
        <div class="p-1.5 sm:p-2 overflow-y-auto space-y-2 custom-scrollbar flex-1" id="caption1-list">
          <!-- Populated by JS -->
        </div>
      </div>

      <!-- CAPTION 2: Accessories -->
      <div class="bg-orange-50/95 backdrop-blur-md border-2 border-orange-600 rounded-xl shadow-xl flex flex-col overflow-hidden flex-1">
        <div class="bg-gradient-to-r from-orange-600 to-orange-700 px-2.5 py-1.5 text-white shadow">
          <h2 class="text-xs sm:text-sm font-bold font-bungee tracking-wide truncate">2. Accessories</h2>
        </div>
        <div class="p-1.5 sm:p-2 overflow-y-auto space-y-2 custom-scrollbar flex-1" id="caption2-list">
          <!-- Populated by JS -->
        </div>
      </div>
    </div>

    <!-- RIGHT SIDE PANEL: CAPTION 3 (COMMANDS) -->
    <div id="caption3-panel" class="absolute top-16 right-2 z-30 w-48 sm:w-64 md:w-72 lg:w-80 bg-rose-50/95 backdrop-blur-md border-2 border-rose-600 rounded-2xl shadow-2xl p-3 flex flex-col space-y-2 transition-all duration-300">
      <div class="border-b border-rose-300 pb-1 text-center">
        <h2 class="text-base sm:text-lg md:text-xl font-black font-bungee text-rose-700 tracking-wider">3. COMMANDS</h2>
        <p class="text-[11px] sm:text-xs text-rose-600 font-semibold leading-tight">Attach items then tap!</p>
      </div>

      <div class="flex flex-col space-y-2">
        <!-- Command 1: Precision Water Dive -->
        <button id="cmd-dive" class="w-full bg-gradient-to-r from-blue-500 to-cyan-600 hover:from-blue-600 hover:to-cyan-700 active:scale-95 text-white font-bold py-2.5 px-3 rounded-xl shadow-md flex items-center space-x-2 text-xs sm:text-sm transition">
          <span class="text-xl">🏊‍♂️</span>
          <span class="text-left font-bold leading-tight">Oasis Water Dive</span>
        </button>

        <!-- Command 2: MJ Moonwalk -->
        <button id="cmd-moonwalk" class="w-full bg-gradient-to-r from-purple-600 to-indigo-600 hover:from-purple-700 hover:to-indigo-700 active:scale-95 text-white font-bold py-2.5 px-3 rounded-xl shadow-md flex items-center space-x-2 text-xs sm:text-sm transition">
          <span class="text-xl">🕺</span>
          <span class="text-left font-bold leading-tight">MJ Moonwalk</span>
        </button>

        <!-- Command 3: Rain & Thunder -->
        <button id="cmd-thunder" class="w-full bg-gradient-to-r from-slate-700 to-sky-900 hover:from-slate-800 hover:to-sky-950 active:scale-95 text-white font-bold py-2.5 px-3 rounded-xl shadow-md flex items-center space-x-2 text-xs sm:text-sm transition">
          <span class="text-xl">⚡</span>
          <span class="text-left font-bold leading-tight">Rain & Thunder</span>
        </button>
      </div>

      <!-- Item Counter -->
      <div class="mt-1 pt-2 border-t border-rose-200 text-center">
        <div class="text-xs font-bold text-rose-800">Items Attached:</div>
        <div id="item-counter" class="text-xl font-bungee text-rose-600">0 / 8</div>
      </div>

      <!-- Take Photo Early Button -->
      <button id="btn-take-photo-now" class="mt-1 w-full bg-emerald-600 hover:bg-emerald-700 active:scale-95 text-white font-black py-2 px-2 rounded-xl text-xs sm:text-sm shadow tracking-wide uppercase">
        📸 Take Photo
      </button>
    </div>

    <!-- Weather Canvas -->
    <canvas id="weather-canvas" class="absolute inset-0 pointer-events-none z-20 hidden"></canvas>
  </div>

  <div id="photo-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-md flex items-center justify-center p-4 hidden">
    <div class="bg-white rounded-3xl max-w-lg w-full p-5 flex flex-col items-center shadow-2xl border-4 border-amber-400 max-h-[95vh] overflow-y-auto">
      
      <div class="text-center mb-2">
        <h2 class="text-2xl font-bungee text-amber-800">Cactus Snapshot!</h2>
        <p class="text-xs text-stone-600 font-semibold">Oasis and your cactus are fully preserved!</p>
      </div>

      <div id="photo-frame" class="relative w-full h-80 bg-gradient-to-b from-sky-200 via-amber-100 to-amber-200 rounded-2xl border-4 border-amber-800 overflow-hidden shadow-inner flex items-center justify-center transition-all duration-300">
        <div id="photo-content" class="relative w-full h-full flex items-center justify-center transform scale-90"></div>
      </div>

      <div class="flex space-x-2 my-3 w-full justify-center">
        <button id="btn-filter-normal" class="flex-1 py-2 px-3 bg-amber-200 border-2 border-amber-600 rounded-xl font-bold text-xs sm:text-sm text-amber-900 shadow active:scale-95">
          ✨ Original
        </button>
        <button id="btn-filter-insta" class="flex-1 py-2 px-3 bg-purple-200 border-2 border-purple-600 rounded-xl font-bold text-xs sm:text-sm text-purple-900 shadow active:scale-95">
          📸 Instagram selfie
        </button>
        <button id="btn-filter-funky" class="flex-1 py-2 px-3 bg-pink-200 border-2 border-pink-600 rounded-xl font-bold text-xs sm:text-sm text-pink-900 shadow active:scale-95">
          🎨 Funky Pop
        </button>
      </div>

      <div class="flex space-x-2 w-full">
        <button id="btn-restart" class="w-full bg-amber-500 hover:bg-amber-600 text-white font-bold py-2.5 px-4 rounded-xl text-sm shadow active:scale-95">
          🔄 Play Again
        </button>
      </div>
    </div>
  </div>

  <script>
    const AudioContext = window.AudioContext || window.webkitAudioContext;
    let audioCtx = null;

    function getAudioCtx() {
      if (!audioCtx) {
        audioCtx = new AudioContext();
      }
      if (audioCtx.state === 'suspended') {
        audioCtx.resume();
      }
      return audioCtx;
    }

    const sound = {
      playPop() {
        try {
          const ctx = getAudioCtx();
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'sine';
          osc.frequency.setValueAtTime(400, ctx.currentTime);
          osc.frequency.exponentialRampToValueAtTime(800, ctx.currentTime + 0.08);
          gain.gain.setValueAtTime(0.3, ctx.currentTime);
          gain.gain.exponentialRampToValueAtTime(0.01, ctx.currentTime + 0.08);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start();
          osc.stop(ctx.currentTime + 0.08);
        } catch(e) {}
      },
      playRemove() {
        try {
          const ctx = getAudioCtx();
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'sine';
          osc.frequency.setValueAtTime(600, ctx.currentTime);
          osc.frequency.exponentialRampToValueAtTime(200, ctx.currentTime + 0.08);
          gain.gain.setValueAtTime(0.3, ctx.currentTime);
          gain.gain.exponentialRampToValueAtTime(0.01, ctx.currentTime + 0.08);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start();
          osc.stop(ctx.currentTime + 0.08);
        } catch(e) {}
      },
      playSplash() {
        try {
          const ctx = getAudioCtx();
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'triangle';
          osc.frequency.setValueAtTime(150, ctx.currentTime);
          osc.frequency.exponentialRampToValueAtTime(40, ctx.currentTime + 0.3);
          gain.gain.setValueAtTime(0.4, ctx.currentTime);
          gain.gain.exponentialRampToValueAtTime(0.01, ctx.currentTime + 0.3);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start();
          osc.stop(ctx.currentTime + 0.3);
        } catch(e) {}
      },
      playBillieJean() {
        try {
          const ctx = getAudioCtx();
          const notes = [261.63, 293.66, 329.63, 349.23, 392.00];
          notes.forEach((freq, idx) => {
            const osc = ctx.createOscillator();
            const gain = ctx.createGain();
            osc.frequency.setValueAtTime(freq, ctx.currentTime + idx * 0.15);
            gain.gain.setValueAtTime(0.2, ctx.currentTime + idx * 0.15);
            gain.gain.exponentialRampToValueAtTime(0.01, ctx.currentTime + idx * 0.15 + 0.12);
            osc.connect(gain);
            gain.connect(ctx.destination);
            osc.start(ctx.currentTime + idx * 0.15);
            osc.stop(ctx.currentTime + idx * 0.15 + 0.12);
          });
        } catch(e) {}
      },
      playThunder() {
        try {
          const ctx = getAudioCtx();
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'sawtooth';
          osc.frequency.setValueAtTime(80, ctx.currentTime);
          osc.frequency.exponentialRampToValueAtTime(20, ctx.currentTime + 0.8);
          gain.gain.setValueAtTime(0.5, ctx.currentTime);
          gain.gain.exponentialRampToValueAtTime(0.01, ctx.currentTime + 0.8);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start();
          osc.stop(ctx.currentTime + 0.8);
        } catch(e) {}
      }
    };

    const itemsData = [
      // --- CAPTION 1: Limbs and facial features ---
      {
        id: 'monster-legs',
        caption: 1,
        name: 'Green Legs',
        widthPercent: 44,
        defaultOffset: { percentX: 28, percentY: 80 },
        svg: `<svg viewBox="0 0 160 120" class="w-full h-auto drop-shadow">
                <path d="M30,10 L70,10 L65,55 L25,55 Z" fill="#1d4ed8"/>
                <path d="M90,10 L130,10 L135,55 L95,55 Z" fill="#1d4ed8"/>
                <path d="M30,55 Q15,80 5,100 L65,100 Q65,85 55,55 Z" fill="#15803d" stroke="#166534" stroke-width="3"/>
                <path d="M100,55 Q90,85 85,100 L150,100 Q140,80 125,55 Z" fill="#15803d" stroke="#166534" stroke-width="3"/>
                <path d="M5,100 L0,108 L10,104 M20,100 L18,110 L26,104" stroke="#fef08a" stroke-width="3" fill="#fef08a"/>
                <path d="M85,100 L80,108 L90,104 M105,100 L105,110 L112,104" stroke="#fef08a" stroke-width="3" fill="#fef08a"/>
              </svg>`
      },
      {
        id: 'goofy-eyes',
        caption: 1,
        name: 'Goofy Eyes',
        widthPercent: 26,
        defaultOffset: { percentX: 37, percentY: 16 },
        svg: `<svg viewBox="0 0 100 60" class="w-full h-auto drop-shadow">
                <circle cx="30" cy="30" r="22" fill="#ffffff" stroke="#000000" stroke-width="3"/>
                <circle cx="70" cy="30" r="22" fill="#ffffff" stroke="#000000" stroke-width="3"/>
                <circle cx="36" cy="26" r="9" fill="#000000"/>
                <circle cx="62" cy="34" r="9" fill="#000000"/>
                <circle cx="38" cy="24" r="3" fill="#ffffff"/>
                <circle cx="64" cy="32" r="3" fill="#ffffff"/>
              </svg>`
      },
      {
        id: 'alien-eyes',
        caption: 1,
        name: 'Alien Eyes',
        widthPercent: 28,
        defaultOffset: { percentX: 36, percentY: 16 },
        svg: `<svg viewBox="0 0 110 50" class="w-full h-auto drop-shadow">
                <ellipse cx="30" cy="25" rx="22" ry="14" fill="#a855f7" stroke="#000" stroke-width="3" transform="rotate(-15 30 25)"/>
                <ellipse cx="80" cy="25" rx="22" ry="14" fill="#a855f7" stroke="#000" stroke-width="3" transform="rotate(15 80 25)"/>
                <ellipse cx="30" cy="25" rx="10" ry="14" fill="#000"/>
                <ellipse cx="80" cy="25" rx="10" ry="14" fill="#000"/>
                <circle cx="28" cy="20" r="3" fill="#fff"/>
                <circle cx="78" cy="20" r="3" fill="#fff"/>
              </svg>`
      },
      {
        id: 'funny-smile',
        caption: 1,
        name: 'Funny Smile',
        widthPercent: 24,
        defaultOffset: { percentX: 38, percentY: 34 },
        svg: `<svg viewBox="0 0 120 60" class="w-full h-auto drop-shadow">
                <path d="M10,15 Q60,65 110,15 Q60,35 10,15 Z" fill="#dc2626" stroke="#991b1b" stroke-width="3"/>
                <path d="M20,20 Q60,45 100,20 Q60,25 20,20 Z" fill="#ffffff"/>
                <line x1="40" y1="21" x2="40" y2="29" stroke="#cbd5e1" stroke-width="2"/>
                <line x1="60" y1="21" x2="60" y2="31" stroke="#cbd5e1" stroke-width="2"/>
                <line x1="80" y1="21" x2="80" y2="29" stroke="#cbd5e1" stroke-width="2"/>
              </svg>`
      },
      {
        id: 'puffy-lips',
        caption: 1,
        name: 'Puffy Lips',
        widthPercent: 22,
        defaultOffset: { percentX: 39, percentY: 34 },
        svg: `<svg viewBox="0 0 100 50" class="w-full h-auto drop-shadow">
                <path d="M10,25 Q30,10 50,20 Q70,10 90,25 Q70,45 50,42 Q30,45 10,25 Z" fill="#ef4444" stroke="#b91c1c" stroke-width="3"/>
                <path d="M15,25 Q50,30 85,25" stroke="#991b1b" stroke-width="3" fill="none"/>
              </svg>`
      },
      {
        id: 'pinocchio-nose',
        caption: 1,
        name: 'Pinocchio Nose',
        widthPercent: 28,
        defaultOffset: { percentX: 48, percentY: 23 },
        svg: `<svg viewBox="0 0 140 40" class="w-full h-auto drop-shadow">
                <path d="M10,20 L130,5 Q135,20 130,25 L10,35 Z" fill="#f97316" stroke="#000000" stroke-width="4" stroke-linejoin="round"/>
                <circle cx="12" cy="27" r="10" fill="#ea580c" stroke="#000000" stroke-width="3"/>
              </svg>`
      },
      {
        id: 'flat-nose',
        caption: 1,
        name: 'Flat Nose',
        widthPercent: 22,
        defaultOffset: { percentX: 39, percentY: 23 },
        svg: `<svg viewBox="0 0 80 45" class="w-full h-auto drop-shadow">
                <path d="M15,10 Q40,0 65,10 Q75,35 40,40 Q5,35 15,10 Z" fill="#d97706" stroke="#78350f" stroke-width="3"/>
                <ellipse cx="28" cy="26" rx="8" ry="10" fill="#000"/>
                <ellipse cx="52" cy="26" rx="8" ry="10" fill="#000"/>
              </svg>`
      },
      {
        id: 'handlebar-moustache',
        caption: 1,
        name: 'Handlebar Stache',
        widthPercent: 28,
        defaultOffset: { percentX: 36, percentY: 29 },
        svg: `<svg viewBox="0 0 130 45" class="w-full h-auto drop-shadow">
                <path d="M65,15 Q40,5 15,20 Q0,10 5,0 Q30,5 65,22 Q100,5 125,0 Q130,10 115,20 Q90,5 65,15 Z" fill="#1e293b" stroke="#0f172a" stroke-width="2"/>
              </svg>`
      },
      {
        id: 'horseshoe-moustache',
        caption: 1,
        name: 'Horseshoe Stache',
        widthPercent: 26,
        defaultOffset: { percentX: 37, percentY: 29 },
        svg: `<svg viewBox="0 0 120 70" class="w-full h-auto drop-shadow">
                <path d="M20,65 L20,30 Q20,10 60,10 Q100,10 100,30 L100,65 L85,65 L85,32 Q85,22 60,22 Q35,22 35,32 L35,65 Z" fill="#27272a" stroke="#09090b" stroke-width="2"/>
              </svg>`
      },
      {
        id: 'blonde-hair',
        caption: 1,
        name: 'Blonde Hair',
        widthPercent: 48,
        defaultOffset: { percentX: 26, percentY: -2 },
        svg: `<svg viewBox="0 0 180 140" class="w-full h-auto drop-shadow">
                <path d="M30,50 Q40,0 90,0 Q140,0 150,50 L170,130 Q140,110 140,70 Q130,20 90,20 Q50,20 40,70 Q40,110 10,130 Z" fill="#fde047" stroke="#ca8a04" stroke-width="3"/>
              </svg>`
      },
      {
        id: 'spiky-mohawk',
        caption: 1,
        name: 'Spiky Mohawk',
        widthPercent: 30,
        defaultOffset: { percentX: 35, percentY: -6 },
        svg: `<svg viewBox="0 0 120 90" class="w-full h-auto drop-shadow">
                <path d="M10,80 L25,40 L40,75 L55,20 L70,75 L85,30 L100,80 Z" fill="#15803d" stroke="#000000" stroke-width="3"/>
                <path d="M20,80 L30,48 L42,75 L55,30 L68,75 L80,40 L90,80 Z" fill="#22c55e"/>
              </svg>`
      },

      // --- CAPTION 2: Accessories ---
      {
        id: 'headscarf',
        caption: 2,
        name: 'Desert Scarf',
        widthPercent: 50,
        defaultOffset: { percentX: 25, percentY: 1 },
        svg: `<svg viewBox="0 0 160 130" class="w-full h-auto drop-shadow">
                <path d="M20,40 Q80,-10 140,40 L155,120 L130,110 L120,60 Q80,40 40,60 L30,110 L5,120 Z" fill="#f8fafc" stroke="#dc2626" stroke-width="3"/>
                <rect x="35" y="25" width="90" height="12" rx="6" fill="#0f172a"/>
                <rect x="40" y="38" width="80" height="8" rx="4" fill="#1e293b"/>
              </svg>`
      },
      {
        id: 'plant-pot',
        caption: 2,
        name: 'Plant Pot',
        widthPercent: 44,
        defaultOffset: { percentX: 28, percentY: 75 },
        svg: `<svg viewBox="0 0 140 100" class="w-full h-auto drop-shadow">
                <path d="M10,10 L130,10 L115,90 L25,90 Z" fill="#c2410c" stroke="#7c2d12" stroke-width="4"/>
                <rect x="5" y="0" width="130" height="20" rx="5" fill="#ea580c" stroke="#7c2d12" stroke-width="4"/>
              </svg>`
      },
      {
        id: 'microphone',
        caption: 2,
        name: 'Singing Mic',
        widthPercent: 26,
        defaultOffset: { percentX: 66, percentY: 22 },
        svg: `<svg viewBox="0 0 120 120" class="w-full h-auto drop-shadow-xl">
                <ellipse cx="40" cy="30" rx="20" ry="22" fill="#94a3b8" stroke="#334155" stroke-width="3"/>
                <rect x="20" y="48" width="40" height="8" rx="3" fill="#cbd5e1" stroke="#1e293b" stroke-width="2"/>
                <path d="M24,56 L30,100 L50,100 L56,56 Z" fill="#1e293b" stroke="#0f172a" stroke-width="3"/>
              </svg>`
      },
      {
        id: 'mexican-guitar',
        caption: 2,
        name: 'Mariachi Guitar',
        widthPercent: 50,
        defaultOffset: { percentX: 25, percentY: 42 },
        svg: `<svg viewBox="0 0 160 90" class="w-full h-auto drop-shadow">
                <path d="M10,45 Q20,10 50,20 Q70,35 90,20 Q110,10 120,45 Q110,80 90,70 Q70,55 50,70 Q20,80 10,45 Z" fill="#ffffff" stroke="#000" stroke-width="3"/>
                <path d="M10,45 Q20,10 50,20 L50,70 Q20,80 10,45 Z" fill="#16a34a"/>
                <path d="M90,20 Q110,10 120,45 Q110,80 90,70 L90,20 Z" fill="#dc2626"/>
                <circle cx="70" cy="45" r="12" fill="#451a03"/>
                <rect x="115" y="40" width="40" height="10" fill="#78350f" stroke="#000" stroke-width="2"/>
              </svg>`
      },
      {
        id: 'punk-guitar',
        caption: 2,
        name: 'Punk Guitar',
        widthPercent: 50,
        defaultOffset: { percentX: 25, percentY: 40 },
        svg: `<svg viewBox="0 0 160 110" class="w-full h-auto drop-shadow-2xl">
                <path d="M10,15 L75,50 L10,100 L45,50 Z" fill="#ec4899" stroke="#831843" stroke-width="4" stroke-linejoin="round"/>
                <path d="M22,28 L60,48 L22,78 L38,50 Z" fill="#f8fafc" stroke="#cbd5e1" stroke-width="2"/>
                <rect x="70" y="45" width="70" height="10" fill="#334155" stroke="#0f172a" stroke-width="2.5" transform="rotate(-12 70 45)"/>
              </svg>`
      },
      {
        id: 'sombrero-hat',
        caption: 2,
        name: 'Sombrero',
        widthPercent: 56,
        defaultOffset: { percentX: 22, percentY: -8 },
        svg: `<svg viewBox="0 0 180 90" class="w-full h-auto drop-shadow">
                <ellipse cx="90" cy="65" rx="85" ry="20" fill="#f59e0b" stroke="#78350f" stroke-width="4"/>
                <path d="M50,60 Q55,10 90,10 Q125,10 130,60 Z" fill="#d97706" stroke="#78350f" stroke-width="4"/>
                <path d="M10,65 Q90,85 170,65" stroke="#ef4444" stroke-width="5" fill="none" stroke-dasharray="10,6"/>
              </svg>`
      },
      {
        id: 'baseball-cap',
        caption: 2,
        name: 'Baseball Cap',
        widthPercent: 36,
        defaultOffset: { percentX: 32, percentY: -1 },
        svg: `<svg viewBox="0 0 120 70" class="w-full h-auto drop-shadow">
                <path d="M20,45 Q20,10 60,10 Q100,10 100,45 Z" fill="#3b82f6" stroke="#1d4ed8" stroke-width="3"/>
                <path d="M20,45 Q20,10 60,10 L60,45 Z" fill="#ef4444"/>
                <path d="M15,45 Q-10,50 30,65 Q70,50 100,45 Z" fill="#facc15" stroke="#ca8a04" stroke-width="3"/>
              </svg>`
      },
      {
        id: 'usa-sunglasses',
        caption: 2,
        name: 'USA Glasses',
        widthPercent: 32,
        defaultOffset: { percentX: 34, percentY: 16 },
        svg: `<svg viewBox="0 0 120 50" class="w-full h-auto drop-shadow">
                <rect x="10" y="10" width="45" height="30" rx="8" fill="#1e3a8a" stroke="#000" stroke-width="3"/>
                <rect x="65" y="10" width="45" height="30" rx="8" fill="#b91c1c" stroke="#000" stroke-width="3"/>
                <line x1="55" y1="20" x2="65" y2="20" stroke="#000" stroke-width="4"/>
                <circle cx="22" cy="20" r="3" fill="#fff"/>
                <circle cx="38" cy="28" r="3" fill="#fff"/>
                <line x1="70" y1="20" x2="105" y2="20" stroke="#fff" stroke-width="3"/>
                <line x1="70" y1="30" x2="105" y2="30" stroke="#fff" stroke-width="3"/>
              </svg>`
      },
      {
        id: 'golden-crown',
        caption: 2,
        name: 'Golden Crown',
        widthPercent: 34,
        defaultOffset: { percentX: 33, percentY: -5 },
        svg: `<svg viewBox="0 0 120 80" class="w-full h-auto drop-shadow">
                <path d="M10,70 L20,20 L45,50 L60,10 L75,50 L100,20 L110,70 Z" fill="#eab308" stroke="#a16207" stroke-width="3"/>
                <circle cx="20" cy="20" r="5" fill="#ef4444"/>
                <circle cx="60" cy="10" r="5" fill="#3b82f6"/>
                <circle cx="100" cy="20" r="5" fill="#10b981"/>
              </svg>`
      }
    ];

    let gameStarted = false;
    let timerSeconds = 90;
    let timerInterval = null;
    let attachedItems = [];
    const MAX_ITEMS = 8;

    const attachedLayer = document.getElementById('attached-layer');
    const counterDisplay = document.getElementById('item-counter');
    const caption3Panel = document.getElementById('caption3-panel');
    const cactusContainer = document.getElementById('cactus-container');

    /* Starts timer immediately on ANY user selection across all 3 captions */
    function startTimerIfNeeded() {
      if (!gameStarted) {
        gameStarted = true;
        timerInterval = setInterval(() => {
          timerSeconds--;
          document.getElementById('timer').textContent = timerSeconds;
          if (timerSeconds <= 0) {
            clearInterval(timerInterval);
            triggerPhotoModal();
          }
        }, 1000);
      }
    }

    function renderPanels() {
      const list1 = document.getElementById('caption1-list');
      const list2 = document.getElementById('caption2-list');
      list1.innerHTML = '';
      list2.innerHTML = '';

      itemsData.forEach(item => {
        const card = document.createElement('div');
        card.className = "bg-white p-1.5 sm:p-2 rounded-xl border border-amber-200 shadow-sm flex items-center justify-between cursor-pointer hover:bg-amber-100/80 active:scale-95 transition select-none";
        card.setAttribute('data-id', item.id);
        card.innerHTML = `
          <div class="w-8 h-8 sm:w-10 sm:h-10 flex items-center justify-center p-0.5 bg-amber-50 rounded-lg border border-amber-200 shrink-0 pointer-events-none">
            ${item.svg}
          </div>
          <span class="text-[11px] sm:text-xs font-bold text-amber-950 flex-1 ml-1.5 leading-tight truncate pointer-events-none">${item.name}</span>
          <button class="btn-add bg-gradient-to-r from-emerald-500 to-teal-600 text-white px-3 sm:px-4 py-1.5 sm:py-2 rounded-xl text-xs sm:text-sm font-black shadow-md hover:from-emerald-600 hover:to-teal-700 active:scale-95 shrink-0 min-w-[42px] sm:min-w-[52px] text-center border border-emerald-300 pointer-events-none">
            +
          </button>
        `;

        /* Clicking item card attaches item & starts the game timer */
        card.addEventListener('click', () => {
          startTimerIfNeeded();
          toggleItem(item.id);
        });

        if (item.caption === 1) {
          list1.appendChild(card);
        } else {
          list2.appendChild(card);
        }
      });
      updatePanelCardStates();
    }

    function updatePanelCardStates() {
      itemsData.forEach(item => {
        const card = document.querySelector(`[data-id="${item.id}"]`);
        if (!card) return;
        const isAttached = attachedItems.some(i => i.id === item.id);
        const btn = card.querySelector('.btn-add');
        if (isAttached) {
          card.classList.add('bg-emerald-100/90', 'border-emerald-500', 'ring-2', 'ring-emerald-400');
          card.classList.remove('hover:bg-amber-100/80', 'bg-white');
          if (btn) {
            btn.textContent = '✓';
            btn.className = 'btn-add bg-rose-500 text-white px-3 sm:px-4 py-1.5 sm:py-2 rounded-xl text-xs sm:text-sm font-black shadow-md hover:bg-rose-600 active:scale-95 shrink-0 min-w-[42px] sm:min-w-[52px] text-center border border-rose-300 pointer-events-none';
          }
        } else {
          card.classList.remove('bg-emerald-100/90', 'border-emerald-500', 'ring-2', 'ring-emerald-400');
          card.classList.add('bg-white');
          if (btn) {
            btn.textContent = '+';
            btn.className = 'btn-add bg-gradient-to-r from-emerald-500 to-teal-600 text-white px-3 sm:px-4 py-1.5 sm:py-2 rounded-xl text-xs sm:text-sm font-black shadow-md hover:from-emerald-600 hover:to-teal-700 active:scale-95 shrink-0 min-w-[42px] sm:min-w-[52px] text-center border border-emerald-300 pointer-events-none';
          }
        }
      });
    }

    function toggleItem(itemId) {
      const existingIdx = attachedItems.findIndex(i => i.id === itemId);
      if (existingIdx !== -1) {
        removeItem(itemId);
      } else {
        attachItemToCactus(itemId);
      }
    }

    function attachItemToCactus(itemId, percentPos = null) {
      sound.playPop();

      const existingIdx = attachedItems.findIndex(i => i.id === itemId);
      if (existingIdx !== -1) {
        if (percentPos) {
          attachedItems[existingIdx].customPercentPos = percentPos;
          renderAttachedLayer();
        }
        return;
      }

      if (attachedItems.length >= MAX_ITEMS) {
        alert("Maximum limit of 8 items reached! Remove an item to swap, or try the Commands now!");
        return;
      }

      const itemDef = itemsData.find(i => i.id === itemId);
      if (!itemDef) return;

      attachedItems.push({
        id: itemDef.id,
        itemDef: itemDef,
        customPercentPos: percentPos
      });

      updateItemCounter();
      updatePanelCardStates();
      renderAttachedLayer();
    }

    function removeItem(itemId) {
      sound.playRemove();
      attachedItems = attachedItems.filter(i => i.id !== itemId);
      updateItemCounter();
      updatePanelCardStates();
      renderAttachedLayer();
    }

    function updateItemCounter() {
      counterDisplay.textContent = `${attachedItems.length} / ${MAX_ITEMS}`;
      if (attachedItems.length >= MAX_ITEMS) {
        caption3Panel.classList.add('flash-command');
      } else {
        caption3Panel.classList.remove('flash-command');
      }
    }

    function renderAttachedLayer() {
      attachedLayer.innerHTML = '';
      const bodyRect = attachedLayer.getBoundingClientRect();
      if (!bodyRect.width || !bodyRect.height) return;

      attachedItems.forEach(attached => {
        const el = document.createElement('div');
        el.className = "absolute cursor-grab active:cursor-grabbing touch-none select-none group";

        const itemWidth = bodyRect.width * ((attached.itemDef.widthPercent || 30) / 100);

        let pctX, pctY;
        if (attached.customPercentPos) {
          pctX = attached.customPercentPos.x;
          pctY = attached.customPercentPos.y;
        } else {
          pctX = attached.itemDef.defaultOffset.percentX;
          pctY = attached.itemDef.defaultOffset.percentY;
        }

        const posX = (bodyRect.width * (pctX / 100));
        const posY = (bodyRect.height * (pctY / 100));

        el.style.left = `${posX}px`;
        el.style.top = `${posY}px`;
        el.style.width = `${itemWidth}px`;

        el.innerHTML = `
          <div class="w-full h-auto relative drop-shadow-md">
            ${attached.itemDef.svg}
          </div>
        `;

        setupDragHandlers(el, attached, pctX, pctY, bodyRect);
        attachedLayer.appendChild(el);
      });
    }

    /* Touch/Mouse dragging repositioning on cactus */
    function setupDragHandlers(element, attachedObj, initialPctX, initialPctY, bodyRect) {
      let isDragging = false;
      let startClientX, startClientY;
      let startPctX = initialPctX;
      let startPctY = initialPctY;

      const onStart = (clientX, clientY) => {
        isDragging = true;
        startClientX = clientX;
        startClientY = clientY;
        startPctX = attachedObj.customPercentPos ? attachedObj.customPercentPos.x : attachedObj.itemDef.defaultOffset.percentX;
        startPctY = attachedObj.customPercentPos ? attachedObj.customPercentPos.y : attachedObj.itemDef.defaultOffset.percentY;
      };

      const onMove = (clientX, clientY) => {
        if (!isDragging) return;
        const currentBodyRect = attachedLayer.getBoundingClientRect();
        if (!currentBodyRect.width || !currentBodyRect.height) return;

        const deltaPxX = clientX - startClientX;
        const deltaPxY = clientY - startClientY;

        const deltaPctX = (deltaPxX / currentBodyRect.width) * 100;
        const deltaPctY = (deltaPxY / currentBodyRect.height) * 100;

        const newPctX = startPctX + deltaPctX;
        const newPctY = startPctY + deltaPctY;

        attachedObj.customPercentPos = { x: newPctX, y: newPctY };

        element.style.left = `${(currentBodyRect.width * (newPctX / 100))}px`;
        element.style.top = `${(currentBodyRect.height * (newPctY / 100))}px`;
      };

      const onEnd = () => {
        isDragging = false;
      };

      element.addEventListener('mousedown', (e) => {
        onStart(e.clientX, e.clientY);
        const handleMouseMove = (me) => onMove(me.clientX, me.clientY);
        const handleMouseUp = () => {
          onEnd();
          window.removeEventListener('mousemove', handleMouseMove);
          window.removeEventListener('mouseup', handleMouseUp);
        };
        window.addEventListener('mousemove', handleMouseMove);
        window.addEventListener('mouseup', handleMouseUp);
      });

      element.addEventListener('touchstart', (e) => {
        const touch = e.touches[0];
        onStart(touch.clientX, touch.clientY);
      }, { passive: true });

      element.addEventListener('touchmove', (e) => {
        if (!isDragging) return;
        const touch = e.touches[0];
        onMove(touch.clientX, touch.clientY);
      }, { passive: true });

      element.addEventListener('touchend', () => onEnd());
    }

    document.getElementById('cmd-dive').addEventListener('click', () => {
      startTimerIfNeeded();
      cactusContainer.classList.add('cactus-dive');
      
      const splash = document.getElementById('splash-effect');
      setTimeout(() => {
        sound.playSplash();
        splash.classList.remove('hidden');
      }, 1800);

      setTimeout(() => {
        splash.classList.add('hidden');
      }, 3000);

      setTimeout(() => {
        cactusContainer.classList.remove('cactus-dive');
      }, 3800);
    });

    document.getElementById('cmd-moonwalk').addEventListener('click', () => {
      startTimerIfNeeded();
      sound.playBillieJean();
      cactusContainer.classList.add('cactus-moonwalk');
      
      setTimeout(() => {
        cactusContainer.classList.remove('cactus-moonwalk');
      }, 6000);
    });

    const weatherCanvas = document.getElementById('weather-canvas');
    let weatherCtx = weatherCanvas.getContext('2d');
    let weatherAnimId = null;

    document.getElementById('cmd-thunder').addEventListener('click', () => {
      startTimerIfNeeded();
      sound.playThunder();
      weatherCanvas.classList.remove('hidden');
      weatherCanvas.width = window.innerWidth;
      weatherCanvas.height = window.innerHeight;

      let drops = Array.from({ length: 120 }, () => ({
        x: Math.random() * weatherCanvas.width,
        y: Math.random() * weatherCanvas.height,
        len: Math.random() * 20 + 10,
        speed: Math.random() * 10 + 15
      }));

      let flashAlpha = 0;
      let startTime = Date.now();

      function drawWeather() {
        weatherCtx.clearRect(0, 0, weatherCanvas.width, weatherCanvas.height);
        
        if (Math.random() < 0.08) flashAlpha = 0.6;
        if (flashAlpha > 0) {
          weatherCtx.fillStyle = `rgba(255, 255, 255, ${flashAlpha})`;
          weatherCtx.fillRect(0, 0, weatherCanvas.width, weatherCanvas.height);
          flashAlpha -= 0.1;
        }

        weatherCtx.strokeStyle = 'rgba(186, 230, 253, 0.7)';
        weatherCtx.lineWidth = 2;
        weatherCtx.beginPath();
        drops.forEach(d => {
          weatherCtx.moveTo(d.x, d.y);
          weatherCtx.lineTo(d.x - 2, d.y + d.len);
          d.y += d.speed;
          if (d.y > weatherCanvas.height) d.y = -20;
        });
        weatherCtx.stroke();

        if (Date.now() - startTime < 6000) {
          weatherAnimId = requestAnimationFrame(drawWeather);
        } else {
          weatherCanvas.classList.add('hidden');
          cancelAnimationFrame(weatherAnimId);
        }
      }

      drawWeather();
    });

    document.getElementById('btn-take-photo-now').addEventListener('click', () => {
      clearInterval(timerInterval);
      triggerPhotoModal();
    });

    function triggerPhotoModal() {
      const modal = document.getElementById('photo-modal');
      const photoContent = document.getElementById('photo-content');
      
      photoContent.innerHTML = '';

      const wrapper = document.createElement('div');
      wrapper.className = "relative w-full h-full flex items-end justify-center px-1 pb-1 overflow-hidden";

      const oasisClone = document.getElementById('oasis-container').cloneNode(true);
      oasisClone.style.position = 'relative';
      oasisClone.style.left = '0';
      oasisClone.style.bottom = '0';
      oasisClone.style.transform = 'scale(0.52)';
      oasisClone.style.transformOrigin = 'bottom center';
      oasisClone.style.margin = '0 -25px -10px -25px';

      const cactusClone = cactusContainer.cloneNode(true);
      cactusClone.style.position = 'relative';
      cactusClone.style.left = '0';
      cactusClone.style.right = '0';
      cactusClone.style.bottom = '0';
      cactusClone.style.transform = 'scale(0.52)';
      cactusClone.style.transformOrigin = 'bottom center';
      cactusClone.style.margin = '0 -25px -10px -25px';

      wrapper.appendChild(oasisClone);
      wrapper.appendChild(cactusClone);
      photoContent.appendChild(wrapper);

      modal.classList.remove('hidden');
    }

    const photoFrame = document.getElementById('photo-frame');
    document.getElementById('btn-filter-normal').addEventListener('click', () => {
      photoFrame.className = "relative w-full h-80 bg-gradient-to-b from-sky-200 via-amber-100 to-amber-200 rounded-2xl border-4 border-amber-800 overflow-hidden shadow-inner flex items-center justify-center transition-all duration-300";
    });

    document.getElementById('btn-filter-insta').addEventListener('click', () => {
      photoFrame.className = "relative w-full h-80 bg-gradient-to-b from-sky-200 via-amber-100 to-amber-200 rounded-2xl border-4 border-amber-800 overflow-hidden shadow-inner flex items-center justify-center transition-all duration-300 filter-instagram";
    });

    document.getElementById('btn-filter-funky').addEventListener('click', () => {
      photoFrame.className = "relative w-full h-80 bg-gradient-to-b from-sky-200 via-amber-100 to-amber-200 rounded-2xl border-4 border-amber-800 overflow-hidden shadow-inner flex items-center justify-center transition-all duration-300 filter-funky";
    });

    document.getElementById('btn-restart').addEventListener('click', () => {
      location.reload();
    });

    window.addEventListener('resize', () => {
      renderAttachedLayer();
    });

    window.onload = function() {
      renderPanels();
    };
  </script>
</body>
</html>
