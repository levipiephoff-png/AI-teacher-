<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AI Mastery Academy</title>

<link rel="preconnect" href="https://fonts.googleapis.com">

<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&display=swap" rel="stylesheet">

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
    margin:0 auto 30px;
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
    grid-template-columns:
    repeat(auto-fit,minmax(280px,1fr));
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

.lesson-card{
    border-left:5px solid #38bdf8;
}

.quiz-btn{
    display:block;
    width:100%;
    margin:10px 0;
}

.price{
    font-size:42px;
    font-weight:800;
    color:#38bdf8;
}

.price-card{
    text-align:center;
}

</style>

</head>
<body>

<nav>

<a href="#home">Home</a>

<a href="#course">Course</a>

<a href="#pricing">Pricing</a>

<a href="#lessons">Lessons</a>

</nav>


<header id="home">

<h1>AI Mastery Academy</h1>

<p>
Learn how to use Artificial Intelligence to improve your
skills, productivity, creativity, and future career.
</p>

<button class="hero-btn" onclick="startCourse()">
Start Learning
</button>

</header>


<section id="pricing">

<div class="container">

<div class="card price-card">

<h2>Learn AI Without Breaking the Bank</h2>

<p>
Get access to the complete AI Mastery Academy course.
</p>

<div class="price">
$9.99
</div>

<p>
One simple payment for the course.
</p>

<br>

<button onclick="startCourse()">
Get Started
</button>

</div>

</div>

</section>


<section id="course">

<div class="container">

<h2>What You'll Learn</h2>

<br>

<div class="grid">


<div class="card">

<h3>🤖 AI Fundamentals</h3>

<p>
Understand what AI is, how it works, and how
you can use it in everyday life.
</p>

</div>


<div class="card">

<h3>💬 Prompt Engineering</h3>

<p>
Learn how to write better prompts and get
better results from AI tools.
</p>

</div>


<div class="card">

<h3>🎨 Creative AI</h3>

<p>
Explore AI for images, video, writing,
and other creative projects.
</p>

</div>


<div class="card">

<h3>⚡ AI Productivity</h3>

<p>
Use AI to save time, organize your work,
and become more productive.
</p>

</div>


<div class="card">

<h3>💼 AI Business</h3>

<p>
Discover ways AI can help with businesses,
marketing, research, and online projects.
</p>

</div>


<div class="card">

<h3>💻 AI Coding</h3>

<p>
Learn how AI can help you understand,
write, and improve code.
</p>

</div>


</div>

</div>

</section>
<section id="lessons">

<div class="container">

<h2>4-Week AI Mastery Course</h2>

<p>
Work through the lessons at your own pace and build
real AI skills along the way.
</p>

<br>

<div class="grid">


<div class="card lesson-card">

<h3>Week 1 — AI Foundations</h3>

<p>
Introduction to AI<br>
Understanding ChatGPT<br>
Writing Better Prompts<br>
AI for Everyday Tasks<br>
AI Safety & Responsible Use
</p>

<button onclick="openLesson(1)">
Start Week 1
</button>

</div>


<div class="card lesson-card">

<h3>Week 2 — AI Skills</h3>

<p>
Advanced Prompting<br>
Image AI<br>
Video AI<br>
Voice AI<br>
AI Productivity
</p>

<button onclick="openLesson(2)">
Start Week 2
</button>

</div>


<div class="card lesson-card">

<h3>Week 3 — AI Applications</h3>

<p>
Automation<br>
Coding with AI<br>
Business AI<br>
Marketing AI<br>
Research AI
</p>

<button onclick="openLesson(3)">
Start Week 3
</button>

</div>


<div class="card lesson-card">

<h3>Week 4 — AI Projects</h3>

<p>
Build AI Projects<br>
Create an AI Workflow<br>
Launch an AI Project<br>
Build Your Portfolio<br>
Final Course Challenge
</p>

<button onclick="openLesson(4)">
Start Week 4
</button>

</div>


</div>

</div>

</section>


<section id="progress">

<div class="container">

<div class="card">

<h2>Your Progress</h2>

<br>

<div class="progress">

<div id="bar"></div>

</div>

<br>

<p id="progressText">
0% Complete
</p>

</div>

</div>

</section>


<section id="lesson">

<div class="container">

<div class="card hidden" id="lessonBox">

<h2 id="lessonTitle">
Lesson Title
</h2>

<br>

<p id="lessonContent">
Your lesson content will appear here.
</p>

<br>

<button onclick="completeLesson()">
Complete Lesson
</button>

</div>

</div>

</section>
<script>

let currentWeek = 0;

let completedLessons = 0;

const lessons = {

1: {
title: "Week 1 — AI Foundations",
content: `
<h3>Welcome to AI Foundations!</h3>

<p>
In this week, you'll learn the basics of artificial
intelligence and how to use AI tools effectively.
</p>

<br>

<h3>Lesson 1: Introduction to AI</h3>

<p>
Artificial Intelligence allows computers to perform
tasks that normally require human intelligence.
Examples include understanding language, recognizing
images, solving problems, and generating content.
</p>

<br>

<h3>Lesson 2: Understanding ChatGPT</h3>

<p>
ChatGPT is an AI assistant that can help you write,
brainstorm, learn, research, organize information,
and solve problems.
</p>

<br>

<h3>Lesson 3: Writing Better Prompts</h3>

<p>
A good prompt clearly explains what you want the AI
to do. Include your goal, useful context, and the
format you want in the answer.
</p>

<br>

<h3>Lesson 4: AI for Everyday Tasks</h3>

<p>
AI can help with studying, planning, writing,
brainstorming, scheduling, and many other everyday
tasks.
</p>

<br>

<h3>Lesson 5: AI Safety</h3>

<p>
Always review important AI-generated information.
Avoid sharing private information and remember that
AI can sometimes make mistakes.
</p>
`
},


2: {
title: "Week 2 — AI Skills",
content: `
<h3>Build Your AI Skills</h3>

<p>
Now that you understand the basics, it's time to
learn how to use AI for more advanced tasks.
</p>

<br>

<h3>Advanced Prompting</h3>

<p>
Learn how to give AI detailed instructions,
examples, constraints, and desired output formats.
</p>

<br>

<h3>Image AI</h3>

<p>
AI image tools can help you create graphics,
concept art, advertisements, illustrations,
and other visual content.
</p>

<br>

<h3>Video AI</h3>

<p>
AI can assist with video ideas, scripts,
storyboards, editing, and visual effects.
</p>

<br>

<h3>Voice AI</h3>

<p>
Voice AI can help create transcripts, voice
content, summaries, and other audio projects.
</p>

<br>

<h3>AI Productivity</h3>

<p>
Use AI to organize information, create plans,
summarize documents, and save time.
</p>
`
},


3: {
title: "Week 3 — AI Applications",
content: `
<h3>Apply AI to Real-World Tasks</h3>

<p>
This week focuses on using AI for business,
coding, marketing, automation, and research.
</p>

<br>

<h3>Automation</h3>

<p>
Learn how AI can help automate repetitive tasks
and create more efficient workflows.
</p>

<br>

<h3>Coding with AI</h3>

<p>
AI can help explain code, find errors, create
examples, and assist with programming projects.
</p>

<br>

<h3>Business AI</h3>

<p>
Explore ways businesses can use AI for customer
service, planning, analysis, and productivity.
</p>

<br>

<h3>Marketing AI</h3>

<p>
Use AI to brainstorm marketing ideas, write
content, develop campaigns, and understand
your audience.
</p>

<br>

<h3>Research AI</h3>

<p>
Learn how AI can help organize information,
compare ideas, summarize sources, and assist
with research.
</p>
`
},


4: {
title: "Week 4 — AI Projects",
content: `
<h3>Build Something With AI</h3>

<p>
This final week is about putting everything
you've learned into practice.
</p>

<br>

<h3>Build AI Projects</h3>

<p>
Choose an idea and use AI to help you plan
and build a real project.
</p>

<br>

<h3>Create an AI Workflow</h3>

<p>
Combine multiple AI tools and techniques into
a workflow that solves a specific problem.
</p>

<br>

<h3>Launch an AI Project</h3>

<p>
Learn how to turn an idea into something that
other people can actually use.
</p>

<br>

<h3>Build Your Portfolio</h3>

<p>
Document your projects and skills so you can
show other people what you've learned.
</p>

<br>

<h3>Final Course Challenge</h3>

<p>
Create a project that demonstrates the AI skills
you developed throughout the course.
</p>
`
}

};


function openLesson(week){

currentWeek = week;

const lesson = lessons[week];

document.getElementById("lessonBox").classList.remove("hidden");

document.getElementById("lessonTitle").textContent =
lesson.title;

document.getElementById("lessonContent").innerHTML =
lesson.content;

document.getElementById("lesson").scrollIntoView({
behavior:"smooth"
});

}


function startCourse(){

document.getElementById("lessons").scrollIntoView({
behavior:"smooth"
});

}


function completeLesson(){

if(currentWeek === 0){
return;
}

completedLessons++;

if(completedLessons > 4){
completedLessons = 4;
}

updateProgress();

alert("Great job! Lesson completed.");

}


function updateProgress(){

const percentage =
(completedLessons / 4) * 100;

document.getElementById("bar").style.width =
percentage + "%";

document.getElementById("progressText").textContent =
Math.round(percentage) + "% Complete";

}

</script>
<section id="quizzes">

<div class="container">

<h2>Knowledge Checks</h2>

<p>
Test what you've learned after each week.
</p>

<br>


<div class="card">

<h3>Week 1 Quiz</h3>

<p>
What is Artificial Intelligence?
</p>

<br>

<button class="quiz-btn"
onclick="checkAnswer(this, true)">
A computer system that can perform tasks
that normally require human intelligence
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
A type of computer monitor
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
A social media platform
</button>

<p class="quiz-result"></p>

</div>


<br>


<div class="card">

<h3>Week 2 Quiz</h3>

<p>
What makes a prompt more effective?
</p>

<br>

<button class="quiz-btn"
onclick="checkAnswer(this, true)">
Clear instructions and useful context
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
Using as few words as possible
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
Giving the AI no instructions
</button>

<p class="quiz-result"></p>

</div>


<br>


<div class="card">

<h3>Week 3 Quiz</h3>

<p>
Which is an example of using AI for business?
</p>

<br>

<button class="quiz-btn"
onclick="checkAnswer(this, true)">
Automating repetitive tasks
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
Turning off all computers
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
Deleting business information
</button>

<p class="quiz-result"></p>

</div>


<br>


<div class="card">

<h3>Week 4 Final Challenge</h3>

<p>
What is the best way to demonstrate your
AI skills?
</p>

<br>

<button class="quiz-btn"
onclick="checkAnswer(this, true)">
Build a useful AI project
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
Only read about AI
</button>

<button class="quiz-btn"
onclick="checkAnswer(this, false)">
Avoid using AI tools
</button>

<p class="quiz-result"></p>

</div>

</div>

</section>
<section id="enroll">

<div class="container">

<div class="card price-card">

<h2>Ready to Master AI?</h2>

<p>
Get full access to the AI Mastery Academy course
and start learning today.
</p>

<br>

<div class="price">
$9.99
</div>

<p>
One-time course price
</p>

<br>

<ul style="list-style:none; padding:0;">

<li>✅ 4 Weeks of AI Training</li>

<li>✅ AI Fundamentals</li>

<li>✅ Prompt Engineering</li>

<li>✅ Image, Video & Voice AI</li>

<li>✅ AI Productivity</li>

<li>✅ Business & Marketing AI</li>

<li>✅ Coding with AI</li>

<li>✅ AI Projects</li>

<li>✅ Knowledge Checks</li>

</ul>

<br>

<button onclick="enrollNow()">
Enroll for $9.99
</button>

<p id="enrollMessage"></p>

</div>

</div>

</section>
<section id="about">

<div class="container">

<div class="card">

<h2>About AI Mastery Academy</h2>

<br>

<p>
AI Mastery Academy was created to make learning
Artificial Intelligence simple, practical, and
accessible.
</p>

<br>

<p>
You don't need to be a programmer or an AI expert
to get started. This course takes you from the
fundamentals of AI to practical projects you can
actually use.
</p>

<br>

<p>
Learn at your own pace, practice what you learn,
and build skills that can help you in school,
work, business, and everyday life.
</p>

</div>

</div>

</section>


<section id="faq">

<div class="container">

<h2>Frequently Asked Questions</h2>

<br>


<div class="card">

<h3>Do I need experience with AI?</h3>

<p>
No. The course starts with the fundamentals and
gradually moves into more advanced topics.
</p>

</div>


<br>


<div class="card">

<h3>Do I need to know how to code?</h3>

<p>
No. Coding is included as one part of the course,
but you can learn the other AI skills without
having programming experience.
</p>

</div>


<br>


<div class="card">

<h3>How long does the course take?</h3>

<p>
The course is organized into four weeks, but you
can learn at your own pace.
</p>

</div>


<br>


<div class="card">

<h3>Is the course online?</h3>

<p>
Yes. The course is designed to be completed online
from a computer, tablet, or compatible mobile device.
</p>

</div>


<br>


<div class="card">

<h3>What will I learn?</h3>

<p>
You'll learn AI fundamentals, prompting, creative AI,
productivity, automation, coding, business AI,
marketing, research, and practical AI projects.
</p>

</div>


<br>


<div class="card">

<h3>How much does the course cost?</h3>

<p>
The current one-time price is only
<strong>$9.99</strong>.
</p>

</div>


</div>

</section>
<footer>

<h2>AI Mastery Academy</h2>

<br>

<p>
Learn AI. Build skills. Create something amazing.
</p>

<br>

<div>

<a href="#home"
style="color:#38bdf8; margin:10px; text-decoration:none;">
Home
</a>

<a href="#course"
style="color:#38bdf8; margin:10px; text-decoration:none;">
Course
</a>

<a href="#lessons"
style="color:#38bdf8; margin:10px; text-decoration:none;">
Lessons
</a>

<a href="#pricing"
style="color:#38bdf8; margin:10px; text-decoration:none;">
Pricing
</a>

<a href="#faq"
style="color:#38bdf8; margin:10px; text-decoration:none;">
FAQ
</a>

</div>

<br>

<p>
© 2026 AI Mastery Academy. All rights reserved.
</p>

</footer>


</body>

</html>