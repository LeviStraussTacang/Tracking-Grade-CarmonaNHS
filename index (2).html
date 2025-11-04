<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Carmona Study Tracker</title>

<style>
  * {
    box-sizing: border-box;
    font-family: "Poppins", sans-serif;
  }
  body {
    margin: 0;
    background: linear-gradient(120deg, #5c258d, #4389a2);
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
  }
  .container {
    width: 90%;
    max-width: 900px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 15px;
    padding: 30px;
    box-shadow: 0 0 20px rgba(0,0,0,0.3);
    animation: fadeIn 1s ease;
  }

  @keyframes fadeIn {
    from {opacity: 0; transform: translateY(20px);}
    to {opacity: 1; transform: translateY(0);}
  }

  h1, h2 {
    text-align: center;
    margin-bottom: 20px;
  }

  input, select, button {
    padding: 10px;
    border: none;
    border-radius: 5px;
    margin: 5px;
  }

  button {
    background-color: #4caf50;
    color: white;
    cursor: pointer;
    transition: 0.3s;
  }
  button:hover { background-color: #45a049; }

  table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
  }
  th, td {
    padding: 10px;
    text-align: center;
    border-bottom: 1px solid rgba(255,255,255,0.3);
  }

  .hidden { display: none; }

  /* Achievement colors */
  .Failed { background: red; }
  .Completers { background: #cd7f32; } /* bronze */
  .Warriors { background: #cd7f32; } /* bronze + bird */
  .Platinum { background: linear-gradient(45deg, #e5e4e2, #bcc6cc); color: black; }
  .Elite { background: silver; color: black; }
  .Epic { background: linear-gradient(45deg, #00a86b, #7fff00); }
  .Legend { background: gold; color: black; }
  .Masters { background: royalblue; }
  .Mythical { background: linear-gradient(45deg, gold, purple); }

  .achievement-card {
    margin: 15px 0;
    padding: 15px;
    border-radius: 10px;
    text-align: center;
    color: white;
    animation: pop 0.5s ease;
  }

  @keyframes pop {
    from {transform: scale(0.8); opacity: 0;}
    to {transform: scale(1); opacity: 1;}
  }

  .logout-btn {
    float: right;
    background: crimson;
  }

  .badge {
    font-size: 50px;
    margin-top: 10px;
  }

</style>
</head>
<body>

<div class="container" id="loginPage">
  <h1>Carmona Study Tracker</h1>
  <p style="text-align:center">Login to start tracking your achievements</p>
  <input type="text" id="name" placeholder="Your Name"><br>
  <select id="school">
    <option value="Carmona National High School">Carmona National High School</option>
  </select><br>
  <input type="number" id="gradeLevel" placeholder="Grade Level"><br>
  <select id="quarter">
    <option value="1st Quarter">1st Quarter</option>
    <option value="2nd Quarter">2nd Quarter</option>
    <option value="3rd Quarter">3rd Quarter</option>
    <option value="4th Quarter">4th Quarter</option>
  </select><br>
  <button onclick="login()">Login</button>
</div>

<div class="container hidden" id="dashboard">
  <button class="logout-btn" onclick="logout()">Logout</button>
  <h2 id="welcome"></h2>
  <table id="subjectTable">
    <tr><th>Subject</th><th>Grade</th><th>Achievement</th></tr>
  </table>
  <div id="averageDisplay"></div>
  <div id="achievementDisplay"></div>
</div>

<script>
const subjects = [
  "Values Education",
  "Mathematics",
  "Science",
  "English",
  "Filipino",
  "MAPEH",
  "Social Studies",
  "TLE"
];

function login() {
  const name = document.getElementById("name").value;
  const school = document.getElementById("school").value;
  const gradeLevel = document.getElementById("gradeLevel").value;
  const quarter = document.getElementById("quarter").value;
  if (!name || !gradeLevel) {
    alert("Please complete all fields!");
    return;
  }
  document.getElementById("loginPage").classList.add("hidden");
  document.getElementById("dashboard").classList.remove("hidden");
  document.getElementById("welcome").innerText = 
    `Welcome ${name} (${school}) - Grade ${gradeLevel} - ${quarter}`;
  loadSubjects();
}

function logout() {
  location.reload();
}

function loadSubjects() {
  const table = document.getElementById("subjectTable");
  subjects.forEach(sub => {
    const row = document.createElement("tr");
    row.innerHTML = `
      <td>${sub}</td>
      <td><input type="number" min="0" max="100" onchange="updateGrades()" class="grade-input"></td>
      <td class="achievement-cell">—</td>
    `;
    table.appendChild(row);
  });
}

function updateGrades() {
  const grades = document.querySelectorAll(".grade-input");
  let total = 0, count = 0;
  grades.forEach((input, idx) => {
    const grade = parseFloat(input.value);
    if (!isNaN(grade)) {
      count++;
      total += grade;
      const achievement = getAchievement(grade);
      const cell = input.parentElement.nextElementSibling;
      cell.innerText = achievement.name;
      cell.className = `achievement-cell ${achievement.class}`;
    }
  });
  if (count > 0) {
    const avg = (total / count).toFixed(2);
    document.getElementById("averageDisplay").innerHTML = `<h3>Average Grade: ${avg}</h3>`;
    const overall = getAchievement(avg);
    showAchievement(overall);
  }
}

function getAchievement(grade) {
  if (grade < 75) return {name: "Failed", class: "Failed", badge: "❌"};
  if (grade < 80) return {name: "Completers", class: "Completers", badge: "🥉"};
  if (grade < 83) return {name: "Warriors Student 🦅", class: "Warriors", badge: "🦅"};
  if (grade < 85) return {name: "Platinum Honor", class: "Platinum", badge: "💎"};
  if (grade < 87) return {name: "Elite Honor 🐏", class: "Elite", badge: "🐏"};
  if (grade < 90) return {name: "Epic Honor 🦏", class: "Epic", badge: "🦏"};
  if (grade < 94) return {name: "Legend Honor 🦁 (3)", class: "Legend", badge: "🦁"};
  if (grade < 98) return {name: "Masters Honor 🌟 (2)", class: "Masters", badge: "🌟"};
  return {name: "Mythical Honor 🐉 (1)", class: "Mythical", badge: "🐉"};
}

function showAchievement(achievement) {
  const div = document.getElementById("achievementDisplay");
  div.innerHTML = `
    <div class="achievement-card ${achievement.class}">
      <h2>${achievement.name}</h2>
      <div class="badge">${achievement.badge}</div>
    </div>
  `;
}
</script>

</body>
</html>
