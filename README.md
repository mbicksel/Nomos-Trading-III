<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nomos Trading | Regulatory Alpha</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap');
        
        :root { --primary: #00f5ff; }
        
        body { font-family: 'Inter', system_ui, sans-serif; }
        .heading-font { font-family: 'Space Grotesk', sans-serif; }

        .hero-bg {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(0, 245, 255, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(138, 43, 226, 0.15) 0%, transparent 50%);
        }

        .nav-link {
            position: relative;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background: linear-gradient(to right, #00f5ff, #8a2be2);
            transition: width 0.3s ease;
        }
        .nav-link:hover:after { width: 100%; }

        .glow-cyan {
            box-shadow: 0 0 25px -5px rgb(0 245 255 / 0.5),
                        0 0 10px -5px rgb(0 245 255 / 0.3);
        }

        .data-row { transition: all 0.2s ease; }
        .data-row:hover {
            background-color: #1f2937;
            transform: translateX(8px);
        }

        .ticker {
            animation: ticker-slide 30s linear infinite;
        }
        @keyframes ticker-slide {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
    </style>
</head>
<body class="bg-black text-white overflow-x-hidden">
    <!-- NAVBAR -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-black/80 backdrop-blur-xl border-b border-white/10">
        <div class="max-w-screen-2xl mx-auto px-8 py-5 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-9 h-9 rounded-2xl bg-gradient-to-br from-cyan-400 to-violet-600 flex items-center justify-center text-2xl font-bold heading-font">N</div>
                <div>
                    <span class="heading-font text-3xl font-semibold tracking-tighter">NOMOS</span>
                    <span class="text-xs tracking-[3px] text-cyan-400 font-mono block -mt-1">TRADING</span>
                </div>
            </div>
            
            <div class="flex items-center gap-10 text-sm font-medium">
                <a href="#" class="nav-link text-white/80 hover:text-white">STRATEGY</a>
                <a href="#" class="nav-link text-white/80 hover:text-white">RESEARCH</a>
                <a href="#" class="nav-link text-white/80 hover:text-white">LIVE SIGNALS</a>
                <a href="#" class="nav-link text-white/80 hover:text-white">PREDICTION MARKETS</a>
                <a href="#" class="nav-link text-white/80 hover:text-white">ABOUT</a>
            </div>

            <div class="flex items-center gap-4">
                <div class="px-6 py-2.5 bg-white/5 hover:bg-white/10 border border-white/20 rounded-2xl text-sm font-medium flex items-center gap-2 transition-all cursor-pointer">
                    <i class="fa-solid fa-bolt text-emerald-400"></i>
                    <span class="text-emerald-400 font-mono text-xs">LIVE</span>
                </div>
                <button onclick="fakeLogin()" 
                        class="px-8 py-3 bg-white text-black rounded-3xl font-semibold hover:bg-cyan-400 hover:text-black transition-all flex items-center gap-2">
                    <i class="fa-solid fa-arrow-right"></i>
                    <span>ACCESS PLATFORM</span>
                </button>
            </div>
        </div>
    </nav>

    <!-- HERO + all other sections (same as before) -->
    <section class="hero-bg min-h-screen flex items-center pt-20">
        <div class="max-w-screen-2xl mx-auto px-8 grid grid-cols-2 gap-16 items-center">
            <div class="space-y-8">
                <div class="inline-flex items-center gap-3 bg-white/5 border border-white/10 rounded-3xl px-6 py-2 text-sm">
                    <div class="w-2 h-2 bg-emerald-400 rounded-full animate-pulse"></div>
                    <span class="font-mono tracking-widest text-emerald-400">REGULATORY ALPHA ENGINE v2.4</span>
                </div>
                
                <h1 class="heading-font text-7xl leading-none font-semibold tracking-tighter">
                    DECODE THE<br>ADMINISTRATIVE<br>STATE.<br>
                    <span class="bg-gradient-to-r from-cyan-400 via-violet-400 to-fuchsia-400 bg-clip-text text-transparent">TRADE THE IMPACT.</span>
                </h1>
                
                <p class="text-2xl text-white/70 max-w-lg">
                    Nomos Trading turns regulatory rulings into quantifiable edge. 
                    We model administrative decisions and execute across equities &amp; prediction markets.
                </p>
                
                <div class="flex items-center gap-6">
                    <button onclick="document.getElementById('performance').scrollIntoView({ behavior: 'smooth' })" 
                            class="px-10 py-5 bg-gradient-to-r from-cyan-400 to-violet-600 rounded-3xl font-semibold text-lg flex items-center gap-3 hover:scale-105 transition-transform">
                        <i class="fa-solid fa-chart-line"></i>
                        VIEW LIVE PERFORMANCE
                    </button>
                    
                    <button onclick="alert('Connecting to Nomos Terminal... (Demo)')"
                            class="px-10 py-5 border border-white/30 hover:border-white/60 rounded-3xl font-medium text-lg flex items-center gap-3 transition-all">
                        <i class="fa-solid fa-terminal"></i>
                        LAUNCH TERMINAL
                    </button>
                </div>
                
                <div class="flex items-center gap-12 pt-8 border-t border-white/10">
                    <div>
                        <div class="text-emerald-400 text-4xl font-mono font-semibold">+41.8%</div>
                        <div class="text-sm text-white/60">YTD NET</div>
                    </div>
                    <div>
                        <div class="text-4xl font-mono font-semibold">2.8s</div>
                        <div class="text-sm text-white/60">AVG. EXECUTION</div>
                    </div>
                    <div>
                        <div class="text-4xl font-mono font-semibold">87</div>
                        <div class="text-sm text-white/60">RULINGS MODELED</div>
                    </div>
                </div>
            </div>
            
            <div class="relative">
                <div class="bg-zinc-950/70 border border-cyan-400/30 rounded-3xl p-8 backdrop-blur-xl glow-cyan">
                    <div class="flex justify-between items-center mb-6">
                        <div class="flex items-center gap-3">
                            <i class="fa-solid fa-gavel text-amber-400"></i>
                            <div>
                                <div class="font-medium">EPA v. Industry</div>
                                <div class="text-xs text-white/50 font-mono">LIVE RULING FEED</div>
                            </div>
                        </div>
                        <div class="text-right">
                            <div class="text-emerald-400 text-sm font-medium">+2.4% expected move</div>
                            <div class="text-xs text-white/50">Probability: 78%</div>
                        </div>
                    </div>
                    
                    <div class="h-80 bg-black rounded-2xl relative overflow-hidden border border-white/10 flex items-end p-6">
                        <div class="absolute inset-0 flex items-end justify-around gap-1 px-8">
                            <div class="bg-gradient-to-t from-cyan-400 to-transparent w-8 rounded-t" style="height: 35%"></div>
                            <div class="bg-gradient-to-t from-cyan-400 to-transparent w-8 rounded-t" style="height: 52%"></div>
                            <div class="bg-gradient-to-t from-emerald-400 to-transparent w-8 rounded-t" style="height: 68%"></div>
                            <div class="bg-gradient-to-t from-emerald-400 to-transparent w-8 rounded-t" style="height: 91%"></div>
                            <div class="bg-gradient-to-t from-violet-400 to-transparent w-8 rounded-t" style="height: 77%"></div>
                        </div>
                        <div class="absolute inset-x-0 bottom-0 h-px bg-gradient-to-r from-transparent via-cyan-400 to-transparent"></div>
                        
                        <div class="absolute top-8 left-8 bg-black/80 px-4 py-2 rounded-2xl border border-cyan-400/50 text-xs font-mono">
                            IMPACT MODEL<br>
                            <span class="text-cyan-400">REG-DELTA: +0.034</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- (The rest of the page - ticker, thesis, performance, footer - is identical to the previous version) -->
    <!-- For brevity I omitted repeating every section here, but use the full code from my previous response or let me know if you need the complete file again. -->

    <script>
        function fakeLogin() {
            alert("Connecting to Nomos Secure Terminal...\n\nWelcome, Quant. (Demo)");
        }
    </script>
</body>
</html>
