<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GTA SA NARUTO MOD PACK | Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;800&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{
    font-family:'Poppins',sans-serif;
    background:linear-gradient(135deg,#f59e0b,#1e293b);
    color:#fff;
    overflow-x:hidden;
    cursor:none;
    position:relative;
}
.cursor{
    width:20px;
    height:20px;
    border:2px solid #f59e0b;
    border-radius:50%;
    position:fixed;
    pointer-events:none;
    transform:translate(-50%,-50%);
    transition:0.1s ease;
    z-index:9999;
}
#particles{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    z-index:-2;
}
header{
    display:flex;
    justify-content:center;
    align-items:center;
    padding:20px 10%;
    background:rgba(0,0,0,0.7);
    border-bottom:2px solid #f59e0b;
}
.logo{
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:10px;
}
.logo-image{
    width:300px;
    max-width:90%;
    margin-top:15px;
    border-radius:15px;
    box-shadow:0 0 25px rgba(245,158,11,0.7);
    opacity:0;
    transform:translateY(20px);
    animation:fadeInImage 1.5s ease forwards;
}

@keyframes fadeInImage{
    to{
        opacity:1;
        transform:translateY(0);
    }
}
.logo h1{
    font-family:'Orbitron',sans-serif;
    color:#f59e0b;
    letter-spacing:2px;
    font-size:36px;
}
.logo .subtitle{
    font-family:'Orbitron',sans-serif;
    color:#fff;
    font-size:20px;
    letter-spacing:1px;
}
.hero{
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    position:relative;
}
.hero h2{
    font-family:'Orbitron',sans-serif;
    font-size:55px;
    color:#f59e0b;
    z-index:1;
}
.typing{
    margin-top:15px;
    font-size:20px;
    color:#fff;
    height:30px;
    z-index:1;
}
.btn{
    margin-top:30px;
    padding:12px 35px;
    border:2px solid #f59e0b;
    color:#f59e0b;
    text-decoration:none;
    border-radius:30px;
    transition:0.3s;
    z-index:1;
}
.btn:hover{
    background:#f59e0b;
    color:#000;
    box-shadow:0 0 20px #f59e0b;
}
section{
    padding:100px 10%;
    text-align:center;
    opacity:0;
    transform:translateY(40px);
    transition:1s ease;
}
section.show{
    opacity:1;
    transform:translateY(0);
}
section h2{font-family:'Orbitron',sans-serif;margin-bottom:40px;color:#f59e0b;}
.projects-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}
.project-card{
    background:rgba(0,0,0,0.7);
    padding:25px;
    border-radius:15px;
    border:1px solid #222;
    transition:0.3s;
}
.project-card:hover{
    transform:translateY(-10px) scale(1.05);
    box-shadow:0 0 25px #f59e0b;
    border-color:#f59e0b;
}
.download-section{
    margin-top:50px;
}
.download-section button{
    padding:15px 25px;
    margin:10px;
    border:none;
    border-radius:15px;
    background:linear-gradient(45deg,#f59e0b,#1e293b);
    color:#fff;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}
.download-section button:hover{
    box-shadow:0 0 20px #f59e0b;
}
footer{
    padding:20px;
    text-align:center;
    background:rgba(0,0,0,0.7);
    border-top:2px solid #f59e0b;
}
@media(max-width:768px){
.hero h2{font-size:32px;}
.logo h1{font-size:28px;}
.logo .subtitle{font-size:16px;}
}
</style>
</head>
<body>
<canvas id="particles"></canvas>
<div class="cursor"></div>

<header>
<div class="logo">
    <h1>Med Gaming</h1>
    <div class="subtitle">GTA SA NARUTO MOD PACK</div>
    
</div>
</header>

<section class="hero" id="home">
<h2>GTA SA NARUTO MOD PACK</h2>
<div class="typing" id="typing"></div>
<a href="#projects" class="btn">Enter My World</a>
</section>

<section id="about">
<h2>About Me</h2>
<p>I create futuristic gaming websites blending Naruto and GTA San Andreas themes with neon effects, animations, and immersive UI experiences.</p>
</section>

<section id="projects">
<h2>My Projects</h2>
<div class="projects-grid">
<div class="project-card"><h3>Gaming Website</h3><p>Futuristic neon design project.</p></div>
<div class="project-card"><h3>Esports Branding Kit</h3><p>Complete gaming brand identity with logo, banners, and social media design.</p></div>
<div class="project-card"><h3>Portfolio Design</h3><p>Interactive animated portfolio.</p></div>
</div>
</section>

<section id="download" class="download-section">
<h2>Download</h2>
<button onclick="window.location.href='https://shrtslug.biz/8HrZ9'">Download APK</button>
<button onclick="window.location.href='game.obb'">Download OBB</button>
<button onclick="window.location.href='game-data.zip'">Download Data</button>
<br>
<button onclick="window.location.href='tutorial.html'">Tutorial / طريقة تركيب الملفات</button>
</section>

<section id="contact">
<h2>Contact Me</h2>
<p>Email: meddibmaylos@gmail.com</p>
</section>

<footer>
<p>© 2026 Med Gaming | GTA SA NARUTO MOD PACK</p>
</footer>

<script>
/* Cursor */
const cursor=document.querySelector('.cursor');
document.addEventListener('mousemove',e=>{cursor.style.left=e.clientX+'px';cursor.style.top=e.clientY+'px';});

/* Typing */
const texts=["Gaming Content Creator","Web Developer","UI Designer"];
let count=0,index=0,currentText='',letter='';
(function type(){if(count===texts.length){count=0;}currentText=texts[count];letter=currentText.slice(0,++index);document.getElementById('typing').textContent=letter;if(letter.length===currentText.length){count++;index=0;setTimeout(type,1000);}else{setTimeout(type,100);}})();

/* Scroll Anim */
const sections=document.querySelectorAll('section');
window.addEventListener('scroll',()=>{sections.forEach(sec=>{const top=sec.getBoundingClientRect().top;if(top<window.innerHeight-100){sec.classList.add('show');}});});

/* Naruto-style Particles */
const canvas=document.getElementById('particles');
const ctx=canvas.getContext('2d');
canvas.width=window.innerWidth;
canvas.height=window.innerHeight;
let particlesArray=[];
class Particle{
  constructor(){
    this.x=Math.random()*canvas.width;
    this.y=Math.random()*canvas.height;
    this.size=Math.random()*4+1;
    this.speedX=Math.random()*1-0.5;
    this.speedY=Math.random()*1-0.5;
    this.color='rgba(255,200,0,'+Math.random()+')';
  }
  update(){
    this.x+=this.speedX;
    this.y+=this.speedY;
    if(this.x>canvas.width)this.x=0;
    if(this.x<0)this.x=canvas.width;
    if(this.y>canvas.height)this.y=0;
    if(this.y<0)this.y=canvas.height;
  }
  draw(){
    ctx.fillStyle=this.color;
    ctx.beginPath();
    ctx.arc(this.x,this.y,this.size,0,Math.PI*2);
    ctx.fill();
  }
}
function init(){
  for(let i=0;i<150;i++){
    particlesArray.push(new Particle());
  }
}
function animate(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  particlesArray.forEach(p=>{p.update();p.draw();});
  requestAnimationFrame(animate);
}
init();
animate();
</script>

</body>
</html>
    padding:25px;
    border-radius:15px;
    border:1px solid #222;
    transition:0.3s;
}

.project-card:hover{
    transform:translateY(-10px) scale(1.05);
    box-shadow:0 0 25px #ff00c8;
    border-color:#ff00c8;
}

footer{
    padding:20px;
    text-align:center;
    background:#111122;
    border-top:2px solid #ff00c8;
}

@media(max-width:768px){
.hero h2{font-size:32px;}
}
</style>
</head>
<body>

<canvas id="particles"></canvas>
<div class="cursor"></div>

<header>
<div style="display:flex;align-items:center;gap:15px;">
    <div style="width:45px;height:45px;border-radius:10px;background:linear-gradient(135deg,#00f7ff,#ff00c8);display:flex;align-items:center;justify-content:center;font-family:'Orbitron',sans-serif;font-weight:800;color:#000;box-shadow:0 0 15px #00f7ff;">
        MG
    </div>
    <h1 style="font-family:'Orbitron',sans-serif;color:#00f7ff;letter-spacing:2px;">Med Gaming</h1>
</div>
<nav>
<a href="#home">Home</a>
<a href="#about">About</a>
<a href="#projects">Projects</a>
<a href="#contact">Contact</a>
</nav>
</header>

<section class="hero" id="home">
<h2>I'm <span>Med Gaming</span></h2>
<div class="typing" id="typing"></div>
<a href="#projects" class="btn">Enter My World</a>
</section>

<section id="about">
<h2>About Me</h2>
<p>I build futuristic gaming-style websites with neon effects, animations, and creative UI experiences.</p>
</section>

<section id="projects">
<h2>My Projects</h2>
<div class="projects-grid">
<div class="project-card"><h3>Gaming Website</h3><p>Futuristic neon design project.</p></div>
<div class="project-card"><h3>Esports Branding Kit</h3><p>Complete gaming brand identity with logo, banners, and social media design.</p></div>
<div class="project-card"><h3>Portfolio Design</h3><p>Interactive animated portfolio.</p></div>
</div>
</section>

<section id="contact">
<h2>Contact Me</h2>
<p>Email: meddibmaylos@gmail.com</p>
</section>

<footer>
<p>© 2026 Med Gaming | Ultimate Gaming Portfolio</p>
</footer>

<script>

/* Custom Cursor */
const cursor = document.querySelector('.cursor');
document.addEventListener('mousemove', e => {
    cursor.style.left = e.clientX + 'px';
    cursor.style.top = e.clientY + 'px';
});

/* Typing Effect */
const texts = ["Gaming Content Creator","Web Developer","UI Designer"];
let count = 0;
let index = 0;
let currentText = '';
let letter = '';

(function type(){
    if(count === texts.length){count = 0;}
    currentText = texts[count];
    letter = currentText.slice(0, ++index);
    document.getElementById('typing').textContent = letter;
    if(letter.length === currentText.length){
        count++;
        index = 0;
        setTimeout(type, 1000);
    } else {
        setTimeout(type, 100);
    }
})();

/* Scroll Animation */
const sections = document.querySelectorAll('section');
window.addEventListener('scroll', () => {
    sections.forEach(sec => {
        const top = sec.getBoundingClientRect().top;
        if(top < window.innerHeight - 100){
            sec.classList.add('show');
        }
    });
});

/* Simple Particles */
const canvas = document.getElementById('particles');
const ctx = canvas.getContext('2d');
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;
let particlesArray = [];

class Particle{
    constructor(){
        this.x = Math.random()*canvas.width;
        this.y = Math.random()*canvas.height;
        this.size = Math.random()*2;
        this.speedX = Math.random()*0.5 - 0.25;
        this.speedY = Math.random()*0.5 - 0.25;
    }
    update(){
        this.x += this.speedX;
        this.y += this.speedY;
    }
    draw(){
        ctx.fillStyle = '#00f7ff';
        ctx.fillRect(this.x,this.y,this.size,this.size);
    }
}

function init(){
    for(let i=0;i<100;i++){
        particlesArray.push(new Particle());
    }
}

function animate(){
    ctx.clearRect(0,0,canvas.width,canvas.height);
    particlesArray.forEach(p=>{
        p.update();
        p.draw();
    });
    requestAnimationFrame(animate);
}

init();
animate();

</script>

</body>
</html>
