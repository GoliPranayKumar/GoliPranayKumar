<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Goli Pranay Kumar</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:#0f172a;
color:white;
line-height:1.6;
}

header{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
background:linear-gradient(120deg,#0ea5e9,#6366f1);
}

header h1{
font-size:3rem;
margin-bottom:10px;
animation:fadeIn 2s ease-in-out;
}

header h2{
font-weight:300;
animation:fadeIn 3s ease-in-out;
}

.btn{
margin-top:20px;
padding:10px 25px;
background:white;
color:#0f172a;
border-radius:30px;
text-decoration:none;
font-weight:600;
transition:0.3s;
}

.btn:hover{
transform:scale(1.1);
}

section{
padding:70px 10%;
}

.section-title{
font-size:2rem;
margin-bottom:30px;
text-align:center;
}

.about{
text-align:center;
max-width:700px;
margin:auto;
}

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
transition:0.3s;
}

.skill:hover{
transform:translateY(-10px);
background:#334155;
}

.projects{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:25px;
}

.project-card{
background:#1e293b;
padding:25px;
border-radius:12px;
transition:0.3s;
position:relative;
overflow:hidden;
}

.project-card:hover{
transform:translateY(-10px);
}

.project-card h3{
margin-bottom:10px;
}

.project-card a{
display:inline-block;
margin-top:10px;
color:#38bdf8;
text-decoration:none;
}

footer{
text-align:center;
padding:30px;
background:#020617;
margin-top:50px;
}

.social{
margin-top:15px;
}

.social a{
margin:0 10px;
color:white;
font-size:20px;
text-decoration:none;
}

@keyframes fadeIn{
from{opacity:0; transform:translateY(20px);}
to{opacity:1; transform:translateY(0);}
}

</style>
</head>

<body>

<header>
<h1>👋 Goli Pranay Kumar</h1>
<h2>AI & Data Science Student | Aspiring AI Engineer</h2>
<a href="#projects" class="btn">View My Work</a>
</header>

<section>
<h2 class="section-title">About Me</h2>
<div class="about">
<p>
B.Tech student in Artificial Intelligence and Data Science at Vignan Institute of Technology and Science.
Interested in AI, Data Structures, and building real-world software systems.
</p>
</div>
</section>

<section>
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

<section id="projects">
<h2 class="section-title">Projects</h2>

<div class="projects">

<div class="project-card">
<h3>MediScannerAI</h3>
<p>AI powered system that analyzes chest X-rays using deep learning.</p>
<a href="https://github.com/GoliPranayKumar/MediScannerAi">View Project</a>
</div>

<div class="project-card">
<h3>Yuddha Bhumi</h3>
<p>Strategy battlefield simulation game with tactical gameplay.</p>
<a href="https://github.com/GoliPranayKumar/YuddhaBhumi">View Project</a>
</div>

<div class="project-card">
<h3>Credovia</h3>
<p>Full stack credibility scoring system built with Next.js and Appwrite.</p>
<a href="https://github.com/GoliPranayKumar/Credovia">View Project</a>
</div>

<div class="project-card">
<h3>Java Data Structures</h3>
<p>Implementation of stacks, queues, trees and graph algorithms.</p>
<a href="https://github.com/GoliPranayKumar/DataStructures">View Project</a>
</div>

</div>
</section>

<section>
<h2 class="section-title">Goals</h2>

<div class="about">
<p>
Solve 500+ LeetCode problems, build AI-powered SaaS applications,
and contribute to open source projects.
</p>
</div>

</section>

<footer>

<p>© 2026 Goli Pranay Kumar</p>

<div class="social">
<a href="https://github.com/GoliPranayKumar">GitHub</a>
<a href="https://www.linkedin.com/in/golipranaykumar/">LinkedIn</a>
</div>

</footer>

</body>
</html>
