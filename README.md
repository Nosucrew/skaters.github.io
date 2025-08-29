<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<title>Skater Downloads</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background: black;
    color: white;
  }

  h1 {
    text-align: center;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    gap: 10px;
    margin-top: 20px;
  }

  .box {
    position: relative;
    width: 120px;
    height: 160px;
    border-radius: 10px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 5px;
    cursor: pointer;
    animation: galaxy 12s infinite alternate;
  }

  .box img {
    width: 100%;
    height: 100px;
    object-fit: cover;
    border-radius: 5px;
  }

  .download-btn {
    background-color: rgba(255,255,255,0.8);
    border: none;
    border-radius: 5px;
    padding: 4px;
    font-size: 12px;
    cursor: pointer;
    text-align: center;
  }

  /* Galaxy animatie */
  @keyframes galaxy {
    0% { background: linear-gradient(135deg, #1e3c72, #2a5298); }
    50% { background: linear-gradient(135deg, #1e3c72, #00ffcc); }
    100% { background: linear-gradient(135deg, #1e3c72, #ff00ff); }
  }

  /* Sterretjes overlay */
  .stars {
    position: absolute;
    width: 100%;
    height: 100%;
    pointer-events: none;
    background-image: radial-gradient(white 1px, transparent 1px);
    background-size: 5px 5px;
    opacity: 0.5;
  }
</style>
</head>
<body>

<h1>Skater Files Download</h1>
<div class="grid" id="grid"></div>

<script>
const grid = document.getElementById('grid');
const totalBoxes = 500;

// Placeholder afbeelding, later vervangen door echte skater afbeeldingen
const skaterImage = 'https://via.placeholder.com/100x100.png?text=Skater';

for(let i=1; i<=totalBoxes; i++){
  const box = document.createElement('div');
  box.className = 'box';

  const stars = document.createElement('div');
  stars.className = 'stars';
  box.appendChild(stars);

  const img = document.createElement('img');
  img.src = skaterImage;
  img.alt = `Skater ${i}`;
  box.appendChild(img);

  const btn = document.createElement('button');
  btn.className = 'download-btn';
  btn.innerText = 'Download';
  btn.onclick = () => {
    alert(`Downloading Skater ${i} file...`);
  };
  box.appendChild(btn);

  grid.appendChild(box);
}
</script>

</body>
</html>
