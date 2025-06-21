<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>StakeVault | Elite Crypto Staking</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(145deg, #000000, #1c1c1c);
      color: gold;
      overflow-x: hidden;
    }
    .hero {
      text-align: center;
      padding: 100px 20px;
      background-image: url('https://images.unsplash.com/photo-1607301962677-2081f3466a32');
      background-size: cover;
      background-position: center;
      background-blend-mode: overlay;
      background-color: rgba(0, 0, 0, 0.6);
    }
    .hero h1 {
      font-size: 3.5rem;
      text-shadow: 0 0 10px gold;
    }
    .hero p {
      font-size: 1.3rem;
      color: #ddd;
    }
    .btn {
      background: gold;
      color: black;
      border: none;
      padding: 15px 30px;
      font-size: 1.1rem;
      border-radius: 10px;
      cursor: pointer;
      margin-top: 20px;
      transition: background 0.3s;
    }
    .btn:hover {
      background: #f5c518;
    }
    .staking {
      padding: 60px 20px;
      max-width: 800px;
      margin: auto;
      background: #111;
      border-radius: 16px;
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.3);
    }
    .staking h2 {
      text-align: center;
      margin-bottom: 20px;
    }
    input, select {
      width: 100%;
      padding: 15px;
      margin-bottom: 20px;
      border: none;
      border-radius: 10px;
      font-size: 1rem;
    }
    .footer {
      text-align: center;
      padding: 30px;
      font-size: 0.9rem;
      background: #000;
      color: #777;
    }
    audio {
      display: none;
    }
  </style>
</head>
<body>
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
  </audio>  <div class="hero">
    <h1>✨ StakeVault</h1>
    <p>Earn passive income with elegance. The future of luxury crypto investing starts here.</p>
    <button class="btn" onclick="document.getElementById('stake-section').scrollIntoView({ behavior: 'smooth' })">Start Staking</button>
  </div>  <div id="stake-section" class="staking">
    <h2>Stake Your Crypto</h2>
    <select id="coin">
      <option value="BNB">BNB</option>
      <option value="ETH">Ethereum (ETH)</option>
      <option value="USDT">Tether (USDT)</option>
    </select>
    <input type="number" id="amount" placeholder="Enter amount to stake" />
    <input type="number" id="days" placeholder="Staking duration (days)" />
    <button class="btn" onclick="calculateProfit()">Calculate Profit</button>
    <p id="result"></p>
  </div>  <div class="footer">
    &copy; 2025 StakeVault. All rights reserved.
  </div>  <script>
    function calculateProfit() {
      const coin = document.getElementById('coin').value;
      const amount = parseFloat(document.getElementById('amount').value);
      const days = parseInt(document.getElementById('days').value);
      if (isNaN(amount) || isNaN(days)) {
        document.getElementById('result').innerText = 'Please enter valid numbers.';
        return;
      }
      const rate = coin === 'BNB' ? 0.12 : coin === 'ETH' ? 0.10 : 0.08;
      const profit = amount * rate * (days / 365);
      document.getElementById('result').innerText = `Estimated profit: ${profit.toFixed(2)} ${coin}`;
    }
  </script></body>
</html>
