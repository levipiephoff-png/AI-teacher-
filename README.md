<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AI Mastery Academy</title>

<style>

body {

  margin: 0;

  font-family: Arial;

  background: #0f172a;

  color: white;

  text-align: center;

}

header {

  background: #1e293b;

  padding: 20px;

}

.card {

  background: #1e293b;

  margin: 15px;

  padding: 15px;

  border-radius: 12px;

}

button {

  padding: 12px;

  margin: 5px;

  border: none;

  border-radius: 8px;

  background: #38bdf8;

  font-weight: bold;

  cursor: pointer;

}

.progress {

  background: #334155;

  height: 15px;

  border-radius: 10px;

  overflow: hidden;

}

#bar {

  height: 100%;

  width: 0%;

  background: #22c55e;

}

iframe {

  width: 100%;

  max-width: 500px;

  height: 250px;

  border-radius: 10px;

}

</style>

</head>

<body>

<header>

<h1>AI Mastery Academy</h1>

<p>Beginner → Intermediate AI Course</p>

</header>

<div class="card" id="home">

<h2>Welcome</h2>

<p>20-day structured AI training program</p>

<button onclick="start()">Start Course</button>

</div>

<div class="card">

<h3>Progress</h3>

<p id="progressText">0% Complete</p>

<div class="progress"><div id="bar"></div></div>

</div>

<div class="card" id="lessonBox" style="display:none;">

<h2 id="title"></h2>

<div id="video"></div>

<p id="content"></p>

<div id="quiz"></div>

<button onclick="next()">Next Lesson</button>

</div>

<script>

let day = parseInt(localStorage.getItem("day")) || 0;

let scoreNeeded = 80;

let progress = parseInt(localStorage.getItem("progress")) || 0;

const lessons = [

{

title: "Day 1 - What is AI?",

video: "https://www.youtube.com/embed/2ePf9rue1Ao",

content: "AI is software that learns patterns from data.",

quiz: [

{q:"What is AI?",a:["A system that learns","A robot only","A calculator"],correct:0},

{q:"Can AI make mistakes?",a:["Yes","No"],correct:0}

]

},

{

title: "Day 2 - What is ChatGPT?",

video: "https://www.youtube.com/embed/JTxsNm9IdYU",

content: "ChatGPT is a large language model that predicts text.",

quiz: [

{q:"What is ChatGPT?",a:["AI text generator","A robot","A search engine"],correct:0},

{q:"Does it understand like humans?",a:["Not exactly","Yes fully"],correct:0}

]

}

];

let score = 0;

function start() {

document.getElementById("home").style.display="none";

document.getElementById("lessonBox").style.display="block";

load();

}

function load() {

let l = lessons[day];

document.getElementById("title").innerText = l.title;

document.getElementById("content").innerText = l.content;

document.getElementById("video").innerHTML =

`<iframe src="${l.video}" allowfullscreen></iframe>`;

let html = "<h3>Quiz</h3>";

l.quiz.forEach((q,i)=>{

html += `<p>${q.q}</p>`;

q.a.forEach((ans,j)=>{

html += `<button onclick="answer(${i},${j})">${ans}</button>`;

});

});

document.getElementById("quiz").innerHTML = html;

score = 0;

}

function answer(qi, ai) {

let q = lessons[day].quiz[qi];

if(ai === q.correct) score += 50;

alert("Answer recorded");

}

function next() {

if(score >= scoreNeeded) {

day++;

progress += 10;

save();

update();

load();

alert("Lesson unlocked!");

} else {

alert("You need 80% to continue");

}

}

function update() {

document.getElementById("progressText").innerText = progress + "% Complete";

document.getElementById("bar").style.width = progress + "%";

}

function save() {

localStorage.setItem("day",day);

localStorage.setItem("progress",progress);

}

update();

</script>

</body>

</html>