<svg width="100%" viewBox="0 0 1200 900"
     xmlns="http://www.w3.org/2000/svg">

  <defs>

    <!-- Background -->
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#030712"/>
      <stop offset="50%" stop-color="#07142d"/>
      <stop offset="100%" stop-color="#16052e"/>
    </linearGradient>

    <!-- Neon gradients -->
    <linearGradient id="cyanPurple" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="50%" stop-color="#8b5cf6"/>
      <stop offset="100%" stop-color="#ec4899"/>
    </linearGradient>

    <linearGradient id="rainbow" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="35%" stop-color="#8b5cf6"/>
      <stop offset="70%" stop-color="#ec4899"/>
      <stop offset="100%" stop-color="#facc15"/>
    </linearGradient>

    <!-- Glow -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="5" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="strongGlow">
      <feGaussianBlur stdDeviation="9" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Animated background glow -->
    <radialGradient id="orb">
      <stop offset="0%" stop-color="#22d3ee" stop-opacity=".35"/>
      <stop offset="100%" stop-color="#22d3ee" stop-opacity="0"/>
    </radialGradient>

    <radialGradient id="orbPink">
      <stop offset="0%" stop-color="#ec4899" stop-opacity=".3"/>
      <stop offset="100%" stop-color="#ec4899" stop-opacity="0"/>
    </radialGradient>

    <clipPath id="clip">
      <rect width="1200" height="900" rx="25"/>
    </clipPath>

  </defs>


  <!-- ===================================================== -->
  <!-- BACKGROUND -->
  <!-- ===================================================== -->

  <g clip-path="url(#clip)">

    <rect width="1200" height="900" fill="url(#bg)"/>

    <!-- Moving glow -->
    <circle cx="150" cy="150" r="230" fill="url(#orb)">
      <animate
        attributeName="cx"
        values="150;300;150"
        dur="8s"
        repeatCount="indefinite"/>
    </circle>

    <circle cx="1050" cy="700" r="250" fill="url(#orbPink)">
      <animate
        attributeName="cy"
        values="700;580;700"
        dur="9s"
        repeatCount="indefinite"/>
    </circle>


    <!-- ================================================= -->
    <!-- STARS -->
    <!-- ================================================= -->

    <g fill="#ffffff">

      <circle cx="70" cy="80" r="2">
        <animate attributeName="opacity"
                 values=".2;1;.2"
                 dur="2s"
                 repeatCount="indefinite"/>
      </circle>

      <circle cx="1120" cy="110" r="2">
        <animate attributeName="opacity"
                 values="1;.2;1"
                 dur="3s"
                 repeatCount="indefinite"/>
      </circle>

      <circle cx="100" cy="720" r="1.5">
        <animate attributeName="opacity"
                 values=".1;1;.1"
                 dur="2.5s"
                 repeatCount="indefinite"/>
      </circle>

      <circle cx="1080" cy="420" r="1.5">
        <animate attributeName="opacity"
                 values=".2;1;.2"
                 dur="3.2s"
                 repeatCount="indefinite"/>
      </circle>

      <circle cx="600" cy="40" r="1.5">
        <animate attributeName="opacity"
                 values="1;.2;1"
                 dur="2.7s"
                 repeatCount="indefinite"/>
      </circle>

    </g>


    <!-- ================================================= -->
    <!-- TITLE -->
    <!-- ================================================= -->

    <text x="600"
          y="65"
          text-anchor="middle"
          font-family="Arial, sans-serif"
          font-size="38"
          font-weight="800"
          fill="url(#rainbow)"
          filter="url(#strongGlow)">

      🌱 Learning Journey

      <animate
        attributeName="opacity"
        values=".7;1;.7"
        dur="3s"
        repeatCount="indefinite"/>

    </text>

    <text x="600"
          y="95"
          text-anchor="middle"
          font-family="Arial, sans-serif"
          font-size="17"
          fill="#a5f3fc">

      From Learning → To Building → To Making an Impact

    </text>


    <!-- ================================================= -->
    <!-- SOFTWARE ENGINEERING -->
    <!-- ================================================= -->

    <rect x="390"
          y="125"
          width="420"
          height="70"
          rx="35"
          fill="#08152f"
          stroke="url(#cyanPurple)"
          stroke-width="3"
          filter="url(#glow)"/>

    <text x="600"
          y="169"
          text-anchor="middle"
          font-family="Arial, sans-serif"
          font-size="24"
          font-weight="800"
          fill="#ffffff">

      👩‍💻 SOFTWARE ENGINEERING

    </text>


    <!-- ================================================= -->
    <!-- CONNECTORS -->
    <!-- ================================================= -->

    <g fill="none"
       stroke="url(#cyanPurple)"
       stroke-width="3"
       filter="url(#glow)">

      <path d="M600 195 L600 220"/>

      <path d="M600 220 L190 220 L190 250"/>

      <path d="M600 220 L600 250"/>

      <path d="M600 220 L1010 220 L1010 250"/>

    </g>


    <!-- Animated particles on connector -->
    <circle r="5" fill="#22d3ee" filter="url(#glow)">

      <animateMotion
        path="M600 195 L600 220 L190 220 L190 250"
        dur="3s"
        repeatCount="indefinite"/>

    </circle>

    <circle r="5" fill="#a78bfa" filter="url(#glow)">

      <animateMotion
        path="M600 195 L600 220"
        dur="2s"
        repeatCount="indefinite"/>

    </circle>

    <circle r="5" fill="#facc15" filter="url(#glow)">

      <animateMotion
        path="M600 195 L600 220 L1010 220 L1010 250"
        dur="3s"
        repeatCount="indefinite"/>

    </circle>


    <!-- ================================================= -->
    <!-- DEVELOPMENT -->
    <!-- ================================================= -->

    <rect x="70"
          y="250"
          width="240"
          height="55"
          rx="27"
          fill="#071b35"
          stroke="#22d3ee"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="190"
          y="285"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#67e8f9">

      💻 DEVELOPMENT

    </text>


    <!-- MOBILE -->

    <rect x="480"
          y="250"
          width="240"
          height="55"
          rx="27"
          fill="#180d36"
          stroke="#a78bfa"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="600"
          y="285"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#c4b5fd">

      📱 MOBILE

    </text>


    <!-- AI -->

    <rect x="890"
          y="250"
          width="240"
          height="55"
          rx="27"
          fill="#24180b"
          stroke="#facc15"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="1010"
          y="285"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#fde68a">

      🤖 AI

    </text>


    <!-- ================================================= -->
    <!-- CARD FUNCTION -->
    <!-- ================================================= -->

    <!-- Frontend -->

    <rect x="40"
          y="330"
          width="270"
          height="175"
          rx="18"
          fill="#071426"
          stroke="#22d3ee"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="175"
          y="365"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#67e8f9">

      🎨 Frontend

    </text>

    <text x="65" y="400"
          font-family="Arial"
          font-size="15"
          fill="#dbeafe">

      • HTML

    </text>

    <text x="65" y="425"
          font-family="Arial"
          font-size="15"
          fill="#dbeafe">

      • CSS

    </text>

    <text x="65" y="450"
          font-family="Arial"
          font-size="15"
          fill="#dbeafe">

      • JavaScript

    </text>

    <text x="65" y="475"
          font-family="Arial"
          font-size="15"
          fill="#dbeafe">

      • React

    </text>


    <!-- Backend -->

    <rect x="330"
          y="330"
          width="270"
          height="175"
          rx="18"
          fill="#071426"
          stroke="#22d3ee"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="465"
          y="365"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#67e8f9">

      ⚙️ Backend

    </text>

    <text x="355" y="405"
          font-family="Arial"
          font-size="15"
          fill="#dbeafe">

      • Python

    </text>

    <text x="355" y="435"
          font-family="Arial"
          font-size="15"
          fill="#dbeafe">

      • Django

    </text>

    <text x="355" y="465"
          font-family="Arial"
          font-size="15"
          fill="#dbeafe">

      • APIs

    </text>


    <!-- Flutter -->

    <rect x="620"
          y="330"
          width="270"
          height="175"
          rx="18"
          fill="#130d2d"
          stroke="#a78bfa"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="755"
          y="365"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#c4b5fd">

      📱 Flutter

    </text>

    <text x="645" y="405"
          font-family="Arial"
          font-size="15"
          fill="#ede9fe">

      • Flutter

    </text>

    <text x="645" y="435"
          font-family="Arial"
          font-size="15"
          fill="#ede9fe">

      • Dart

    </text>

    <text x="645" y="465"
          font-family="Arial"
          font-size="15"
          fill="#ede9fe">

      • Firebase

    </text>


    <!-- Dart -->

    <rect x="910"
          y="330"
          width="250"
          height="175"
          rx="18"
          fill="#21170b"
          stroke="#facc15"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="1035"
          y="365"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#fde68a">

      🤖 AI Tools

    </text>

    <text x="935" y="405"
          font-family="Arial"
          font-size="15"
          fill="#fef3c7">

      • AI APIs

    </text>

    <text x="935" y="435"
          font-family="Arial"
          font-size="15"
          fill="#fef3c7">

      • AI Integration

    </text>

    <text x="935" y="465"
          font-family="Arial"
          font-size="15"
          fill="#fef3c7">

      • Automation

    </text>


    <!-- ================================================= -->
    <!-- UI UX -->
    <!-- ================================================= -->

    <path d="M175 505 L175 545 L350 545"
          fill="none"
          stroke="#ec4899"
          stroke-width="3"
          filter="url(#glow)"/>

    <path d="M755 505 L755 545 L850 545"
          fill="none"
          stroke="#22d3ee"
          stroke-width="3"
          filter="url(#glow)"/>


    <rect x="120"
          y="550"
          width="460"
          height="55"
          rx="27"
          fill="#260d25"
          stroke="#ec4899"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="350"
          y="585"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#f9a8d4">

      🎨 UI/UX DESIGN

    </text>


    <!-- Cybersecurity -->

    <rect x="650"
          y="550"
          width="430"
          height="55"
          rx="27"
          fill="#071f27"
          stroke="#22d3ee"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="865"
          y="585"
          text-anchor="middle"
          font-family="Arial"
          font-size="20"
          font-weight="700"
          fill="#67e8f9">

      🛡️ CYBERSECURITY

    </text>


    <!-- ================================================= -->
    <!-- BOTTOM CARDS -->
    <!-- ================================================= -->

    <rect x="100"
          y="630"
          width="230"
          height="120"
          rx="18"
          fill="#170d25"
          stroke="#ec4899"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="215"
          y="665"
          text-anchor="middle"
          font-family="Arial"
          font-size="18"
          font-weight="700"
          fill="#f9a8d4">

      🎨 Figma

    </text>

    <text x="125"
          y="700"
          font-family="Arial"
          font-size="14"
          fill="#fce7f3">

      • Design Systems

    </text>

    <text x="125"
          y="725"
          font-family="Arial"
          font-size="14"
          fill="#fce7f3">

      • Wireframing

    </text>


    <rect x="370"
          y="630"
          width="230"
          height="120"
          rx="18"
          fill="#170d25"
          stroke="#a78bfa"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="485"
          y="665"
          text-anchor="middle"
          font-family="Arial"
          font-size="18"
          font-weight="700"
          fill="#c4b5fd">

      ✨ Prototyping

    </text>

    <text x="395"
          y="700"
          font-family="Arial"
          font-size="14"
          fill="#ede9fe">

      • User Research

    </text>

    <text x="395"
          y="725"
          font-family="Arial"
          font-size="14"
          fill="#ede9fe">

      • User Experience

    </text>


    <rect x="650"
          y="630"
          width="190"
          height="120"
          rx="18"
          fill="#071d25"
          stroke="#22d3ee"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="745"
          y="665"
          text-anchor="middle"
          font-family="Arial"
          font-size="18"
          font-weight="700"
          fill="#67e8f9">

      🌐 Web Security

    </text>

    <text x="670"
          y="700"
          font-family="Arial"
          font-size="14"
          fill="#cffafe">

      • OWASP

    </text>

    <text x="670"
          y="725"
          font-family="Arial"
          font-size="14"
          fill="#cffafe">

      • Secure Coding

    </text>


    <rect x="870"
          y="630"
          width="190"
          height="120"
          rx="18"
          fill="#071d25"
          stroke="#4ade80"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="965"
          y="665"
          text-anchor="middle"
          font-family="Arial"
          font-size="18"
          font-weight="700"
          fill="#86efac">

      🔐 Secure Coding

    </text>

    <text x="890"
          y="700"
          font-family="Arial"
          font-size="14"
          fill="#dcfce7">

      • Best Practices

    </text>

    <text x="890"
          y="725"
          font-family="Arial"
          font-size="14"
          fill="#dcfce7">

      • Security Awareness

    </text>


    <!-- ================================================= -->
    <!-- FOOTER -->
    <!-- ================================================= -->

    <line x1="100"
          y1="790"
          x2="1100"
          y2="790"
          stroke="url(#rainbow)"
          stroke-width="2"
          filter="url(#glow)"/>

    <text x="600"
          y="830"
          text-anchor="middle"
          font-family="Arial"
          font-size="23"
          font-weight="800"
          fill="url(#rainbow)">

      🚀 Learn • Build • Improve • Repeat

    </text>

    <text x="600"
          y="860"
          text-anchor="middle"
          font-family="Arial"
          font-size="15"
          fill="#94a3b8">

      Turning ideas into real-world digital solutions.

    </text>


    <!-- Moving scan line -->

    <rect x="100"
          y="785"
          width="180"
          height="3"
          fill="#22d3ee"
          filter="url(#glow)">

      <animate
        attributeName="x"
        values="100;920;100"
        dur="5s"
        repeatCount="indefinite"/>

    </rect>

  </g>


  <!-- Border -->

  <rect x="3"
        y="3"
        width="1194"
        height="894"
        rx="25"
        fill="none"
        stroke="url(#rainbow)"
        stroke-width="2"
        opacity=".7"
        filter="url(#glow)"/>

</svg>
