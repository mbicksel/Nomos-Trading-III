# Nomos-Trading-III
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
        body { font-family: 'Inter', system_ui, sans-serif; }
        .heading-font { font-family: 'Space Grotesk', sans-serif; }
        .hero-bg { background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%); }
        .nav-link { position: relative; }
        .nav-link:after {
            content: ''; position: absolute; width: 0; height: 2px; bottom: -2px; left: 0;
            background: linear-gradient(to right, #00f5ff, #8a2be2); transition: width 0.3s;
        }
        .nav-link:hover:after { width: 100%; }
        .ticker { animation: ticker-slide 30s linear infinite; }
        @keyframes ticker-slide { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
    </style>
</head>
<body class="bg-black text-white">

<nav class="fixed top-0 left-0 right-0 z-50 bg-black/80 backdrop-blur-xl border-b border-white/10">
    <div class="max-w-screen-2xl mx-auto px-8 py-5 flex items-center justify-between">
        <div class="flex items-center gap-3">
            <div class="w-9 h-9 rounded-2xl bg-gradient-to-br from-cyan-400 to-violet-600 flex items-center justify-center text-2xl font-bold heading-font">N</div>
            <span class="heading-font text-3xl font-semibold tracking-tighter">NOMOS</span>
        </div>
        <div class="flex gap-8 text-sm">
            <a href="#" class="nav-link">STRATEGY</a>
            <a href="#" class="nav-link">RESEARCH</a>
            <a href="#" class="nav-link">LIVE SIGNALS</a>
        </div>
        <button onclick="alert('Demo Mode')" class="bg-white text-black px-6 py-2 rounded-3xl font-bold">ACCESS PLATFORM</button>
    </div>
</nav>

<section class="hero-bg min-h-screen flex items-center pt-20">
    <div class="max-w-screen-2xl mx-auto px-8 text-center">
        <h1 class="text-7xl font-bold heading-font tracking-tighter">NOMOS TRADING</h1>
        <p class="text-3xl mt-4 text-cyan-400">Regulatory Alpha Engine</p>
        <p class="mt-8 text-xl max-w-2xl mx-auto">We turn government rulings into trading profits.</p>
    </div>
</section>

<script>
    function fakeLogin() { alert("Welcome to Nomos Trading (Demo)"); }
</script>
</body>
</html>
