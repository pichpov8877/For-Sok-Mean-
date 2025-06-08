<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Do You Love Me?</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 50px;
      background-color: #ffeef0;
    }
    h1 {
      font-size: 2em;
      color: #e91e63;
    }
    .buttons {
      margin-top: 30px;
      position: relative;
    }
    button {
      font-size: 1.2em;
      padding: 10px 20px;
      margin: 10px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }
    #yesBtn {
      background-color: #4caf50;
      color: white;
    }
    #noBtn {
      background-color: #f44336;
      color: white;
      position: absolute;
    }
    #response {
      margin-top: 30px;
      font-size: 1.5em;
      color: #4caf50;
    }
  </style>
</head>
<body>
  <h1>Do You Love Me?</h1>
  <div class="buttons">
    <button id="yesBtn">Yes ❤️</button>
    <button id="noBtn">No 😬</button>
  </div>
  <div id="response"></div>

  <script>
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');
    const response = document.getElementById('response');

    yesBtn.addEventListener('click', () => {
      response.textContent = "I knew it! 😍";
    });

    function moveButton() {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight - 100);
      noBtn.style.left = x + 'px';
      noBtn.style.top = y + 'px';
    }

    // Move on hover or touch
    noBtn.addEventListener('mouseover', moveButton);
    noBtn.addEventListener('touchstart', (e) => {
      e.preventDefault();
      moveButton();
    });
  </script>
</body>
</html>
