<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Med Gaming | Ultimate Gaming Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;800&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{
    font-family:'Poppins',sans-serif;
    background:#0a0a0f;
    color:#fff;
    overflow-x:hidden;
    cursor:none;
}

/* Custom Cursor */
.cursor{
    width:20px;
    height:20px;
    border:2px solid #00f7ff;
    border-radius:50%;
    position:fixed;
    pointer-events:none;
    transform:translate(-50%,-50%);
    transition:0.1s ease;
    z-index:9999;
}

/* Particle Canvas */
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
    justify-content:space-between;
    align-items:center;
    padding:20px 10%;
    background:#111122;
    border-bottom:2px solid #00f7ff;
}

header h1{
    font-family:'Orbitron',sans-serif;
    color:#00f7ff;
}

nav a{
    color:#fff;
    text-decoration:none;
    margin-left:25px;
    position:relative;
}

nav a::after{
    content:"";
    position:absolute;
    width:0%;
    height:2px;
    background:#ff00c8;
    bottom:-5px;
    left:0;
    transition:0.3s;
}

nav a:hover::after{width:100%;}

.hero{
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
}

.hero h2{
    font-family:'Orbitron',sans-serif;
    font-size:55px;
}

.hero span{color:#ff00c8;}

.typing{
    margin-top:15px;
    font-size:20px;
    color:#00f7ff;
    height:30px;
}

.btn{
    margin-top:30px;
    padding:12px 35px;
    border:2px solid #00f7ff;
    color:#00f7ff;
    text-decoration:none;
    border-radius:30px;
    transition:0.3s;
}

.btn:hover{
    background:#00f7ff;
    color:#000;
    box-shadow:0 0 20px #00f7ff;
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

section h2{
    font-family:'Orbitron',sans-serif;
    margin-bottom:40px;
    color:#00f7ff;
}

.projects-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
}

.project-card{
    background:#111122;
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
