# AI-teacher-
<!DOCTYPE html>

<html lang="en">

<head>

  <meta charset="UTF-8">

  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>AI Mastery Academy</title>

  <style>

    body {

      font-family: Arial;

      margin: 0;

      background: #0f172a;

      color: white;

      text-align: center;

    }

    header {

      padding: 20px;

      background: #1e293b;

    }

    .card {

      background: #1e293b;

      margin: 20px;

      padding: 20px;

      border-radius: 12px;

    }

    button {

      padding: 12px 20px;

      border: none;

      border-radius: 8px;

      background: #38bdf8;

      font-weight: bold;

    }

    .progress {

      width: 100%;

      background: #334155;

      height: 20px;

      border-radius: 10px;

      overflow: hidden;

      margin-top: 10px;

    }

    #bar {

      width: 0%;

      height: 100%;

      background: #22c55e;

      transition: 0.3s;

    }

  </style>

</head>

<body>

<header>

  <h1>AI Mastery Academy</h1>

  <p>20-Day AI Learning Journey (Beginner → Intermediate)</p>

</header>

<div class="card">

  <h2>Welcome</h2>

  <p>Learn AI step-by-step with quizzes, fun challenges, and real skills.</p>

  <button onclick="start()">Start Course</button>

</div>

<div class="card">

  <h2>Progress</h2>

  <p id="text">0% Complete</p>

  <div class="progress">

    <div id="bar"></div>

  </div>

</div>

<script>

  let progress = 0;

  function start() {

    progress = 5;

    update();

    alert("Course started! Next we’ll build lessons and quizzes.");

  }

  function update() {

    document.getElementById("text").innerText = progress + "% Complete";

    document.getElementById("bar").style.width = progress + "%";

  }

</script>

</body>

</html>