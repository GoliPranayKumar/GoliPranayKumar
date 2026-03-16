<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Goli Pranay Kumar | Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>

/* ---------- GLOBAL ---------- */

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:"Poppins",sans-serif;
}

body{
background:#0f172a;
color:white;
scroll-behavior:smooth;
}

/* ---------- NAVBAR ---------- */

nav{
position:fixed;
top:0;
width:100%;
display:flex;
justify-content:space-between;
padding:15px 10%;
background:rgba(0,0,0,0.4);
backdrop-filter:blur(10px);
z-index:1000;
}

nav h2{
color:#38bdf8;
}

nav ul{
display:flex;
gap:25px;
list-style:none;
}

nav a{
text-decoration:none;
color:white;
transition:.3s;
}

nav a:hover{
color:#38bdf8;
}

/* ---------- HERO ---------- */

.hero{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
background:linear-gradient(135deg,#1e3a8a,#06b6d4);
}

.hero h1{
font-size:3.2rem;
margin-bottom:10px;
animation:fadeIn 1.5s ease;
}

.hero p{
font-size:1.2rem;
opacity:.9;
}

.btn{
margin-top:25px;
padding:12px 30px;
border-radius:30px;
background:white;
color:#0f172a;
text-decoration:none;
font-weight:600;
transition:.3s;
}

.btn:hover{
transform:scale(1.08);
}

/* ---------- SECTIONS ---------- */

section{
padding:80px 10%;
}

.section-title{
text-align:center;
font-size:2rem;
margin-bottom:40px;
}

/* ---------- ABOUT ---------- */

.about{
max-width:700px;
margin:auto;
text-align:center;
line-height:1.7;
}

/* ---------- SKILLS ---------- */

.skills{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
gap:20px;
}

.skill{
background:#1e293b;
padding:20px;
border-radius:10px;
text-align:center;
transition:.3s;
}

.skill:hover{
transform:translateY(-8px);
background:#334155;
}

/* ---------- PROJECTS ---------- */

.projects{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:25px;
}

.project{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
border-radius:12px;
padding:25px;
transition:.3s;
backdrop-filter:blur(10px);
}

.project:hover{
transform:translateY(-10px);
border-color:#38bdf8;
}

.project h3{
margin-bottom:10px;
}

.project p{
opacity:.85;
}

.project a{
display:inline-block;
margin-top:10px;
color:#38bdf8;
text-decoration:none;
}

/* ---------- CONTACT ---------- */

.contact{
text-align:center;
}

.contact a{
display:inline-block;
margin:10px;
padding:10px 20px;
border-radius:25px;
background:#38bdf8;
color:#0f172a;
text-decoration:none;
font-weight:600;
}

/* ---------- FOOTER ---------- */

footer{
text-align:center;
padding:25px;
background:#020617;
}

/* ---------- ANIMATIONS ---------- */

@keyframes fadeIn{
from{
opacity:0;
transform:translateY(20px);
}
to{
opacity:1;
transform:translateY(0);
}
}

</style>

</head>

<body>

<!-- NAVBAR -->

<nav>
<h2>Pranay</h2>
<ul>
<li><a href="#about">About</a></li>
<li><a href="#skills">Skills</a></li>
<li><a href="#projects">Projects</a></li>
<li><a href="#contact">Contact</a></li>
</ul>
</nav>

<!-- HERO -->

<section class="hero">

<h1>👋 Goli Pranay Kumar</h1>
<p>AI & Data Science Student | Aspiring AI Engineer</p>

<a href="#projects" class="btn">Explore My Work</a>

</section>

<!-- ABOUT -->

<section id="about">

<h2 class="section-title">About Me</h2>

<div class="about">

<p>
I am a B.Tech student in Artificial Intelligence and Data Science at 
Vignan Institute of Technology and Science (2023-2027).

I enjoy building AI systems, solving algorithmic problems, and creating
modern web applications.

</p>

</div>

</section>

<!-- SKILLS -->

<section id="skills">

<h2 class="section-title">Tech Stack</h2>

<div class="skills">

<div class="skill">Python</div>
<div class="skill">Java</div>
<div class="skill">C</div>
<div class="skill">JavaScript</div>
<div class="skill">React</div>
<div class="skill">Node.js</div>
<div class="skill">MongoDB</div>
<div class="skill">MySQL</div>

</div>

</section>

<!-- PROJECTS -->

<section id="projects">

<h2 class="section-title">Projects</h2>

<div class="projects">

<div class="project">
<h3>MediScannerAI</h3>
<p>Deep learning based system that analyzes chest X-rays for abnormalities.</p>
<a href="https://github.com/GoliPranayKumar/MediScannerAi">View Project</a>
</div>

<div class="project">
<h3>Yuddha Bhumi</h3>
<p>Strategy battlefield simulation game with tactical gameplay mechanics.</p>
<a href="https://github.com/GoliPranayKumar/YuddhaBhumi">View Project</a>
</div>

<div class="project">
<h3>Credovia</h3>
<p>Credibility scoring system built using Next.js and Appwrite backend.</p>
<a href="https://github.com/GoliPranayKumar/Credovia">View Project</a>
</div>

<div class="project">
<h3>Java Data Structures</h3>
<p>Implementation of stacks, queues, trees, and graph algorithms in Java.</p>
<a href="https://github.com/GoliPranayKumar/DataStructures">View Project</a>
</div>

</div>

</section>

<!-- CONTACT -->

<section id="contact">

<h2 class="section-title">Connect With Me</h2>

<div class="contact">

<a href="https://github.com/GoliPranayKumar">GitHub</a> <a href="https://www.linkedin.com/in/golipranaykumar/">LinkedIn</a> <a href="mailto:golipranaykumar@gmail.com">Email</a>

</div>

</section>

<!-- FOOTER -->

<footer>

<p>© 2026 Goli Pranay Kumar</p>

</footer>

</body>
</html>
