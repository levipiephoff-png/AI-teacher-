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

  border: none;

  border-radius: 8px;

  background: #38bdf8;

  font-weight: bold;

  cursor: pointer;

  margin: 5px;

}

.lesson {

  display: none;

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

</style>

</head>

<body>

<header>

  <h1>AI Mastery Academy</h1>

  <p>Beginner → Intermediate AI Course</p>

</header>

<div class="card" id="home">

  <h2>Welcome</h2>

  <p>20 days to learn AI step-by-step</p>

  <button onclick="startCourse()">Start Learning</button>

</div>

<div class="card">

  <h3>Progress</h3>

  <p id="progressText">0% Complete</p>

  <div class="progress"><div id="bar"></div></div>

</div>

<!-- LESSON VIEW -->

<div class="card lesson" id="lessonBox">

  <h2 id="lessonTitle"></h2>

  <p id="lessonContent"></p>

  <button onclick="nextLesson()">Next Lesson</button>

  <div id="quizBox" style="margin-top:15px;"></div>

</div>

<script>

let current = parseInt(localStorage.getItem("day")) || 0;

let progress = parseInt(localStorage.getItem("progress")) || 0;

const lessons = Array.from({length: 20}, (_, i) => ({

  title: `Day ${i+1}`,

  content: `This is lesson ${i+1}. We will expand this with videos, AI prompts, and exercises later.`

}));

function startCourse() {

  document.getElementById("home").style.display = "none";

  document.getElementById("lessonBox").style.display = "block";

  loadLesson();

}

function loadLesson() {

  let lesson = lessons[current];

  document.getElementById("lessonTitle").innerText = lesson.title;

  document.getElementById("lessonContent").innerText = lesson.content;

  document.getElementById("quizBox").innerHTML = `

    <h4>Quick Quiz</h4>

    <p>What is AI?</p>

    <button onclick="answer(true)">A system that learns</button>

    <button onclick="answer(false)">Just robots</button>

  `;

}

function answer(correct) {

  if(correct) {

    alert("Correct! +5% progress");

    progress += 5;

  } else {

    alert("Not quite — AI is broader than robots.");

  }

  updateProgress();

}

function nextLesson() {

  if(current < 19) {

    current++;

    progress += 5;

    save();

    loadLesson();

    updateProgress();

  } else {

    alert("You completed the course!");

  }

}

function updateProgress() {

  document.getElementById("progressText").innerText = progress + "% Complete";

  document.getElementById("bar").style.width = progress + "%";

}

function save() {

  localStorage.setItem("day", current);

  localStorage.setItem("progress", progress);

}

updateProgress();

</script>

</body>

</html>