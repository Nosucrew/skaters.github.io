<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Galaxy Skater Hub</title>
<script src="https://cdn.tailwindcss.com"></script>
<link href="https://fonts.googleapis.com/css2?family=Bangers&display=swap" rel="stylesheet">
<style>
  body {
    background: radial-gradient(circle at 50% 0%, #0d0d0d, #111 80%);
    color: #f0f0f0;
    font-family: Arial, sans-serif;
    overflow-x: hidden;
  }
  h1,h2,h3,h4 { font-family: 'Bangers', cursive; }
  .skater-card {
    min-width: 220px;
    flex-shrink: 0;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    border: 2px solid transparent;
  }
  .skater-card:hover {
    transform: translateY(-5px) rotate(-1deg);
    box-shadow: 0 10px 20px rgba(0,255,255,0.5);
    border-color: cyan;
  }
  .scrollbar-hide::-webkit-scrollbar { display: none; }
  .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }
</style>
</head>
<body class="text-gray-100">

<!-- Terms of Service Overlay -->
<div id="tosOverlay" class="fixed inset-0 bg-black/90 flex flex-col items-center justify-center z-50 px-4">
  <h2 class="text-4xl font-bold mb-6 text-green-400 drop-shadow-lg text-center">Welcome to Galaxy Skater Hub</h2>
  <p class="text-gray-300 max-w-lg text-center mb-6">
    Yo! Some skaters here might be wild or not suitable for everyone. We don’t condone anything inappropriate — but some things may exist anyway.
    Skate safe and have fun!
  </p>
  <button onclick="acceptTerms()" class="bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-xl shadow-lg transition">
    Okeeeeeeeee, I Accept
  </button>
</div>

<!-- Navbar -->
<nav class="bg-gray-900/90 backdrop-blur p-4 sticky top-0 z-40 flex justify-between items-center">
  <h1 class="text-3xl font-bold text-cyan-400">Galaxy Skater Hub</h1>
  <a href="#contact" class="bg-cyan-600 hover:bg-cyan-700 text-white px-4 py-2 rounded-xl transition">Contact</a>
</nav>

<!-- Hero -->
<header class="text-center py-12 bg-gray-900/70">
  <h2 class="text-5xl font-bold mb-4 text-cyan-400 drop-shadow-lg">Skate the Galaxy</h2>
  <p class="text-gray-300 text-lg max-w-2xl mx-auto">Scroll through 500 cosmic skaters. Click to download your favorites and hit the streets!</p>
</header>

<!-- Skater Gallery -->
<section class="py-16 px-6">
  <h3 class="text-4xl font-bold text-cyan-400 mb-6 text-center">All Skaters</h3>
  <div class="overflow-x-auto scrollbar-hide flex space-x-4 px-4">
    <div id="skaterContainer" class="flex space-x-4"></div>
  </div>
</section>

<!-- About -->
<section id="about" class="bg-gray-900/70 py-16 px-6 text-center">
  <h3 class="text-3xl font-bold mb-6 text-cyan-400">About Galaxy Skater Hub</h3>
  <p class="max-w-2xl mx-auto text-gray-300">
    Galaxy Skater Hub is the ultimate collection of cosmic skaters for your games. Hundreds of characters, all free to use. Skate fast, look cosmic!
  </p>
</section>

<!-- Contact -->
<section id="contact" class="container mx-auto px-6 py-16 text-center">
  <h3 class="text-3xl font-bold mb-6 text-cyan-400">Contact</h3>
  <p class="text-gray-300 mb-6">Questions, feedback, or cosmic suggestions? Hit me up!</p>
  <a href="mailto:youremail@example.com" class="bg-cyan-600 hover:bg-cyan-700 text-white px-6 py-3 rounded-xl transition">Email Me</a>
</section>

<!-- Footer -->
<footer class="bg-gray-900/80 text-center py-6 text-gray-400">
  <p>&copy; 2025 Galaxy Skater Hub. All rights reserved.</p>
</footer>

<script>
function acceptTerms() {
  document.getElementById('tosOverlay').style.display = 'none';
}

// Generate 500 skater cards dynamically
const container = document.getElementById('skaterContainer');
for(let i=1; i<=500; i++){
  const card = document.createElement('div');
  card.className = 'skater-card bg-gray-800 rounded-2xl shadow-lg text-center p-4';
  card.innerHTML = `
    <div class="h-48 bg-gradient-to-br from-purple-900 via-pink-800 to-blue-900 flex items-center justify-center text-gray-400 mb-4">
      Skater ${i}
    </div>
    <h4 class="text-xl font-bold mb-2 text-yellow-400">Skater ${i}</h4>
    <p class="text-gray-300 mb-4">Cosmic tricks!</p>
    <a href="#" class="bg-cyan-600 hover:bg-cyan-700 text-white px-4 py-2 rounded-xl transition inline-block">Download</a>
  `;
  container.appendChild(card);
}
</script>

</body>
</html>
