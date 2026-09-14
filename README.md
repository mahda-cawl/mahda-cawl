<!DOCTYPE html>
<html lang="so" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Profile README Builder & Showcase</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        github: {
                            dark: '#0d1117',
                            card: '#161b22',
                            border: '#30363d',
                            accent: '#238636',
                            blue: '#58a6ff',
                            purple: '#bc8cff',
                            text: '#c9d1d9',
                            muted: '#8b949e'
                        }
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-10px)' },
                        },
                        pulseGlow: {
                            '0%, 100%': { opacity: '0.4', filter: 'drop-shadow(0 0 15px rgba(88,166,255,0.6))' },
                            '50%': { opacity: '0.8', filter: 'drop-shadow(0 0 25px rgba(188,140,255,0.9))' },
                        },
                        rocketFly: {
                            '0%, 100%': { transform: 'translate(0, 0) rotate(0deg)' },
                            '50%': { transform: 'translate(8px, -12px) rotate(3deg)' },
                        },
                        codeScroll: {
                            '0%': { strokeDashoffset: '100' },
                            '100%': { strokeDashoffset: '0' },
                        }
                    },
                    animation: {
                        'float': 'float 4s ease-in-out infinite',
                        'pulse-glow': 'pulseGlow 3s infinite',
                        'rocket': 'rocketFly 3s ease-in-out infinite',
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome for GitHub Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
        code, pre { font-family: 'Fira Code', monospace; }
        
        /* Custom Glowing Elements */
        .glow-box {
            box-shadow: 0 0 25px -5px rgba(88, 166, 255, 0.15);
        }
        
        .animated-dash {
            stroke-dasharray: 10;
            animation: dash 20s linear infinite;
        }

        @keyframes dash {
            to {
                stroke-dashoffset: -1000;
            }
        }
    </style>
</head>
<body class="bg-github-dark text-github-text min-h-screen p-4 md:p-8 flex flex-col items-center justify-start">

    <!-- Top Navigation Header -->
    <header class="w-full max-w-6xl mb-8 flex flex-col sm:flex-row justify-between items-center border-b border-github-border pb-5 gap-4">
        <div class="flex items-center gap-3">
            <i class="fa-brands fa-github text-4xl text-white"></i>
            <div>
                <h1 class="text-xl font-bold text-white flex items-center gap-2">
                    GitHub Profile README Creator
                    <span class="text-xs bg-github-purple/20 text-github-purple px-2 py-0.5 rounded-full border border-github-purple/30">Side-by-Side</span>
                </h1>
                <p class="text-xs text-github-muted">Waxay leedahay xarakaad SVG animation ah oo aad toos kaga isticmaali karto GitHub Readme-kaaga</p>
            </div>
        </div>
        
        <!-- Tab Selector Button -->
        <div class="flex bg-github-card p-1 rounded-lg border border-github-border">
            <button id="btn-preview" onclick="switchTab('preview')" class="px-4 py-2 rounded-md text-sm font-semibold transition-all bg-github-blue/20 text-github-blue border border-github-blue/30 flex items-center gap-2">
                <i class="fa-solid fa-eye"></i> Aragtidaba (Preview)
            </button>
            <button id="btn-code" onclick="switchTab('code')" class="px-4 py-2 rounded-md text-sm font-semibold transition-all text-github-muted hover:text-white flex items-center gap-2">
                <i class="fa-solid fa-code"></i> Nuulso Code-ka (Copy Code)
            </button>
        </div>
    </header>

    <!-- MAIN CONTAINER -->
    <main class="w-full max-w-6xl bg-github-card border border-github-border rounded-xl shadow-2xl overflow-hidden glow-box">
        
        <!-- GitHub Header Bar Simulator -->
        <div class="bg-[#161b22] px-4 py-3 border-b border-github-border flex items-center justify-between text-xs text-github-muted">
            <div class="flex items-center gap-2">
                <i class="fa-regular fa-file-code text-github-blue"></i>
                <span class="font-mono text-github-text font-medium">README.md</span>
            </div>
            <div class="flex items-center gap-3">
                <span class="hidden sm:inline-block">209 lines (146 loc) · 7.24 KB</span>
                <span class="bg-github-border text-github-text px-2 py-1 rounded text-[11px] font-mono">Markdown</span>
            </div>
        </div>

        <!-- PREVIEW TAB CONTENT -->
        <div id="tab-preview" class="p-6 md:p-10">
            <!-- Simulated Readme Side-by-Side Table Layout -->
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-stretch">
                
                <!-- LEFT COLUMN: Profile Bio Text -->
                <div class="space-y-6 flex flex-col justify-between">
                    <div>
                        <p class="text-github-text text-base leading-relaxed mb-6">
                            Building modern, useful, and creative digital applications.
                        </p>

                        <!-- What I Do Section -->
                        <div class="mb-6">
                            <h2 class="text-lg font-bold text-white flex items-center gap-2 mb-3">
                                <span>🚀</span> What I Do
                            </h2>
                            <ul class="space-y-2 text-sm text-github-text pl-2">
                                <li class="flex items-center gap-3 hover:text-github-blue transition-colors">
                                    <span>💻</span> <strong class="text-white">Full-Stack Development</strong>
                                </li>
                                <li class="flex items-center gap-3 hover:text-github-blue transition-colors">
                                    <span>🎨</span> <strong class="text-white">UI/UX Design</strong>
                                </li>
                                <li class="flex items-center gap-3 hover:text-github-blue transition-colors">
                                    <span>📱</span> <strong class="text-white">Mobile App Development</strong>
                                </li>
                                <li class="flex items-center gap-3 hover:text-github-blue transition-colors">
                                    <span>🤖</span> <strong class="text-white">AI Engineering & Integration</strong>
                                </li>
                                <li class="flex items-center gap-3 hover:text-github-blue transition-colors">
                                    <span>🛡️</span> <strong class="text-white">Cybersecurity Exploration</strong>
                                </li>
                                <li class="flex items-center gap-3 hover:text-github-blue transition-colors">
                                    <span>🌱</span> <strong class="text-white">Continuous Learning & Building</strong>
                                </li>
                            </ul>
                        </div>

                        <p class="text-sm text-github-muted mb-6">
                            I enjoy transforming ideas into <strong class="text-white">real-world digital products</strong> and exploring new technologies.
                        </p>

                        <!-- My Goal Section -->
                        <div class="mb-6 border-l-2 border-github-purple/60 pl-4 py-1 bg-github-purple/5 rounded-r">
                            <h2 class="text-lg font-bold text-white flex items-center gap-2 mb-1">
                                <span>🎯</span> My Goal
                            </h2>
                            <p class="text-sm text-github-muted italic">
                                To build innovative software that solves real problems and creates meaningful digital experiences.
                            </p>
                        </div>

                        <!-- My Interests Section -->
                        <div>
                            <h2 class="text-lg font-bold text-white flex items-center gap-2 mb-3">
                                <span>💡</span> My Interests
                            </h2>
                            <ul class="grid grid-cols-1 sm:grid-cols-2 gap-2 text-sm text-github-text">
                                <li class="flex items-center gap-2">
                                    <span>🌐</span> Modern Web Applications
                                </li>
                                <li class="flex items-center gap-2">
                                    <span>📱</span> Mobile Applications
                                </li>
                                <li class="flex items-center gap-2">
                                    <span>🤖</span> Artificial Intelligence
                                </li>
                                <li class="flex items-center gap-2">
                                    <span>🔐</span> Cybersecurity
                                </li>
                                <li class="flex items-center gap-2">
                                    <span>🎨</span> User Experience
                                </li>
                            </ul>
                        </div>
                    </div>

                    <!-- Footer tagline inside README -->
                    <div class="pt-6 border-t border-github-border/50 text-xs text-github-muted italic">
                        Kobcinta Fikirkaaga Digital-ka ah | <span class="text-github-blue font-medium">Empowering Your Digital Vision</span>
                    </div>
                </div>

                <!-- RIGHT COLUMN: Interactive Animated SVG Illustration -->
                <div class="relative bg-[#090d12] border border-github-border/80 rounded-2xl p-6 flex flex-col items-center justify-center overflow-hidden min-h-[450px]">
                    
                    <!-- Background Ambient Glowing Orbs -->
                    <div class="absolute top-10 right-10 w-40 h-40 bg-github-blue/10 rounded-full blur-3xl animate-pulse"></div>
                    <div class="absolute bottom-10 left-10 w-40 h-40 bg-github-purple/10 rounded-full blur-3xl animate-pulse" style="animation-delay: 1.5s;"></div>

                    <!-- Main SVG Visual Artwork -->
                    <svg viewBox="0 0 500 500" class="w-full h-auto max-w-[440px] drop-shadow-2xl relative z-10" xmlns="http://www.w3.org/2000/svg">
                        <defs>
                            <!-- Gradients -->
                            <linearGradient id="bluePurple" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#58a6ff" />
                                <stop offset="100%" stop-color="#bc8cff" />
                            </linearGradient>
                            
                            <linearGradient id="shieldGrad" x1="0%" y1="0%" x2="0%" y2="100%">
                                <stop offset="0%" stop-color="#1f6feb" stop-opacity="0.8" />
                                <stop offset="100%" stop-color="#0d1117" stop-opacity="0.9" />
                            </linearGradient>

                            <linearGradient id="rocketGrad" x1="0%" y1="0%" x2="100%" y2="0%">
                                <stop offset="0%" stop-color="#bc8cff" />
                                <stop offset="100%" stop-color="#58a6ff" />
                            </linearGradient>

                            <!-- Glow Filter -->
                            <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
                                <feGaussianBlur stdDeviation="6" result="blur" />
                                <feComposite in="SourceGraphic" in2="blur" operator="over" />
                            </filter>
                        </defs>

                        <!-- Connecting Orbital Paths -->
                        <path d="M 100 120 Q 250 50 400 120 Q 450 250 400 380" fill="none" stroke="url(#bluePurple)" stroke-width="1.5" stroke-dasharray="4 4" class="animated-dash" opacity="0.5"/>
                        <path d="M 80 380 Q 50 200 120 100" fill="none" stroke="#58a6ff" stroke-width="1" stroke-dasharray="3 3" opacity="0.4"/>

                        <!-- TOP LEFT: Global Network (Full-Stack & UI/UX) -->
                        <g transform="translate(90, 100)" class="animate-float">
                            <circle cx="0" cy="0" r="45" fill="#0d1117" stroke="#58a6ff" stroke-width="2" filter="url(#glow)"/>
                            <circle cx="0" cy="0" r="35" fill="none" stroke="#388bfd" stroke-width="1" stroke-dasharray="2 2"/>
                            <!-- Globe Grid Lines -->
                            <ellipse cx="0" cy="0" rx="35" ry="12" fill="none" stroke="#58a6ff" stroke-width="1" opacity="0.7"/>
                            <ellipse cx="0" cy="0" rx="15" ry="35" fill="none" stroke="#58a6ff" stroke-width="1" opacity="0.7"/>
                            <line x1="-35" y1="0" x2="35" y2="0" stroke="#58a6ff" stroke-width="1"/>
                            <line x1="0" y1="-35" x2="0" y2="35" stroke="#58a6ff" stroke-width="1"/>
                            <text x="0" y="62" text-anchor="middle" fill="#58a6ff" font-size="11" font-weight="bold">Full-Stack & UI/UX</text>
                        </g>

                        <!-- TOP RIGHT: AI & Rocket Exploration -->
                        <g transform="translate(380, 100)" class="animate-rocket">
                            <!-- AI Cloud Rocket Burst -->
                            <path d="M-10,30 Q-20,50 0,60 Q20,50 10,30 Z" fill="#bc8cff" opacity="0.6" filter="url(#glow)"/>
                            <!-- Rocket body -->
                            <path d="M 0 -25 C 15 -10 15 15 12 30 L -12 30 C -15 15 -15 -10 0 -25 Z" fill="url(#rocketGrad)" />
                            <!-- Rocket Wings -->
                            <path d="M -12 10 L -22 25 L -12 25 Z" fill="#388bfd" />
                            <path d="M 12 10 L 22 25 L 12 25 Z" fill="#388bfd" />
                            <!-- Porthole -->
                            <circle cx="0" cy="-2" r="6" fill="#0d1117" stroke="#ffffff" stroke-width="1.5"/>
                            <text x="0" y="-35" text-anchor="middle" fill="#bc8cff" font-size="12" font-weight="bold">AI Rocket</text>
                        </g>

                        <!-- CENTER RIGHT: Cybersecurity Shield -->
                        <g transform="translate(420, 220)" class="animate-pulse-glow">
                            <path d="M 0 -35 L 30 -20 L 30 10 C 30 30 0 45 0 45 C 0 45 -30 30 -30 10 L -30 -20 Z" fill="url(#shieldGrad)" stroke="#58a6ff" stroke-width="2"/>
                            <!-- Binary code in shield -->
                            <text x="0" y="-5" text-anchor="middle" fill="#388bfd" font-size="9" font-family="monospace">10101</text>
                            <text x="0" y="8" text-anchor="middle" fill="#bc8cff" font-size="9" font-family="monospace">01010</text>
                            <text x="0" y="20" text-anchor="middle" fill="#388bfd" font-size="9" font-family="monospace">11001</text>
                            <text x="0" y="60" text-anchor="middle" fill="#58a6ff" font-size="11" font-weight="bold">Cybersecurity</text>
                        </g>

                        <!-- CENTER MAIN: Futuristic Developer with VR Glasses & Laptop -->
                        <g transform="translate(230, 270)">
                            <!-- Glowing Floating Desk Platform -->
                            <ellipse cx="0" cy="70" rx="120" ry="20" fill="none" stroke="url(#bluePurple)" stroke-width="2" filter="url(#glow)"/>
                            
                            <!-- Floating Screens/Windows -->
                            <rect x="-110" y="-100" width="85" height="55" rx="6" fill="#161b22" stroke="#58a6ff" stroke-width="1.5" opacity="0.9"/>
                            <line x1="-100" y1="-85" x2="-40" y2="-85" stroke="#bc8cff" stroke-width="2" stroke-linecap="round"/>
                            <line x1="-100" y1="-75" x2="-60" y2="-75" stroke="#58a6ff" stroke-width="2" stroke-linecap="round"/>
                            <line x1="-100" y1="-65" x2="-50" y2="-65" stroke="#3ea6ff" stroke-width="2" stroke-linecap="round"/>

                            <rect x="35" y="-110" width="80" height="65" rx="6" fill="#161b22" stroke="#bc8cff" stroke-width="1.5" opacity="0.9"/>
                            <line x1="45" y1="-95" x2="95" y2="-95" stroke="#58a6ff" stroke-width="2" stroke-linecap="round"/>
                            <line x1="45" y1="-85" x2="80" y2="-85" stroke="#238636" stroke-width="2" stroke-linecap="round"/>
                            <line x1="45" y1="-75" x2="100" y2="-75" stroke="#bc8cff" stroke-width="2" stroke-linecap="round"/>
                            <line x1="45" y1="-65" x2="70" y2="-65" stroke="#e3b341" stroke-width="2" stroke-linecap="round"/>

                            <!-- Developer Figure -->
                            <!-- Body / Hoodie -->
                            <path d="M -30 65 C -30 20 -20 5 0 5 C 20 5 30 20 30 65 Z" fill="#1f2937" stroke="#374151" stroke-width="2"/>
                            <!-- Head -->
                            <circle cx="0" cy="-15" r="22" fill="#d1d5db" />
                            <!-- VR Glasses / Visor -->
                            <rect x="-18" y="-22" width="36" height="14" rx="4" fill="#0d1117" stroke="#58a6ff" stroke-width="2" filter="url(#glow)"/>
                            <line x1="-14" y1="-15" x2="14" y2="-15" stroke="#bc8cff" stroke-width="2"/>
                            <!-- Headphones -->
                            <path d="M -22 -15 C -22 -35 22 -35 22 -15" fill="none" stroke="#bc8cff" stroke-width="3"/>
                            <rect x="-25" y="-20" width="6" height="12" rx="2" fill="#bc8cff"/>
                            <rect x="19" y="-20" width="6" height="12" rx="2" fill="#bc8cff"/>

                            <!-- Laptop -->
                            <path d="M -35 45 L 35 45 L 25 25 L -25 25 Z" fill="#0d1117" stroke="#58a6ff" stroke-width="1.5"/>
                            <path d="M -42 48 L 42 48 L 38 45 L -38 45 Z" fill="#30363d"/>
                            <!-- Glowing Screen Light on Face -->
                            <polygon points="-20,25 20,25 12,-5 -12,-5" fill="#58a6ff" opacity="0.15"/>
                        </g>

                        <!-- BOTTOM DIGITAL BLOCKS / BLOCKCHAIN -->
                        <g transform="translate(100, 410)" class="animate-pulse">
                            <g transform="translate(0,0)">
                                <rect x="0" y="0" width="22" height="22" rx="4" fill="#161b22" stroke="#58a6ff" stroke-width="1.5"/>
                            </g>
                            <g transform="translate(35,0)">
                                <rect x="0" y="0" width="22" height="22" rx="4" fill="#161b22" stroke="#bc8cff" stroke-width="1.5"/>
                            </g>
                            <g transform="translate(70,0)">
                                <rect x="0" y="0" width="22" height="22" rx="4" fill="#161b22" stroke="#238636" stroke-width="1.5"/>
                            </g>
                            <g transform="translate(105,0)">
                                <rect x="0" y="0" width="22" height="22" rx="4" fill="#161b22" stroke="#e3b341" stroke-width="1.5"/>
                            </g>
                            <!-- Connection lines between blocks -->
                            <line x1="22" y1="11" x2="35" y2="11" stroke="#58a6ff" stroke-width="1.5"/>
                            <line x1="57" y1="11" x2="70" y2="11" stroke="#bc8cff" stroke-width="1.5"/>
                            <line x1="92" y1="11" x2="105" y2="11" stroke="#238636" stroke-width="1.5"/>
                        </g>

                        <!-- IDEA BULB (Interests) -->
                        <g transform="translate(420, 360)" class="animate-float" style="animation-delay: 1s;">
                            <circle cx="0" cy="0" r="22" fill="#0d1117" stroke="#e3b341" stroke-width="2" filter="url(#glow)"/>
                            <path d="M-6,-5 C-6,-12 6,-12 6,-5 C6,0 2,2 2,6 L-2,6 C-2,2 -6,0 -6,-5 Z" fill="none" stroke="#e3b341" stroke-width="2"/>
                            <line x1="-3" y1="10" x2="3" y2="10" stroke="#e3b341" stroke-width="2"/>
                        </g>

                    </svg>

                    <!-- Bottom interactive status pill -->
                    <div class="mt-4 flex items-center gap-2 bg-github-dark/80 px-4 py-1.5 rounded-full border border-github-border text-xs text-github-text">
                        <span class="w-2.5 h-2.5 rounded-full bg-emerald-500 animate-ping"></span>
                        <span>Interactive Visual Profile Ready for GitHub</span>
                    </div>
                </div>

            </div>
        </div>

        <!-- CODE TAB CONTENT (Instruction & Markdown Copy Snippets) -->
        <div id="tab-code" class="p-6 md:p-10 hidden space-y-8">
            
            <div class="bg-github-blue/10 border border-github-blue/30 rounded-lg p-4 text-sm text-github-text flex items-start gap-3">
                <i class="fa-solid fa-circle-info text-github-blue text-lg mt-0.5"></i>
                <div>
                    <h3 class="font-bold text-white mb-1">Sida aad ugu xerto GitHub Profile-kaaga (How to use on GitHub):</h3>
                    <p class="text-xs text-github-muted leading-relaxed">
                        GitHub README.md wuxuu taageeraa HTML table side-by-side ah. Dooro mid ka mid ah labada opshan ee hoose, kaddib taabo <strong>Copy Code</strong> oo ku paste-garee faaylkaaga <code>README.md</code>.
                    </p>
                </div>
            </div>

            <!-- OPTION 1: HTML Table Readme Layout -->
            <div class="space-y-3">
                <div class="flex justify-between items-center">
                    <h3 class="text-base font-bold text-white flex items-center gap-2">
                        <span class="bg-github-purple text-github-dark w-6 h-6 rounded-full inline-flex items-center justify-center text-xs">1</span>
                        Code-ka README.md (HTML Table Side-by-Side)
                    </h3>
                    <button onclick="copyToClipboard('code-option-1', 'btn-copy-1')" id="btn-copy-1" class="bg-github-accent hover:bg-emerald-600 text-white text-xs px-3 py-1.5 rounded-md font-medium transition flex items-center gap-1.5">
                        <i class="fa-regular fa-copy"></i> Copy Code
                    </button>
                </div>
                
                <pre class="bg-github-dark p-4 rounded-xl border border-github-border text-xs text-github-blue overflow-x-auto"><code id="code-option-1">&lt;table border="0"&gt;
  &lt;tr&gt;
    &lt;!-- SIFADA BIDIX: Qoraalka Profile-kaaga --&gt;
    &lt;td width="50%" valign="top"&gt;
      &lt;p&gt;Building modern, useful, and creative digital applications.&lt;/p&gt;
      
      &lt;h3&gt;🚀 What I Do&lt;/h3&gt;
      &lt;ul&gt;
        &lt;li&gt;💻 &lt;b&gt;Full-Stack Development&lt;/b&gt;&lt;/li&gt;
        &lt;li&gt;🎨 &lt;b&gt;UI/UX Design&lt;/b&gt;&lt;/li&gt;
        &lt;li&gt;📱 &lt;b&gt;Mobile App Development&lt;/b&gt;&lt;/li&gt;
        &lt;li&gt;🤖 &lt;b&gt;AI Engineering & Integration&lt;/b&gt;&lt;/li&gt;
        &lt;li&gt;🛡️ &lt;b&gt;Cybersecurity Exploration&lt;/b&gt;&lt;/li&gt;
        &lt;li&gt;🌱 &lt;b&gt;Continuous Learning & Building&lt;/b&gt;&lt;/li&gt;
      &lt;/ul&gt;

      &lt;p&gt;I enjoy transforming ideas into &lt;b&gt;real-world digital products&lt;/b&gt; and exploring new technologies.&lt;/p&gt;

      &lt;h3&gt;🎯 My Goal&lt;/h3&gt;
      &lt;blockquote&gt;
        To build innovative software that solves real problems and creates meaningful digital experiences.
      &lt;/blockquote&gt;

      &lt;h3&gt;💡 My Interests&lt;/h3&gt;
      &lt;ul&gt;
        &lt;li&gt;🌐 Modern Web Applications&lt;/li&gt;
        &lt;li&gt;📱 Mobile Applications&lt;/li&gt;
        &lt;li&gt;🤖 Artificial Intelligence&lt;/li&gt;
        &lt;li&gt;🔐 Cybersecurity&lt;/li&gt;
        &lt;li&gt;🎨 User Experience&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/td&gt;

    &lt;!-- SIFADA MIDIG: Sawirka Animation-ka ah --&gt;
    &lt;td width="50%" align="center" valign="middle"&gt;
      &lt;img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg" alt="Developer Animation Art" width="100%" /&gt;
      &lt;br/&gt;&lt;br/&gt;
      &lt;sub&gt;✨ Kobcinta Fikirkaaga Digital-ka ah | Empowering Your Digital Vision&lt;/sub&gt;
    &lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;</code></pre>
            </div>

            <!-- OPTION 2: Pure Markdown Alternative -->
            <div class="space-y-3">
                <div class="flex justify-between items-center">
                    <h3 class="text-base font-bold text-white flex items-center gap-2">
                        <span class="bg-github-blue text-github-dark w-6 h-6 rounded-full inline-flex items-center justify-center text-xs">2</span>
                        Markdown-ka Standard-ka ah (Pure Markdown)
                    </h3>
                    <button onclick="copyToClipboard('code-option-2', 'btn-copy-2')" id="btn-copy-2" class="bg-github-border hover:bg-github-muted/30 text-white text-xs px-3 py-1.5 rounded-md font-medium transition flex items-center gap-1.5">
                        <i class="fa-regular fa-copy"></i> Copy Code
                    </button>
                </div>

                <pre class="bg-github-dark p-4 rounded-xl border border-github-border text-xs text-github-purple overflow-x-auto"><code id="code-option-2">Building modern, useful, and creative digital applications.

### 🚀 What I Do
- 💻 **Full-Stack Development**
- 🎨 **UI/UX Design**
- 📱 **Mobile App Development**
- 🤖 **AI Engineering & Integration**
- 🛡️ **Cybersecurity Exploration**
- 🌱 **Continuous Learning & Building**

I enjoy transforming ideas into **real-world digital products** and exploring new technologies.

### 🎯 My Goal
> To build innovative software that solves real problems and creates meaningful digital experiences.

### 💡 My Interests
- 🌐 Modern Web Applications
- 📱 Mobile Applications
- 🤖 Artificial Intelligence
- 🔐 Cybersecurity
- 🎨 User Experience

---
*Kobcinta Fikirkaaga Digital-ka ah | Empowering Your Digital Vision*</code></pre>
            </div>

        </div>

    </main>

    <!-- Toast Notification for Copying -->
    <div id="toast" class="fixed bottom-6 right-6 bg-github-accent text-white px-4 py-2.5 rounded-lg shadow-xl text-sm font-medium flex items-center gap-2 transition-all transform translate-y-20 opacity-0 pointer-events-none">
        <i class="fa-solid fa-circle-check"></i>
        <span>Waa lagu guuleystay in lagu nuuxsado (Copied to Clipboard!)</span>
    </div>

    <script>
        // Tab switching logic
        function switchTab(tab) {
            const previewTab = document.getElementById('tab-preview');
            const codeTab = document.getElementById('tab-code');
            const btnPreview = document.getElementById('btn-preview');
            const btnCode = document.getElementById('btn-code');

            if (tab === 'preview') {
                previewTab.classList.remove('hidden');
                codeTab.classList.add('hidden');
                
                btnPreview.className = "px-4 py-2 rounded-md text-sm font-semibold transition-all bg-github-blue/20 text-github-blue border border-github-blue/30 flex items-center gap-2";
                btnCode.className = "px-4 py-2 rounded-md text-sm font-semibold transition-all text-github-muted hover:text-white flex items-center gap-2";
            } else {
                previewTab.classList.add('hidden');
                codeTab.classList.remove('hidden');

                btnCode.className = "px-4 py-2 rounded-md text-sm font-semibold transition-all bg-github-purple/20 text-github-purple border border-github-purple/30 flex items-center gap-2";
                btnPreview.className = "px-4 py-2 rounded-md text-sm font-semibold transition-all text-github-muted hover:text-white flex items-center gap-2";
            }
        }

        // Clipboard Copy function compatible with iFrame restrictions
        function copyToClipboard(elementId, btnId) {
            const codeElement = document.getElementById(elementId);
            const textToCopy = codeElement.innerText;

            // Create temporary textarea element to use execCommand
            const tempTextArea = document.createElement('textarea');
            tempTextArea.value = textToCopy;
            document.body.appendChild(tempTextArea);
            tempTextArea.select();
            
            try {
                document.execCommand('copy');
                showToast();
                
                // Visual feedback on button
                const btn = document.getElementById(btnId);
                const originalText = btn.innerHTML;
                btn.innerHTML = `<i class="fa-solid fa-check"></i> Copied!`;
                setTimeout(() => {
                    btn.innerHTML = originalText;
                }, 2000);
            } catch (err) {
                console.error('Failed to copy text: ', err);
            }
            
            document.body.removeChild(tempTextArea);
        }

        // Show Toast Function
        function showToast() {
            const toast = document.getElementById('toast');
            toast.classList.remove('translate-y-20', 'opacity-0', 'pointer-events-none');
            
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0', 'pointer-events-none');
            }, 3000);
        }
    </script>
</body>
</html>
