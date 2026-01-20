<h2>Login</h2>

<form action="/login" method="POST">
  <input type="text" name="username" placeholder="Username" required><br><br>
  <input type="password" name="password" placeholder="Password" required><br><br>
  <button type="submit">Login</button>
</form>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Website - Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
  <h1>My Website</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
  </nav>
</header>

<main>
  <h2>Welcome</h2>
  <p>This is the home page of my medium-level website.</p>

  <button onclick="showMessage()">Click Me</button>
  <p id="message"></p>
</main>

<footer>
  <p>© 2026 My Website</p>
</footer>

<script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>About Us</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
  <h1>About Us</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
  </nav>
</header>

<main>
  <h2>Who We Are</h2>
  <p>
    This website is built using HTML, CSS, and JavaScript.
    It is a complete beginner-to-medium project.
  </p>
</ý
  <p>
    You can upgrade this later with a backend and database.
  </p>
</main>

<footer>
  <p>© 2026 My Website</p>
</footer>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contact</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
  <h1>Contact Us</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>03288832899
  </nav>
</header>

<main>
  <h2>Contact Form</h2>

  <input type="text" placeholder="Raja Nadir Ali"><br><br>
  <input type="email" placeholder="rajanadirali4@gmail.com"><br><br>
  <textarea placeholder="Your Message"></textarea><br><br>

  <button onclick="sendMessage()">Send</button>
</main>

<footer>
  <p>© 2026 My Website</p>
</footer>

<script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background: #f2f2f2;
}

header {
  background: #333;
  color: white;
  padding: 15px;
}

nav a {
  color: white;
  margin-right: 15px;
  text-decoration: none;
}

main {
  padding: 20px;
  background: white;
  margin: 20px;
  border-radius: 5px;
}

input, textarea {
  width: 100%;
  padding: 8px;
}

button {
  padding: 10px 15px;
  cursor: pointer;
}

footer {
  text-align: center;
  background: #222;
  color: white;
  padding: 10px;
}
function showMessage() {
  document.getElementById("message").innerText =
    "You clicked the button!";
}

function sendMessage() {
  alert("Message sent successfully!");
}
const express = require("express");
const bodyParser = require("body-parser");

const app = express();
const PORT = 3000;

// Middleware
app.use(bodyParser.urlencoded({ extended: true }));
app.use(express.static("public"));

// Fake user data (for learning)
const user = {
  username: "admin",
  password: "1234"
};

// Login API
app.post("/login", (req, res) => {
  const { username, password } = req.body;

  if (username === user.username && password === user.password) {
    res.send("Login successful");
  } else {
    res.send("Invalid credentials");
  }
});

// Start server
app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}`);
});
node server.js
