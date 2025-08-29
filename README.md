<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Skater Hub - Massive Gallery</title>
<script src="https://cdn.tailwindcss.com"></script>
<style>
  body {
    font-family: 'Arial', sans-serif;
    background: linear-gradient(to bottom, #1a1a1a, #111);
    color: #f0f0f0;
  }
  h1,h2,h3,h4 { font-family: 'Bangers', cursive; }
  .skater-card {
    min-width: 200px; /* fixed width for horizontal scrolling */
    flex-shrink: 0;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .skater-card:hover {
    transform: translateY(-5px) rotate(-1deg);
    box-shadow: 0 10px 20px rgba(0,255,0,0.3);
  }
</style>
</head>
<body class="text-gray-100">

<!-- Navbar -->
<nav class="bg-gray-800/90 backdrop-blur p-4 sticky top-0 z-50 flex justify-between items-center">
  <h1 class="text-3xl font-bold text-green-400">Skater Hub</h1>
</nav>

<!-- Hero -->
<header class="text-center py-12 bg-gray-900/80">
  <h2 class="text-5xl font-bold mb-4 text-green-400 drop-shadow-lg">Skater Mega Gallery</h2>
  <p class="text-gray-300 text-lg max-w-2xl mx-auto">Scroll through hundreds of skaters. Click to download your favorites!</p>
</header>

<!-- Horizontal Scroll Gallery -->
<section class="py-16 px-6">
  <h3 class="text-3xl font-bold text-green-400 mb-6 text-center">All Skaters</h3>
  <div class="flex space-x-4 overflow-x-auto scrollbar-hide px-4">

    <!-- JS will populate 500 boxes -->
    <div id="skaterContainer" class="flex space-x-4"></div>

  </div>
</section>

<script>
  const container = document.getElementById('skaterContainer');

  for(let i=1; i<=500; i++){
    const card = document.createElement('div');
    card.className = 'skater-card bg-gray-800 rounded-2xl overflow-hidden shadow-lg text-center p-4';
    card.innerHTML = `
      <div class="h-48 bg-gray-700 flex items-center justify-center text-gray-400 mb-4">Skater ${i}</div>
      <h4 class="text-xl font-bold mb-2 text-yellow-400">Skater ${i}</h4>
      <p class="text-gray-300 mb-4">Awesome tricks!</p>
      <a href="#" class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-xl transition inline-block">Download</a>
    `;
    container.appendChild(card);
  }
</script>

</body>
</html>

