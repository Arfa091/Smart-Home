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

    header {
      text-align: center;
      padding: 40px 20px;
      background: linear-gradient(135deg, #1e293b, #0f172a);
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    .container {
      padding: 20px;
      max-width: 900px;
      margin: auto;
    }

    .card {
      background: #1e293b;
      padding: 20px;
      margin: 15px 0;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }

    button {
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 10px;
      font-weight: bold;
    }

    .on {
      background: #22c55e;
      color: white;
    }

    .off {
      background: #ef4444;
      color: white;
    }

    footer {
      text-align: center;
      padding: 20px;
      opacity: 0.6;
    }

    img {
      width: 100%;
      border-radius: 12px;
      margin-top: 10px;
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
    <img src="tungtung-tungtung-sahur.gif" alt="Smart Home GIF">
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
