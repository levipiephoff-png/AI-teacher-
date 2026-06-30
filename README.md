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

<section id="pricing">

<div class="container">

<h2>Choose Your Plan</h2>

<div class="grid">

<div class="card">

<h3>Starter</h3>

<h1>$49</h1>

<p>Perfect for beginners</p>

<ul style="text-align:left;line-height:2;">

<li>✔ Full AI Basics Course</li>

<li>✔ Prompt Library</li>

<li>✔ Downloadable Resources</li>

<li>✔ Lifetime Access</li>

</ul>

<br>

<button onclick="buyCourse('Starter')">
Enroll Now
</button>

</div>

<div class="card" style="border:3px solid #00d4ff;transform:scale(1.05);">

<h3>Pro (Most Popular)</h3>

<h1>$149</h1>

<p>Everything in Starter plus:</p>

<ul style="text-align:left;line-height:2;">

<li>✔ Advanced AI Lessons</li>

<li>✔ AI Business Training</li>

<li>✔ Weekly Live Sessions</li>

<li>✔ Community Access</li>

<li>✔ Certificates</li>

</ul>

<br>

<button onclick="buyCourse('Pro')">
Get Pro Access
</button>

</div>

<div class="card">

<h3>Elite</h3>

<h1>$499</h1>

<p>For serious entrepreneurs</p>

<ul style="text-align:left;line-height:2;">

<li>✔ Everything in Pro</li>

<li>✔ Private Coaching</li>

<li>✔ Website Templates</li>

<li>✔ AI Automation Systems</li>

<li>✔ Business Launch Kit</li>

</ul>

<br>

<button onclick="buyCourse('Elite')">
Join Elite
</button>

</div>

</div>

</div>

</section>

<section id="testimonials">

<div class="container">

<h2>Student Success Stories</h2>

<div class="grid">

<div class="card">

<h3>★★★★★</h3>

<p>
"This course completely changed how I use AI every day."
</p>

<strong>- Sarah M.</strong>

</div>

<div class="card">

<h3>★★★★★</h3>

<p>
"I built my first AI business within two months."
</p>

<strong>- Jason R.</strong>

</div>

<div class="card">

<h3>★★★★★</h3>

<p>
"Hands down the best AI course I've taken."
</p>

<strong>- Amanda T.</strong>

</div>

</div>

</div>

</section>

</div>

</section>

<section id="faq">

<div class="container">

<h2>Frequently Asked Questions</h2>

<div class="card">

<h3>Do I need any AI experience?</h3>

<p>
No. This course is designed for complete beginners and gradually progresses to advanced topics.
</p>

</div>

<div class="card">

<h3>How long do I have access?</h3>

<p>
Once enrolled, you'll receive lifetime access to all course content and future updates.
</p>

</div>

<div class="card">

<h3>Will I receive a certificate?</h3>

<p>
Yes! After completing all lessons and passing the final assessment, you'll receive your AI Mastery Academy Certificate.
</p>

</div>

<div class="card">

<h3>Can I access the course on mobile?</h3>

<p>
Absolutely. The website is fully responsive and works on phones, tablets, and computers.
</p>

</div>

</div>

</section>

<section id="contact">

<div class="container">

<h2>Contact Us</h2>

<div class="card">

<form onsubmit="submitContact(event)">

<input
type="text"
id="name"
placeholder="Your Name"
required
style="width:100%;padding:15px;margin:10px 0;border-radius:8px;border:none;"
>

<input
type="email"
id="email"
placeholder="Your Email"
required
style="width:100%;padding:15px;margin:10px 0;border-radius:8px;border:none;"
>

<textarea
id="message"
placeholder="Your Message"
required
style="width:100%;padding:15px;height:150px;margin:10px 0;border-radius:8px;border:none;"
></textarea>

<button type="submit">
Send Message
</button>

</form>

<p id="contactSuccess" class="hidden">
✅ Thanks! Your message has been received.
</p>

</div>

</div>

</section>

<footer>

<div class="container">

<h3>AI Mastery Academy</h3>

<p>
Empowering the next generation with Artificial Intelligence.
</p>

<p>
© 2026 AI Mastery Academy. All Rights Reserved.
</p>

</div>

</footer>

<script>

const lessons = [

{
title: "Welcome to AI Mastery Academy",
video: "https://www.youtube.com/embed/aircAruvnKk",
content: "Welcome! In this lesson you'll learn what Artificial Intelligence is, where it's used today, and how you'll master it throughout this course."
},

{
title: "Understanding Prompt Engineering",
video: "https://www.youtube.com/embed/jC4v5AS4RIM",
content: "Learn how to write prompts that produce accurate, detailed, and consistent AI responses."
},

{
title: "Using AI for Productivity",
video: "https://www.youtube.com/embed/5MgBikgcWnY",
content: "Discover how AI can help with writing, scheduling, brainstorming, coding, research, and automation."
},

{
title: "Building Your AI Business",
video: "https://www.youtube.com/embed/G2fqAlgmoPo",
content: "Put everything together and begin building your own AI-powered business or career."
}

];

let currentLesson = 0;

function openLesson(index){

currentLesson = index;

document.getElementById("lesson").scrollIntoView({
behavior:"smooth"
});

const box = document.getElementById("lessonBox");

box.classList.remove("hidden");

document.getElementById("lessonTitle").innerHTML =
lessons[index].title;

document.getElementById("lessonVideo").innerHTML =
`<iframe width="100%" height="450"
src="${lessons[index].video}"
frameborder="0"
allowfullscreen>
</iframe>`;

document.getElementById("lessonContent").innerHTML =
lessons[index].content;

loadQuiz(index);

}

function nextLesson(){

currentLesson++;

if(currentLesson >= lessons.length){

alert("🎉 Congratulations! You've completed the course.");

return;

}

openLesson(currentLesson);

}

function loadQuiz(index){

const quiz = document.getElementById("quizArea");

const questions = [

{
question:"What does AI stand for?",
answers:[
"Artificial Intelligence",
"Automatic Internet",
"Applied Information"
],
correct:0
},

{
question:"What is Prompt Engineering?",
answers:[
"Writing effective instructions for AI",
"Repairing computers",
"Programming websites"
],
correct:0
},

{
question:"Which task can AI help with?",
answers:[
"Writing",
"Research",
"Automation"
],
correct:0
},

{
question:"What's the goal of this academy?",
answers:[
"Learn practical AI skills",
"Build confidence",
"Create AI-powered projects"
],
correct:0
}

];

const q = questions[index];

quiz.innerHTML = `
<h3>${q.question}</h3>

${q.answers.map((a,i)=>
`<button
style="display:block;margin:10px auto;"
onclick="checkAnswer(${i},${q.correct})">
${a}
</button>`
).join("")}

<div id="quizResult"></div>
`;

}

function checkAnswer(selected, correct){

const result = document.getElementById("quizResult");

if(selected === correct){

result.innerHTML =
"<p style='color:#00ff88;font-weight:bold;'>✅ Correct! Great job.</p>";

}else{

result.innerHTML =
"<p style='color:#ff4d4d;font-weight:bold;'>❌ Incorrect. Try again.</p>";

}

}

function buyCourse(plan){

alert(`🚀 Redirecting to ${plan} enrollment...`);

}

function submitContact(event){

event.preventDefault();

document.getElementById("contactSuccess").classList.remove("hidden");

event.target.reset();

}

const observer = new IntersectionObserver((entries)=>{

entries.forEach(entry => {

if(entry.isIntersecting){

entry.target.classList.add("show");

}

});

});

document.querySelectorAll(".card").forEach(card => {

card.classList.add("hidden");

observer.observe(card);

});

</script>

</body>

</html>