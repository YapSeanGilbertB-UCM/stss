<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Life Below Water</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" />
<link rel="stylesheet" href="styless.css" />
</head>
<body>

<!-- BACKGROUND -->
<div id="background">
  <canvas id="wavesCanvas"></canvas>
  <div class="wave" style="top: 0;"></div>
  <div class="wave" style="top: 50px; opacity: 0.05;"></div>
</div>

<!-- NAVIGATION -->
<nav>
  <div class="logo">LIFE BELOW WATER</div>
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#intro">Introduction</a></li>
    <li><a href="#explore">Explore</a></li>
    <li><a href="#oceanproblem">Ocean Problem/Solution</a></li>
    <li><a href="#about">About Us</a></li>
    <li><a href="#contact">Contact Us</a></li>
    <li><a href="#guessGame">Game</a></li>
    
  
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <h1>Life Below Water</h1>
  <p>Life below water is a wonderful world hidden under the waves...</p>
  <button class="cta-btn" onclick="document.getElementById('explore').scrollIntoView({behavior:'smooth'})">
    Explore Oceans
  </button>
</section>

<!-- INTRODUCTION -->
<section id="intro">
  <div class="section-wrapper">
    <div class="img-wrapper">
      <img src="life_underwater.jpg" />
      <div class="img-caption"></div>
    </div>
    <div class="text-wrapper">
      <h2>🌊 Introduction to Life Below Water</h2>
      <p>Life below water is the world of oceans, seas, and all the creatures that live in them. Many animals, from tiny plankton to large whales, depend on clean and healthy water to survive. Protecting life below water helps keep our planet balanced and full of life.</p>
    </div>
  </div>
</section>

<!-- EXPLORE -->
<section id="explore">
  <div class="section-wrapper">
    <div class="text-wrapper">
      <h2>🧭 Exploring the Ocean</h2>
      <p>People explore the ocean in many exciting ways, such as scuba diving to see sea animals up close and using submarines to visit deep underwater places. Divers also use special cameras to record the beauty of marine life. Scientists map the ocean floor to discover its shape and better understand what lies beneath the waves.</p>
    </div>

    <div class="explore-grid">
      <div class="explore-item">
        <img src="yapps.jpg" alt="Scuba Diving">
        <div class="caption">Scuba Diving</div>
      </div>
      <div class="explore-item">
        <img src="submarine.jpg" alt="Submarine Exploration">
        <div class="caption">Exploring Deep Ocean with Submarines</div>
      </div>
      <div class="explore-item">
        <img src="camera.jpg" alt="Underwater Camera">
        <div class="caption">Recording Sea Life with Cameras</div>
      </div>
      <div class="explore-item">
        <img src="MAPING.jpg" alt="Ocean Mapping">
        <div class="caption">Mapping the Ocean Floor</div>
      </div>
    </div>
  </div>
</section>
<!-- OCEAN PROBLEMS SLIDER -->
<section id="problems-slider">
  <section id="oceanproblem">
  <h2 class="slider-title">🌏 Ocean Problems</h2>

  <div class="slider-container">
    <div class="slide active">
      <img src="trash.jpg" alt="Pollution">
      <h3>🗑️ Plastic Pollution</h3>
      <p>Millions of tons of plastic end up in the ocean every year, harming fish, turtles, and other sea animals.</p>
    </div>

    <div class="slide">
      <img src="overfishing.webp" alt="Overfishing">
      <h3>🎣 Overfishing</h3>
      <p>Overfishing removes too many fish from the ocean, making it hard for species to recover and survive.</p>
    </div>

    <div class="slide">
      <img src="coral_bleaching.jpg" alt="Coral Bleaching">
      <h3>🌡️ Coral Bleaching</h3>
      <p>Rising ocean temperatures cause coral to lose their color and die, destroying homes for many sea creatures.</p>
    </div>
  </div>
</section>
  <div class="slider-buttons">
    <button id="prevSlide">⟵</button>
    <button id="nextSlide">⟶</button>
  </div>
</section>
<script>
let currentSlide = 0;
const slides = document.querySelectorAll("#problems-slider .slide");
const nextBtn = document.getElementById("nextSlide");
const prevBtn = document.getElementById("prevSlide");

function showSlide(index) {
  slides.forEach(slide => slide.classList.remove("active"));
  slides[index].classList.add("active");
}

nextBtn.onclick = () => {
  currentSlide = (currentSlide + 1) % slides.length;
  showSlide(currentSlide);
};

prevBtn.onclick = () => {
  currentSlide = (currentSlide - 1 + slides.length) % slides.length;
  showSlide(currentSlide);
};

// Auto-slide
setInterval(() => {
  currentSlide = (currentSlide + 1) % slides.length;
  showSlide(currentSlide);
}, 6000);
</script>
<!-- OCEAN SOLUTIONS SLIDER -->
<section id="solutions-slider">
  <h2 class="slider-title">💡 Ocean Solutions</h2>

  <div class="slider-container">
    <div class="solution-slide active">
      <img src="clean_beach.jpg" alt="Beach Clean-up">
      <h3>🏖️ Beach Clean-ups</h3>
      <p>Organizing beach clean-ups helps remove plastic and debris before they reach the ocean, protecting marine life.</p>
    </div>

    <div class="solution-slide">
      <img src="sustainable_fishing.webp" alt="Sustainable Fishing">
      <h3>🎣 Sustainable Fishing</h3>
      <p>Using sustainable fishing practices ensures fish populations stay healthy and ecosystems remain balanced.</p>
    </div>

    <div class="solution-slide">
      <img src="coral_reef_planting.avif" alt="Coral Restoration">
      <h3>🌱 Coral Restoration</h3>
      <p>Planting new corals and protecting reefs help restore habitats for countless marine species.</p>
    </div>
  </div>

  <div class="slider-buttons">
    <button id="prevSolution">⟵</button>
    <button id="nextSolution">⟶</button>
  
  </div>
</section>
<script>
let currentSolution = 0;
const solutions = document.querySelectorAll("#solutions-slider .solution-slide");
const nextSolBtn = document.getElementById("nextSolution");
const prevSolBtn = document.getElementById("prevSolution");

function showSolution(index) {
  solutions.forEach(slide => slide.classList.remove("active"));
  solutions[index].classList.add("active");
}

nextSolBtn.onclick = () => {
  currentSolution = (currentSolution + 1) % solutions.length;
  showSolution(currentSolution);
};

prevSolBtn.onclick = () => {
  currentSolution = (currentSolution - 1 + solutions.length) % solutions.length;
  showSolution(currentSolution);
};

// Auto-slide every 6 seconds
setInterval(() => {
  currentSolution = (currentSolution + 1) % solutions.length;
  showSolution(currentSolution);
}, 6000);
</script>

<!-- ABOUT US -->
<section id="about">
  <h1 class="about-title">Our Ocean Guardians</h1>
  <p class="about-desc">We are a team united by passion for the ocean...</p>

  <div class="about-grid">
    <div class="member-card">
      <img src="seanss.jpg" alt="Sean Gilbert B. Yap">
      <h3>Sean Gilbert B. Yap</h3>
      <span>Researcher / Designer</span>
    </div>

    <div class="member-card">
      <img src="steve.jpg" alt="Steve Rafael Briones">
      <h3>Steve Rafael Briones</h3>
      <span>Research Assistant</span>
    </div>

    <div class="member-card">
      <img src="koys.jpg" alt="John Charlie Baclaan">
      <h3>John Charlie Baclaan</h3>
      <span>Field Explorer</span>
    </div>

    <!-- New member card added -->
    <div class="member-card">
      <img src="newmember.jpg" alt="Maria Lopez">
      <h3>Ervic Jay Omiping</h3>
      <span>Marine Biologist</span>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <h2>📬 Contact Us</h2>
  <form>
    <input type="text" placeholder="Your Name" required />
    <input type="email" placeholder="Your Email" required />
    <textarea rows="5" placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
  </form>
</section>


<!-- GUESS THE MARINE ANIMAL GAME -->
<section id="guessGame" class="game-section">
  <h2>🐠 Guess the Marine Animal</h2>
  <p>Can you identify the animal from its silhouette?</p>

  <div class="guess-wrapper">
    <div class="silhouette-container">
      <img id="animalSilhouette" class="silhouette" src="silhouette1.jpg">
    </div>

    <div id="answerButtons" class="answer-buttons"></div>

    <p id="guessResult"></p>

    <div id="animalInfo" class="animal-info"></div>

    <button id="nextAnimalBtn" class="next-btn" style="display:none;">Next Animal</button>
  </div>
</section>

<!-- BACK TO TOP -->
<div id="backTop" onclick="document.getElementById('home').scrollIntoView({behavior:'smooth'})">↑ Top</div>

<!-- CANVAS FOR FISH AND BUBBLES -->
<canvas id="fishCanvas"></canvas>

<!-- ------------------- JS ------------------- -->
<script>
const canvas = document.getElementById("fishCanvas");
const ctx = canvas.getContext("2d");
let w = (canvas.width = window.innerWidth);
let h = (canvas.height = window.innerHeight);
window.addEventListener("resize", () => { w = canvas.width = window.innerWidth; h = canvas.height = window.innerHeight; });

let particles = [];
for (let i=0;i<80;i++){
  particles.push({ x: Math.random()*w, y: Math.random()*h, radius: Math.random()*4+1, speed: Math.random()*1+0.5, opacity: Math.random()*0.5+0.3 });
}

class Fish {
  constructor(){ this.x=Math.random()*w; this.y=Math.random()*h; this.speed=1+Math.random()*1.5; this.flip=Math.random()>0.5?1:-1; this.size=50+Math.random()*60; this.angle=0; this.wave=Math.random()*0.03+0.01; }
  move(){ this.x+=this.speed*this.flip; this.y+=Math.sin(this.angle)*2; this.angle+=this.wave; if(this.x>w+150)this.x=-150; if(this.x<-150)this.x=w+150; }
  draw(){ ctx.save(); ctx.translate(this.x,this.y); ctx.rotate(Math.sin(this.angle)*0.2); ctx.scale(this.flip,1); ctx.fillStyle="#00e6ff"; ctx.fillRect(-this.size/2,-this.size/4,this.size,this.size/2); ctx.restore(); }
}
let fishArray=[]; for(let i=0;i<12;i++)fishArray.push(new Fish());

function animate(){
  ctx.clearRect(0,0,w,h);
  particles.forEach(p=>{ ctx.beginPath(); ctx.arc(p.x,p.y,p.radius,0,Math.PI*2); ctx.fillStyle=`rgba(255,255,255,${p.opacity})`; ctx.fill(); p.y-=p.speed; if(p.y<-10)p.y=h+10; });
  fishArray.forEach(f=>{f.move();f.draw();});
  requestAnimationFrame(animate);
}
animate();

const sections = document.querySelectorAll("section");
const backTop = document.getElementById("backTop");
function revealOnScroll(){ const triggerBottom=window.innerHeight*0.85; sections.forEach(section=>{ const top=section.getBoundingClientRect().top; if(top<triggerBottom) section.classList.add("reveal"); }); backTop.style.display=window.scrollY>400?"block":"none"; }
window.addEventListener("scroll", revealOnScroll);
window.addEventListener("load", revealOnScroll);

document.querySelectorAll("img").forEach(img => {
  img.addEventListener("mousemove",(e)=>{ const rect=img.getBoundingClientRect(); const x=e.clientX-rect.left; const y=e.clientY-rect.top; const rotateX=((y-rect.height/2)/20)*-1; const rotateY=(x-rect.width/2)/20; img.style.transform=`scale(1.08) rotateX(${rotateX}deg) rotateY(${rotateY}deg)`; });
  img.addEventListener("mouseleave",()=>{ img.style.transform="scale(1) rotateX(0deg) rotateY(0deg)"; });
});

// ---------------- GUESS THE MARINE ANIMAL GAME ----------------
const animalData = [
  {
    silhouette: "silhouette5.jpg",
    real: "dolphin.jpg",
    name: "Dolphin",
    fact: "Dolphins use echolocation to navigate and hunt underwater!",
    choices: ["Shark", "Seal", "Dolphin"]
  },
  {
    silhouette: "silhouette4.jpg",
    real: "turtle.jpg",
    name: "Turtle",
    fact: "Sea turtles can live up to 100 years!",
    choices: ["Clam", "Prawn", "Turtle"]
  },
  {
    silhouette: "silhouette3.jpg",
    real: "shark.jpg",
    name: "Shark",
    fact: "Sharks have been around for over 400 million years!",
    choices: ["Shark", "Dolphin", "Seal"]
  },
  {
    silhouette: "silhouette2.jpg",
    real: "seal.jpg",
    name: "Seal",
    fact: "Seals have sensitive whiskers to detect prey in the water.",
    choices: ["Seal", "Penguin", "Dolphin"]
  },
  {
    silhouette: "silhouette1.jpg",
    real: "seahorse.jpg",
    name: "Seahorse",
    fact: "Male seahorses carry and give birth to the babies!",
    choices: ["Seahorse", "Prawn", "Star Fish"]
  }
];

let current = 0;

function loadAnimal() {
  const data = animalData[current];
  const img = document.getElementById("animalSilhouette");

  img.src = data.silhouette;
  img.classList.remove("reveal");

  document.getElementById("guessResult").textContent = "";
  document.getElementById("animalInfo").textContent = "";
  document.getElementById("nextAnimalBtn").style.display = "none";

  const btns = document.getElementById("answerButtons");
  btns.innerHTML = "";

  data.choices.forEach(choice => {
    const btn = document.createElement("button");
    btn.textContent = choice;
    btn.onclick = () => checkAnswer(choice);
    btns.appendChild(btn);
  });
}

function checkAnswer(choice) {
  const data = animalData[current];
  const result = document.getElementById("guessResult");
  const img = document.getElementById("animalSilhouette");

  if (choice === data.name) {
    img.src = data.real;
    img.classList.add("reveal");

    result.textContent = "Correct! 🎉";
    result.style.color = "lightgreen";

    document.getElementById("animalInfo").innerHTML =
      `<strong>${data.name}</strong><br>${data.fact}`;

    document.getElementById("nextAnimalBtn").style.display = "inline-block";
  } else {
    result.textContent = "Incorrect! Try Again!";
    result.style.color = "red";
  }
}

document.getElementById("nextAnimalBtn").onclick = () => {
  current = (current + 1) % animalData.length;
  loadAnimal();
};

loadAnimal();

</script>

</body>
</html>


ody {
  margin: 0;
  font-family: "Poppins", sans-serif;
  overflow-x: hidden;
  background: #001f2b;
  color: #a6f6ff;
  scroll-behavior: smooth;
}
h1, h2, h3 { margin: 0; }
p, li { line-height: 1.7; }
a { text-decoration: none; color: inherit; }

/* FIXED NAVIGATION (ALWAYS ON TOP) */
nav {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999999;   /* SUPER HIGH TO STAY ABOVE EVERYTHING */
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px 50px;
  background: rgba(0, 0, 0, 0.45); /* Slightly stronger so it’s visible */
  backdrop-filter: blur(10px);
  gap: 50px;
}
#home, .hero {
  padding-top: 120px;
}
nav .logo { font-size: 28px; font-weight: 700; }
nav ul { list-style: none; display: flex; gap: 25px; }
nav ul li a:hover { color: #00e6ff; }

/* Play Game button in nav */
.nav-btn {
  background: none;        
  color: inherit;          
  border: none;           
  font-weight: 700;
  cursor: pointer;
  transition: color 0.3s, transform 0.3s;
  padding: 0;              
}

.nav-btn:hover {
  color: #00e6ff;         
  transform: scale(1.05);  
}

/* RESPONSIVE */
@media (max-width: 800px){
  .nav-btn {
    margin-top: 10px;
  }
}

/* BACKGROUND */
#background {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  z-index: -10;
  background: linear-gradient(to bottom, #004466 0%, #001f2b 100%);
}
.wave {
  position: absolute;
  width: 200%;
  height: 100%;
 
  opacity: 0.08;
  animation: waveMove 12s linear infinite;
}

@keyframes waveMove {
  0% {transform: translateX(0);}
  100% {transform: translateX(-50%);}
}

/* HERO */
.hero {
  height: 100vh;
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  text-align:center;
  padding:50px;
}

.hero h1 {font-size:64px;}
.hero p {max-width:700px;}

.cta-btn {
  margin-top:30px;
  padding:15px 30px;
  background:#00e6ff;
  color:#001f2b;
  border-radius:8px;
  border:none;
  font-weight:700;
  cursor:pointer;
}

/* SECTIONS */
section {
  padding:120px 50px;
  max-width:1200px;
  margin:auto;
  opacity:0;
  transform:translateY(60px);
  transition:1s ease;
}
section.reveal {
  opacity:1;
  transform:translateY(0);
}

.section-wrapper {
  display:flex;
  flex-wrap:wrap;
  gap:40px;
  justify-content:center;
  align-items:center;
}

.img-wrapper, .text-wrapper {
  flex:1;
  max-width:600px;
  text-align:center;
}

img {
  width:100%;
  border-radius:12px;
  box-shadow: 0 0 30px rgba(0,0,0,0.5);
}

.img-caption {
  margin-top:10px;
}

/* ABOUT */
#about {
  text-align:center;
}

.about-title {
  font-size:45px;
  background: linear-gradient(to right,#00e6ff,#00ffcc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

.about-desc {
  max-width:800px;
  margin:20px auto 60px;
}

.about-grid {
  display:grid;
  grid-template-columns: repeat(auto-fit,minmax(230px,1fr));
  gap:40px;
}

.member-card {
  background: rgba(255,255,255,0.05);
  padding:20px;
  border-radius:20px;
  transition:0.3s;
}
.member-card:hover {
  transform: translateY(-10px);
}
.member-card img {
  height:260px;
  object-fit:cover;
  border-radius:15px;
.member-card {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(15px);
  border-radius: 20px;
  padding: 20px;
  transition: 0.4s ease;
  box-shadow: 0 0 20px rgba(0,0,0,0.7);
}

.member-card:hover {
  transform: translateY(-12px) scale(1.05);
  box-shadow: 0 0 30px #00e6ff;
}

.member-card img {
  width:100%;
  height:260px;
  object-fit:cover;
  border-radius:15px;
}

.member-card h3 {
  margin-top:15px;
  color:#00e6ff;
}

.member-card span {
  opacity:0.8;
  font-size:14px;
}

}


/* CONTACT */
form {
  max-width:500px;
  margin:auto;
  display:flex;
  flex-direction:column;
  gap:15px;
}
form input, form textarea {
  padding:12px;
  border-radius:8px;
  border:none;
}



/* BACK TO TOP */
#backTop {
  position:fixed;
  bottom:30px;
  right:30px;
  background:#00e6ff;
  padding:12px 18px;
  border-radius:50px;
  cursor:pointer;
  display:none;
}

/* RESPONSIVE */
@media (max-width:800px){
  nav { flex-direction: column; }
  .hero h1 {font-size:38px;}
}
.hero {
  position: relative;
  height: 100vh;
  overflow: hidden;
  color: white;
}

.hero-video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 0;
}

.hero-content {
  position: relative;
  z-index: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  text-align: center;
  padding: 0 20px;
  background: rgba(0, 0, 0, 0.4);
}
/* ABOUT — PRO HOVER EFFECT */
.member-card {
  position: relative;
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(15px);
  border-radius: 20px;
  padding: 20px;
  overflow: hidden;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  box-shadow: 0 0 15px rgba(0,0,0,0.5);
}

/* Shine effect element */
.member-card::after {
  content: "";
  position: absolute;
  top: -100%;
  left: -100%;
  width: 250%;
  height: 250%;
  background: linear-gradient(
    120deg,
    transparent 0%,
    rgba(255,255,255,0.2) 50%,
    transparent 100%
  );
  transform: rotate(25deg);
  opacity: 0;
  transition: 0.6s ease;
}

.member-card:hover::after {
  top: -30%;
  left: -30%;
  opacity: 1;
}

/* Hover transformation */
.member-card:hover {
  transform: translateY(-12px) scale(1.07);
  box-shadow: 0 0 35px #00e6ff;
}

/* Image style */
.member-card img {
  width:100%;
  height:260px;
  object-fit:cover;
  border-radius:15px;
  transition: transform 0.5s ease;
}

/* Image animation on hover */
.member-card:hover img {
  transform: scale(1.12);
}
/* 🌊 UNIVERSAL PRO HOVER IMAGE EFFECT */
img {
  border-radius: 12px;
  transition: transform 0.5s ease, box-shadow 0.5s ease;
  position: relative;
  z-index: 1;
}

/* Shine Layer */
img::after {
  content: "";
  position: absolute;
  top: -100%;
  left: -100%;
  width: 250%;
  height: 250%;
  background: linear-gradient(
    120deg,
    transparent 0%,
    rgba(255,255,255,0.25) 50%,
    transparent 100%
  );
  transform: rotate(25deg);
  opacity: 0;
  transition: 0.6s ease;
}

/* Hover Glow + Zoom + Shine */
img:hover {
  transform: scale(1.12);
  box-shadow: 0 0 25px #00e6ff;
}

/* Shine Sweep Motion */
img:hover::after {
  top: -30%;
  left: -30%;
  opacity: 1;
}
/* 🌊 UNIVERSAL 3D HOVER EFFECT FOR ALL IMAGES */
img {
  border-radius: 12px;
  transition: transform 0.25s ease, box-shadow 0.35s ease;
  transform-style: preserve-3d;
  perspective: 800px;
  position: relative;
}

/* Glow on hover */
img:hover {
  box-shadow: 0 0 25px #00e6ff;
  transform: scale(1.05);
}
/* EXPLORE IMAGE GRID */
.explore-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
  width: 100%;
  max-width: 900px;
}

.explore-grid img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 0 25px rgba(0,0,0,0.5);
  transition: 0.4s ease;
  cursor: pointer;
}

/* 3D + Glow Hover */
.explore-grid img:hover {
  transform: scale(1.08) rotateX(10deg) rotateY(10deg);
  box-shadow: 0 0 30px #00e6ff;
}
/* EXPLORE IMAGE GRID */
.explore-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
  width: 100%;
  max-width: 900px;
}

.explore-item {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.explore-item img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 0 25px rgba(0,0,0,0.5);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  cursor: pointer;
}

.explore-item img:hover {
  transform: scale(1.08) rotateX(10deg) rotateY(10deg);
  box-shadow: 0 0 30px #00e6ff;
}

.explore-item .caption {
  margin-top: 8px;
  font-size: 14px;
  color: #a6f6ff;
  text-align: center;
}
/* EXPLORE SECTION */
#explore .section-wrapper {
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
  justify-content: center;
  align-items: flex-start;
}

/* TEXT */
#explore .text-wrapper {
  flex: 1;
  min-width: 280px;
  max-width: 500px;
  text-align: left;
}

#explore .text-wrapper h2 {
  font-size: 36px;
  margin-bottom: 20px;
  color: #00e6ff;
}

#explore .text-wrapper p {
  font-size: 16px;
  line-height: 1.7;
  margin-bottom: 15px;
  color: #a6f6ff;
}

/* IMAGE GRID */
.explore-grid {
  flex: 1;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  max-width: 600px;
}

.explore-item {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.explore-item img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 0 25px rgba(0,0,0,0.5);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  cursor: pointer;
}

.explore-item img:hover {
  transform: scale(1.08) rotateX(10deg) rotateY(10deg);
  box-shadow: 0 0 30px #00e6ff;
}

.explore-item .caption {
  margin-top: 8px;
  font-size: 14px;
  color: #a6f6ff;
  text-align: center;
}

/* RESPONSIVE */
@media (max-width: 900px) {
  #explore .section-wrapper {
    flex-direction: column;
    align-items: center;
  }

  #explore .text-wrapper {
    text-align: center;
  }
}

/* Guess Game UI */
.game-section {
  text-align: center;
  padding: 50px 20px;
}

.silhouette-container {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.silhouette {
  width: 260px;
  filter: brightness(0);
  opacity: 1;
  transition: 0.6s ease;
}

.reveal {
  filter: brightness(1);
  transform: scale(1.1);
  opacity: 1;
}

.answer-buttons {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
  margin-top: 10px;
}

.answer-buttons button {
  padding: 12px 20px;
  background: #0077b6;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  font-size: 16px;
  transition: 0.3s;
}

.answer-buttons button:hover {
  background: #00b4d8;
  transform: scale(1.05);
}

#guessResult {
  font-size: 22px;
  margin-top: 15px;
  font-weight: bold;
}

.animal-info {
  margin-top: 20px;
  font-size: 18px;
  color: #ffffff;
}

.next-btn {
  margin-top: 25px;
  padding: 12px 24px;
  background: #00a8e8;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 18px;
  cursor: pointer;
  transition: 0.3s;
}

.next-btn:hover {
  background: #0092c8;
  transform: scale(1.05);
}

.silhouette-container {
  width: 300px;         /* max width for the silhouette container */
  margin: 20px auto;
  text-align: center;
}

.silhouette {
  width: 100%;          /* fill container width */
  max-width: 300px;     /* limit the image size */
  height: auto;         /* maintain aspect ratio */
  filter: blur(5px);    /* blurred initially */
  transition: filter 0.5s, transform 0.5s;
}

.silhouette.reveal {
  filter: blur(0);      /* remove blur when correct */
}

/* --- all your original CSS --- */
/* Include everything you already wrote above, plus these updates for the guessing game */

.game-section {
  text-align: center;
  padding: 50px 20px;
}

.silhouette-container {
  width: 300px;
  margin: 20px auto;
  text-align: center;
}

.silhouette {
  width: 100%;
  max-width: 300px;
  height: auto;
  filter: blur(5px);
  transition: filter 0.5s, transform 0.5s;
}

.silhouette.reveal {
  filter: blur(0);
  transform: scale(1.05);
}

.answer-buttons {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
  margin-top: 10px;
}

.answer-buttons button {
  padding: 12px 20px;
  background: #0077b6;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  font-size: 16px;
  transition: 0.3s;
}

.answer-buttons button:hover {
  background: #00b4d8;
  transform: scale(1.05);
}

#guessResult {
  font-size: 22px;
  margin-top: 15px;
  font-weight: bold;
}

.animal-info {
  margin-top: 20px;
  font-size: 18px;
  color: #ffffff;
}

.next-btn {
  margin-top: 25px;
  padding: 12px 24px;
  background: #00a8e8;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 18px;
  cursor: pointer;
  transition: 0.3s;
}

.next-btn:hover {
  background: #0092c8;
  transform: scale(1.05);
}
/* ----- OCEAN PROBLEMS SLIDER ----- */
#problems-slider {
  padding: 80px 5%;
  text-align: center;
  color: white;
}

.slider-title {
  font-size: 2.5rem;
  margin-bottom: 40px;
  color: #12d4ff;
  text-shadow: 0 0 8px #00c8ff;
}

.slider-container {
  position: relative;
  width: 70%;
  margin: auto;
  overflow: hidden;
  border-radius: 15px;
  box-shadow: 0 0 25px rgba(0, 255, 255, 0.2);
}

.slide {
  display: none;
  animation: fadeSlide 1s ease-in-out;
}

.slide.active {
  display: block;
}

.slide img {
  width: 100%;
  border-radius: 15px;
  height: 380px;
  object-fit: cover;
}

.slide h3 {
  margin-top: 15px;
  font-size: 1.8rem;
  color: #19e6ff;
}

.slide p {
  max-width: 700px;
  margin: 10px auto 20px;
  font-size: 1rem;
  opacity: 0.9;
}

/* Slide animation */
@keyframes fadeSlide {
  from { opacity: 0; transform: translateX(20px); }
  to   { opacity: 1; transform: translateX(0); }
}

/* Buttons */
.slider-buttons {
  margin-top: 20px;
}

.slider-buttons button {
  background: #003b55;
  border: none;
  padding: 12px 20px;
  margin: 0 10px;
  border-radius: 10px;
  color: white;
  font-size: 1.3rem;
  cursor: pointer;
  transition: 1s;
}

.slider-buttons button:hover {
  background: #00c8ff;
  color: #003b55;
}

/* GENERAL NAV BAR STYLING */
nav {
  width: 100%;
  position: fixed;         /* keeps it always on top */
  top: 0;
  left: 0;
  z-index: 1000;

  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 15px 50px;
  background: rgba(0, 50, 100, 0.7); /* semi-transparent blue */
  backdrop-filter: blur(8px);
  box-shadow: 0 4px 10px rgba(0,0,0,0.2);
  box-sizing: border-box;
  transition: 0.3s ease;
}

/* LOGO */
nav .logo {
  font-size: 26px;
  font-weight: 700;
  color: #a6f6ff;
  letter-spacing: 1px;
  text-transform: uppercase;
}

/* NAV LINKS */
nav ul {
  list-style: none;
  display: flex;
  gap: 30px;
}

nav ul li a {
  text-decoration: none;
  color: #a6f6ff;
  font-weight: 500;
  position: relative;
  transition: 0.3s;
}

/* HOVER EFFECT: UNDERLINE ANIMATION */
nav ul li a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -5px;
  width: 0;
  height: 2px;
  background: #00e6ff;
  transition: 0.3s;
}

nav ul li a:hover::after {
  width: 100%;
}

/* HOVER EFFECT: COLOR CHANGE */
nav ul li a:hover {
  color: #00e6ff;
}

/* RESPONSIVE FOR MOBILE */
@media (max-width: 900px) {
  nav {
    flex-direction: column;
    padding: 15px 20px;
  }

  nav ul {
    flex-direction: column;
    gap: 15px;
    margin-top: 10px;
    align-items: center;
  }
}
#solutions-slider {
  padding: 80px 5%;
  text-align: center;
  color: white;
}

.solution-slide {
  display: none;
  animation: fadeSlide 1s ease-in-out;
}

.solution-slide.active {
  display: block;
}

.solution-slide img {
  width: 100%;
  border-radius: 15px;
  height: 380px;
  object-fit: cover;
}

.solution-slide h3 {
  margin-top: 15px;
  font-size: 1.8rem;
  color: #19e6ff;
}

.solution-slide p {
  max-width: 700px;
  margin: 10px auto 20px;
  font-size: 1rem;
  opacity: 0.9;
}

/* Reuse button style */
#solutions-slider .slider-buttons button {
  background: #003b55;
  border: none;
  padding: 12px 20px;
  margin: 0 10px;
  border-radius: 10px;
  color: white;
  font-size: 1.3rem;
  cursor: pointer;
  transition: 1s;
}

#solutions-slider .slider-buttons button:hover {
  background: #00c8ff;
  color: #003b55;
}
