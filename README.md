<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AI Mastery Academy</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
}

html{
scroll-behavior:smooth;
}

body{
font-family:'Poppins',sans-serif;
background:#0f172a;
color:white;
line-height:1.6;
}

nav{
position:sticky;
top:0;
z-index:999;
display:flex;
justify-content:center;
align-items:center;
gap:25px;
padding:18px;
background:#020617;
box-shadow:0 2px 12px rgba(0,0,0,.4);
}

nav a{
text-decoration:none;
color:white;
font-weight:600;
transition:.3s;
}

nav a:hover{
color:#38bdf8;
}

header{
background:linear-gradient(135deg,#1e293b,#0f172a);
padding:90px 20px;
text-align:center;
}

header h1{
font-size:3.2rem;
margin-bottom:15px;
}

header p{
font-size:1.2rem;
color:#cbd5e1;
max-width:700px;
margin:auto;
margin-bottom:30px;
}

.hero-btn{
padding:16px 32px;
font-size:18px;
background:#38bdf8;
border:none;
border-radius:12px;
color:white;
cursor:pointer;
transition:.3s;
}

.hero-btn:hover{
background:#0ea5e9;
transform:scale(1.05);
}

.container{
width:95%;
max-width:1200px;
margin:auto;
padding:60px 0;
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:25px;
}

.card{
background:#1e293b;
padding:25px;
border-radius:18px;
box-shadow:0 10px 25px rgba(0,0,0,.35);
transition:.3s;
}

.card:hover{
transform:translateY(-8px);
}

section{
padding:40px 0;
}

button{
padding:12px 24px;
border:none;
border-radius:10px;
background:#38bdf8;
color:white;
font-weight:bold;
cursor:pointer;
transition:.3s;
}

button:hover{
background:#0ea5e9;
}

.progress{
width:100%;
height:18px;
background:#334155;
border-radius:30px;
overflow:hidden;
}

#bar{
height:100%;
width:0%;
background:#22c55e;
transition:.5s;
}

iframe{
width:100%;
height:380px;
border:none;
border-radius:12px;
}

.hidden{
display:none;
}

footer{
background:#020617;
text-align:center;
padding:35px;
color:#94a3b8;
margin-top:60px;
}

.badge{
display:inline-block;
padding:8px 16px;
background:#22c55e;
border-radius:30px;
margin:5px;
font-size:14px;
}

.lesson-card{
border-left:5px solid #38bdf8;
}

.quiz-btn{
display:block;
width:100%;
margin:10px 0;
}

</style>

</head>

<body>

<nav>

<a href="#home">Home</a>
<a href="#dashboard">Dashboard</a>
<a href="#curriculum">Curriculum</a>
<a href="#lesson">Lessons</a>
<a href="#resources">Resources</a>
<a href="#contact">Contact</a>

</nav>

<header id="home">

<h1>🚀 AI Mastery Academy</h1>

<p>
Master Artificial Intelligence step-by-step through a structured
20-day program designed for complete beginners.
</p>

<button class="hero-btn" onclick="startCourse()">
Start Your Journey
</button>

</header>

<section id="dashboard">

<div class="container">

<h2>📊 Student Dashboard</h2>

<div class="grid">

<div class="card">

<h3>Course Progress</h3>

<p id="progressText">0% Complete</p>

<div class="progress">
<div id="bar"></div>
</div>

</div>

<div class="card">

<h3>Current Lesson</h3>

<h2 id="currentLesson">
Day 1
</h2>

<p>
Continue learning where you left off.
</p>

</div>

<div class="card">

<h3>Achievements</h3>

<div id="badges">

<span class="badge">
🎯 Beginner
</span>

</div>

</div>

</div>

</div>

</section>

<section id="curriculum">

<div class="container">

<h2>📚 20-Day Curriculum</h2>

<div class="grid">

<div class="card lesson-card">

<h3>Week 1</h3>

<p>
AI Basics<br>
What is ChatGPT?<br>
Prompt Writing<br>
AI Ethics<br>
Daily Practice
</p>

</div>

<div class="card lesson-card">

<h3>Week 2</h3>

<p>
Advanced Prompting<br>
Image AI<br>
Video AI<br>
Voice AI<br>
Productivity
</p>

</div>

<div class="card lesson-card">

<h3>Week 3</h3>

<p>
Automation<br>
Coding with AI<br>
Business AI<br>
Marketing AI<br>
Research AI
</p>

</div>

<div class="card lesson-card">

<h3>Week 4</h3>

<p>
Build Projects<br>
Launch Your AI Business<br>
Portfolio<br>
Final Assessment<br>
Certificate
</p>

</div>

</div>

</div>

</section>

<section id="lesson">

<div class="container">

<div class="card hidden" id="lessonBox">

<h2 id="lessonTitle">
Lesson Title
</h2>

<div id="lessonVideo"></div>

<br>

<p id="lessonContent">
Lesson content will appear here.
</p>

<br>

<div id="quizArea"></div>

<br>

<button onclick="nextLesson()">
Next Lesson
</button>

</div>

</div>

</section>