<!-- Terms of Service Overlay -->
<div id="tosOverlay" class="fixed inset-0 bg-black/90 flex flex-col items-center justify-center z-50 px-4">
  <h2 class="text-4xl font-bold mb-6 text-green-400 drop-shadow-lg text-center">Welcome to Skater Hub</h2>
  <p class="text-gray-300 max-w-lg text-center mb-6">
    Yo! Some skaters on this site might be wild or not suitable for everyone. We don’t condone anything inappropriate — but some things may exist anyway. 
    Skate safe and have fun!
  </p>
  <button onclick="acceptTerms()" class="bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-xl shadow-lg transition">
    Okeeeeeeeee, I Accept
  </button>
</div>

<script>
  function acceptTerms() {
    document.getElementById('tosOverlay').style.display = 'none';
  }
</script>
