<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Page title</title>
</head>
<body>
    
</body>
</html>DOCTYPE html>
<html lang="en">
<head>.<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Page title</title>
</head>
<body>
    l
</body>
</html>
  <meta charset="UTF-8">
  <title>snax Calculator</title>  
  <style> 
    body {
      background-color: black;999
      font-family: 'Courier New', monospace;p <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <title>Page title</title>
      </head>
      <body>
          r e 
      </body>
      </html>
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .neon-text {
      font-size: 40px;
      color: #00ff00;
      text-shadow:
        0 0 5px #00ff00,
        0 0 10px #00ff00,
        0 0 20px #00ff00,
        0 0 40px #00ff00,
        0 0 80px #00ff00;
      animation: flicker 1.5s infinite alternate;
      margin-bottom: 30px;
    }

    @keyframes flicker {
      from { opacity: 1; }
      to { opacity: 0.85; }
    }

    .calculator {
      background: rgba(0, 255, 0, 0.05);
      border: 2px solid #00ff00;
      border-radius: 20px;
      box-shadow: 0 0 20px #00ff00;
      padding: 20px;
      width: 300px;
    }

    .display {
      background: black;
      color: #00ff00;
      font-size: 2em;
      border: none;
      text-align: right;
      padding: 15px;
      width: 100%;
      margin-bottom: 20px;
      box-shadow: 0 0 10px #00ff00 inset;
      border-radius: 10px;
    }

    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
    }

    button {
      background: black;
      border: 2px solid #00ff00;
      color: #00ff00;
      font-size: 1.3em;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 0 10px #00ff00;
      cursor: pointer;
      transition: 0.2s;
    }

    button:hover {
      background: #00ff00;
      color: black;
    }
  </style>
</head>
<body>
  <div class="neon-text">░A░L░O░K░</div>

  <div class="calculator">
    <input type="text" class="display" id="display" disabled>
    <div class="buttons">
      <button onclick="clearDisplay()">C</button>
      <button onclick="appendValue('(')">(</button>
      <button onclick="appendValue(')')">)</button>
      <button onclick="appendValue('%')">%</button>
      
      <button onclick="appendValue('+')">+</button>
      <button onclick="appendValue('7')">7</button>
      <button onclick="appendValue('8')">8</button>
      <button onclick="appendValue('9')">9</button>

      <button onclick="appendValue('-')">−</button>
      <button onclick="appendValue('4')">4</button>
      <button onclick="appendValue('5')">5</button>
      <button onclick="appendValue('6')">6</button>

      <button onclick="appendValue('×')">×</button>
      <button onclick="appendValue('1')">1</button>
      <button onclick="appendValue('2')">2</button>
      <button onclick="appendValue('3')">3</button>

      <button onclick="appendValue('/')">÷</button>
      <button onclick="appendValue('0')">0</button>
      <button onclick="appendValue('.')">.</button>
      <button onclick="calculate()">=</button>


      <button onclick="backspace()" style="grid-column: span 1;">⌫ Backspace</button>
    </div>
  </div>

  <script>
    const display = document.getElementById('display');

    function appendValue(value) {
      display.value += value;
    }

    function clearDisplay() {
      display.value = '0';
    }

    function backspace() {
      display.value = display.value.slice(0, -1);
    }

    function calculate() {
      try {
        // Replace × and ÷ with * and / for evaluation
        const result = display.value.replace(/×/g, '*').replace(/÷/g, '/');
        display.value = eval(result);
      } catch {
        display.value = 'अनपढ़ हो क्या';
      }
    }
  </script>
</body>
</html>

