<head>
  <meta charset="UTF-8">
  <title>Lesson Plan Generator</title>
  <link rel="stylesheet" href="style.css">
</head>
  <meta charset="UTF-8">
  <title>Lesson Plan Generator</title>
</head>
<body>
  <h1>Lesson Plan Generator</h1>

  <form id="lessonForm">
    <label for="class">Class Level:</label><br>
    <input type="text" id="class" name="class"><br><br>

    <label for="subject">Subject:</label><br>
    <input type="text" id="subject" name="subject"><br><br>

    <label for="week">Week:</label><br>
    <input type="text" id="week" name="week"><br><br>

    <label for="objectives">Objectives:</label><br>
    <textarea id="objectives" name="objectives" rows="4" cols="50"></textarea><br><br>

    <label for="activities">Teaching Activities:</label><br>
    <textarea id="activities" name="activities" rows="4" cols="50"></textarea><br><br>

    <button type="submit">Generate Plan</button>
  </form>

</body>
</html># General-Elia-Eros-
General lesson plan for All teachers
// script.js
document.getElementById("lessonForm").addEventListener("submit", function (e) {
  e.preventDefault();

  const classLevel = document.getElementById("class").value;
  const subject = document.getElementById("subject").value;
  const week = document.getElementById("week").value;
  const objectives = document.getElementById("objectives").value;
  const activities = document.getElementById("activities").value;

  const output = `
    <h2>Lesson Plan Preview</h2>
    <p><strong>Class:</strong> ${classLevel}</p>
    <p><strong>Subject:</strong> ${subject}</p>
    <p><strong>Week:</strong> ${week}</p>
    <p><strong>Objectives:</strong><br> ${objectives}</p>
    <p><strong>Teaching Activities:</strong><br> ${activities}</p>
  `;

  document.getElementById("result").innerHTML = output;
});
body {
  font-family: Arial, sans-serif;
  background-color: #f7f7f7;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 700px;
  margin: auto;
  background: white;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  margin-top: 40px;
  border-radius: 8px;
}

h1 {
  text-align: center;
  color: #333;
}

label {
  display: block;
  margin-bottom: 10px;
  font-weight: bold;
}

input[type="text"],
textarea {
  width: 100%;
  padding: 10px;
  margin-top: 4px;
  margin-bottom: 15px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  background-color: #0275d8;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #025aa5;
}

#result {
  background: #f1f1f1;
  padding: 15px;
  border-radius: 6px;
  margin-top: 20px;
}
