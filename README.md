<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Search AI | The Ultimate Directory</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap');
        body { font-family: 'Inter', sans-serif; background: #05070a; color: #ffffff; margin: 0; overflow-x: hidden; -webkit-tap-highlight-color: transparent; }
        
        @keyframes liquid { 0% { transform: translate(-5%, -5%) scale(1); } 50% { transform: translate(5%, 5%) scale(1.1); } 100% { transform: translate(-5%, -5%) scale(1); } }
        .liquid-bg { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(circle at 50% 50%, #1e3a8a 0%, #05070a 70%); z-index: -1; opacity: 0.6; animation: liquid 20s infinite alternate ease-in-out; }
        
        .glass-card { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(15px); border: 1px solid rgba(59, 130, 246, 0.2); transition: all 0.3s ease; }
        .glass-card:hover { border: 1px solid #60a5fa; background: rgba(30, 64, 175, 0.15); transform: translateY(-3px); }
        .blue-gradient-text { background: linear-gradient(90deg, #60a5fa, #93c5fd); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .tag { font-size: 9px; text-transform: uppercase; font-weight: bold; padding: 2px 8px; border-radius: 999px; background: rgba(59, 130, 246, 0.2); color: #93c5fd; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body>

    <div class="liquid-bg"></div>

    <nav class="sticky top-0 z-50 px-4 py-4 flex justify-between items-center border-b border-blue-500/20 bg-[#05070a]/80 backdrop-blur-md">
        <div class="text-xl font-extrabold tracking-tighter uppercase text-white">Search <span class="blue-gradient-text">AI</span></div>
    </nav>

    <header class="pt-8 pb-6 px-4 text-center">
        <h1 class="text-3xl font-extrabold text-white leading-tight">Find the AI you want.<br><span class="blue-gradient-text">The best way to find AI is to find Search AI.</span></h1>
    </header>

    <div class="flex overflow-x-auto gap-2 px-4 pb-6 no-scrollbar">
        <button onclick="filterTools('all')" class="filter-btn shrink-0 px-4 py-2 rounded-full bg-blue-600 text-white text-xs font-bold">All</button>
        <button onclick="filterTools('chat')" class="filter-btn shrink-0 px-4 py-2 rounded-full glass-card text-blue-100 text-xs font-medium">Chat</button>
        <button onclick="filterTools('code')" class="filter-btn shrink-0 px-4 py-2 rounded-full glass-card text-blue-100 text-xs font-medium">Code</button>
        <button onclick="filterTools('prod')" class="filter-btn shrink-0 px-4 py-2 rounded-full glass-card text-blue-100 text-xs font-medium">Prod</button>
        <button onclick="filterTools('art')" class="filter-btn shrink-0 px-4 py-2 rounded-full glass-card text-blue-100 text-xs font-medium">Art</button>
        <button onclick="filterTools('video')" class="filter-btn shrink-0 px-4 py-2 rounded-full glass-card text-blue-100 text-xs font-medium">Video</button>
        <button onclick="filterTools('music')" class="filter-btn shrink-0 px-4 py-2 rounded-full glass-card text-blue-100 text-xs font-medium">Music</button>
    </div>

    <section id="toolGrid" class="px-4 grid grid-cols-1 gap-4 pb-8">
        
        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="chat">
            <div class="w-12 h-12 bg-blue-600 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-star"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Gemini AI</h3><span class="tag">All Rounder</span><br><a href="https://gemini.google.com" class="text-blue-400 text-xs underline">gemini.google.com</a></div>
        </div>
        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="chat">
            <div class="w-12 h-12 bg-blue-500 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-message"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">ChatGPT</h3><span class="tag">Best Chat</span><br><a href="https://chat.openai.com" class="text-blue-400 text-xs underline">chat.openai.com</a></div>
        </div>
        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="chat">
            <div class="w-12 h-12 bg-orange-700 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-brain"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Claude AI</h3><span class="tag">Best Logic</span><br><a href="https://claude.ai" class="text-blue-400 text-xs underline">claude.ai</a></div>
        </div>
        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="chat">
            <div class="w-12 h-12 bg-blue-400 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-comments"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Copilot</h3><br><a href="https://copilot.microsoft.com" class="text-blue-400 text-xs underline">copilot.microsoft.com</a></div>
        </div>

        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="code">
            <div class="w-12 h-12 bg-indigo-600 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-terminal"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Replit AI</h3><span class="tag">Best IDE</span><br><a href="https://replit.com/ai" class="text-blue-400 text-xs underline">replit.com/ai</a></div>
        </div>
        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="code">
            <div class="w-12 h-12 bg-slate-600 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-code"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Cursor</h3><span class="tag">Best Code</span><br><a href="https://cursor.com" class="text-blue-400 text-xs underline">cursor.com</a></div>
        </div>

        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="prod">
            <div class="w-12 h-12 bg-emerald-500 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-calendar-check"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Reclaim AI</h3><a href="https://reclaim.ai" class="text-blue-400 text-xs underline">reclaim.ai</a></div>
        </div>
        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="prod">
            <div class="w-12 h-12 bg-amber-500 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-clock"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Motion</h3><a href="https://usemotion.com" class="text-blue-400 text-xs underline">usemotion.com</a></div>
        </div>

        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="art">
            <div class="w-12 h-12 bg-cyan-500 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-palette"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Midjourney</h3><span class="tag">Best Art</span><br><a href="https://midjourney.com" class="text-blue-400 text-xs underline">midjourney.com</a></div>
        </div>

        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="video">
            <div class="w-12 h-12 bg-red-600 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-film"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Sora</h3><br><a href="https://openai.com/sora" class="text-blue-400 text-xs underline">openai.com/sora</a></div>
        </div>
        
        <div class="tool-card glass-card p-5 rounded-2xl flex items-center gap-4" data-category="music">
            <div class="w-12 h-12 bg-pink-500 rounded-lg flex items-center justify-center text-white text-lg"><i class="fa-solid fa-music"></i></div>
            <div class="flex-grow"><h3 class="font-bold text-white">Suno</h3><br><a href="https://suno.com" class="text-blue-400 text-xs underline">suno.com</a></div>
        </div>
    </section>

    <footer class="text-center py-8 text-blue-500 text-xs uppercase tracking-widest">
        By Gemini and Harshith
    </footer>

    <script>
        function filterTools(category) {
            const cards = document.querySelectorAll('.tool-card');
            const buttons = document.querySelectorAll('.filter-btn');
            buttons.forEach(btn => { btn.classList.remove('bg-blue-600', 'text-white'); btn.classList.add('glass-card', 'text-blue-100'); });
            event.target.classList.add('bg-blue-600', 'text-white'); event.target.classList.remove('glass-card', 'text-blue-100');
            cards.forEach(card => { 
                card.style.display = (category === 'all' || card.getAttribute('data-category') === category) ? 'flex' : 'none'; 
            });
        }
    </script>
</body>
</html>

