# Enigma
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" width="1000" height="300" viewBox="0 0 1000 300" preserveAspectRatio="xMidYMid meet">
  <defs>
    <!-- создаём эффект волны -->
    <filter id="wave">
      <feTurbulence id="turb" baseFrequency="0.02 0.03" numOctaves="2" result="turbulence"/>
      <feDisplacementMap in2="turbulence" in="SourceGraphic" scale="15" xChannelSelector="R" yChannelSelector="G"/>
      <animate xlink:href="#turb" attributeName="baseFrequency" dur="10s"
        values="0.02 0.03;0.04 0.06;0.02 0.03" repeatCount="indefinite"/>
    </filter>
    <style>
      .flag-text {
        font: bold 60px 'Segoe UI', sans-serif;
        fill: #ffffff;
        stroke: #00000055;
        stroke-width: 2px;
      }
    </style>
  </defs>

  <g filter="url(#wave)">
    <!-- верхняя полоса (голубая) -->
    <rect x="0" y="0" width="1000" height="100" fill="#1eb1e6"/>
    <!-- белая полоса -->
    <rect x="0" y="100" width="1000" height="100" fill="#ffffff"/>
    <!-- зелёная полоса -->
    <rect x="0" y="200" width="1000" height="100" fill="#1ca354"/>
    <!-- красные разделители -->
    <rect x="0" y="95" width="1000" height="5" fill="#d51b1b"/>
    <rect x="0" y="195" width="1000" height="5" fill="#d51b1b"/>

    <!-- полумесяц -->
    <circle cx="80" cy="50" r="24" fill="#ffffff"/>
    <circle cx="88" cy="50" r="24" fill="#1eb1e6"/>

    <!-- звёзды -->
    <g fill="#ffffff">
      <circle cx="120" cy="25" r="3"/>
      <circle cx="140" cy="35" r="3"/>
      <circle cx="160" cy="25" r="3"/>
      <circle cx="180" cy="35" r="3"/>
      <circle cx="200" cy="25" r="3"/>
      <circle cx="220" cy="35" r="3"/>
      <circle cx="240" cy="25" r="3"/>
      <circle cx="260" cy="35" r="3"/>
      <circle cx="280" cy="25" r="3"/>
      <circle cx="300" cy="35" r="3"/>
      <circle cx="320" cy="25" r="3"/>
      <circle cx="340" cy="35" r="3"/>
    </g>

    <!-- текст ENIGMA -->
    <text x="500" y="170" text-anchor="middle" class="flag-text">ENIGMA</text>
  </g>
</svg>
