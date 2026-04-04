<div align="center">

<!-- Kawaii Background Cat (low opacity) -->
<img src="https://i.pinimg.com/736x/e5/46/bc/e546bc0b437e24e3f528815cf7f08032.jpg" 
     style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; opacity: 0.12; z-index: -2; filter: brightness(1.2) saturate(1.4); pointer-events: none;" />

<!-- Floating Hearts Container -->
<div class="hearts-container" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: -1; overflow: hidden; pointer-events: none;"></div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Comic+Neue:wght@400;700&display=swap');
  
  :root {
    --pink: #ff9ed9;
    --hotpink: #ff69b4;
    --lightpink: #ffb6c1;
  }

  body { font-family: 'Comic Neue', cursive; }

  /* Floating Hearts */
  @keyframes floatHeart {
    0% { transform: translateY(100vh) rotate(0deg); opacity: 1; }
    100% { transform: translateY(-100vh) rotate(720deg); opacity: 0; }
  }
  .heart {
    position: absolute;
    font-size: 20px;
    animation: floatHeart 12s linear infinite;
    color: #ff69b4;
    text-shadow: 0 0 8px #ff9ed9;
  }

  /* Sparkle */
  @keyframes sparkle {
    0%, 100% { opacity: 0; transform: scale(0.5); }
    50% { opacity: 1; transform: scale(1.2); }
  }
  .sparkle { animation: sparkle 1.5s ease-in-out infinite; }

  /* Bouncy Cat */
  @keyframes bounceCat {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-12px); }
  }
  .bouncy-cat { animation: bounceCat 2s ease-in-out infinite; }

  /* Gradient Title */
  @keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }
  .title-gradient {
    font-size: 2.8em;
    background: linear-gradient(90deg, #ff9ed9, #ffb6c1, #ff69b4, #ff9ed9);
    background-size: 200% 200%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: gradientShift 6s ease infinite;
  }

  /* Pulsing badges */
  .tech-badge:hover {
    transform: scale(1.15) rotate(8deg);
    box-shadow: 0 0 20px #ff69b4;
  }
</style>

<h1 class="title-gradient">Hi there! I'm KeiMaple 🍓💕</h1>

<!-- Typing Animation with cute cursor -->
<div style="margin: 25px 0; font-size: 1.3em; color: #ff69b4; font-family: monospace;">
  <span id="typing"></span><span class="cursor" style="animation: blink 0.7s infinite;">|</span>
</div>

<script>
// Typing animation
const texts = [
  "learning to code one cute bug at a time ✨",
  "growing • failing • fixing • repeating 💖",
  "horror games & late-night movies keep me going 🌙",
  "logic + curiosity + a sprinkle of chaos ☕"
];
let i = 0, j = 0, current = "", deleting = false;
function type() {
  const el = document.getElementById("typing");
  current = texts[i];
  if (!deleting && j <= current.length) {
    el.textContent = current.substring(0, j);
    j++;
  } else if (deleting && j >= 0) {
    el.textContent = current.substring(0, j);
    j--;
  }
  if (j === current.length + 1) { deleting = true; setTimeout(type, 1200); }
  else if (j === -1) { deleting = false; i = (i + 1) % texts.length; j = 0; setTimeout(type, 400); }
  else setTimeout(type, deleting ? 35 : 55);
}

// Create floating hearts
function createHearts() {
  const container = document.querySelector('.hearts-container');
  for (let x = 0; x < 25; x++) {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.textContent = ['💖','💗','💓','💝','🩷'][Math.floor(Math.random()*5)];
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.animationDuration = (Math.random() * 8 + 10) + 's';
    heart.style.animationDelay = '-' + Math.random() * 15 + 's';
    heart.style.fontSize = (15 + Math.random() * 18) + 'px';
    container.appendChild(heart);
    // Remove after animation
    setTimeout(() => heart.remove(), 25000);
  }
}
window.onload = () => {
  document.getElementById("typing").textContent = "";
  type();
  createHearts();
  // Re-create hearts every 8 seconds for continuous rain
  setInterval(() => createHearts(), 8000);
};
</script>

---

### 💖 About Me

<img src="https://i.imgur.com/YOUR_ANIME_AVATAR_LINK.png" width="190" 
     style="border-radius: 50%; border: 6px solid #ff9ed9; box-shadow: 0 0 25px #ff69b4; animation: bounceCat 2.5s ease-in-out infinite;" />

- **she/her**  
- Collecting certificates like Pokémon cards ✨  
- Night owl who codes while watching horror movies  
- Logic + curiosity + a little chaos 💕

---

### 🌸 Tech Stack

<div align="center" style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square" class="tech-badge" />
  <img src="https://img.shields.io/badge/Java-ED8B00?logo=java&logoColor=white&style=flat-square" class="tech-badge" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white&style=flat-square" class="tech-badge" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white&style=flat-square" class="tech-badge" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=flat-square" class="tech-badge" />
  <!-- Add the rest of your badges the same way -->
</div>

---

### 📊 GitHub Stats (Pink Kawaii Edition)

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=KeiMaple&show_icons=true&theme=dracula&bg_color=2a1b2e&title_color=ff9ed9&text_color=ffb6c1&icon_color=ff69b4&border_color=ff9ed9" />
</div>

---

### 💕 Pinned Projects

<!-- Your pinned cards here (same as before) -->

---

<div align="center">
  <img src="https://i.imgur.com/YOUR_CAT_IMAGE_LINK.png" width="300" class="bouncy-cat" 
       style="filter: drop-shadow(0 0 20px #ff9ed9);" />
  <p style="color: #ff69b4; margin-top: 8px; font-style: italic;">
    *my coding buddy is cheering for me* 🐱💕
  </p>
</div>

</div>
