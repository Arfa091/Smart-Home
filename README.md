<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Smart Home Beginner</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0f172a;
      color: #e2e8f0;
    }

  
  </style>
</head>
<body>

<header>
  <h1>🏠 Smart Home Beginner</h1>
  <p>Control your home like the future is already here</p>
</header>

<div class="container">

  <div class="card">
    <h2>💡 Smart Light</h2>
    <p>Status: <span id="lightStatus">OFF</span></p>
    <button class="on" onclick="turnOnLight()">Turn ON</button>
    <button class="off" onclick="turnOffLight()">Turn OFF</button>
  </div>

  <div class="card">
    <h2>🔐 Smart Door (RFID Simulation)</h2>
    <p id="doorStatus">Door is Locked</p>
    <button onclick="scanRFID()">Tap RFID Card</button>
  </div>

  <div class="card">
    <h2>📡 How It Works</h2>
    <p>This is a simple simulation of a smart home system using JavaScript. In real life, this would connect to hardware like Arduino or ESP32.</p>
    <img src="https://media.giphy.com/media/3o7aD2saalBwwftBIY/giphy.gif" alt="Smart Home">
  </div>

</div>

<footer>
  <p>Made for learning Smart Home 🚀</p>
</footer>

<script>
  function turnOnLight() {
    document.getElementById("lightStatus").innerText = "ON";
  }

  function turnOffLight() {
    document.getElementById("lightStatus").innerText = "OFF";
  }

  function scanRFID() {
    const valid = Math.random() > 0.5;
    if (valid) {
      document.getElementById("doorStatus").innerText = "Door Unlocked ✅";
    } else {
      document.getElementById("doorStatus").innerText = "Access Denied ❌";
    }
  }
</script>

</body>
</html>
