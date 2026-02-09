<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <title>Valentine?</title>  
  <style>  
    body {  
      height: 100vh;  
      overflow: hidden;  
      display: flex;  
      flex-direction: column;  
      justify-content: center;  
      align-items: center;  
      font-family: Arial, sans-serif;  
      background: #ffe6f0;  
      text-align: center;  
    }  
  
    h1 {  
      font-size: 40px;  
      color: #ff4d88;  
    }  
  
    .aca {  
      display: inline-block;  
      animation: wiggle 0.8s infinite;  
      font-weight: bold;  
      color: #ff1a66;  
    }  
  
    @keyframes wiggle {  
      0% { transform: rotate(-8deg); }  
      50% { transform: rotate(8deg); }  
      100% { transform: rotate(-8deg); }  
    }  
  
    #buttons {  
      margin-top: 30px;  
      position: relative;  
      width: 300px;  
      height: 200px;  
    }  
  
    button {  
      padding: 15px 35px;  
      font-size: 18px;  
      border: none;  
      border-radius: 12px;  
      cursor: pointer;  
      position: absolute;  
    }  
  
    #yes {  
      background-color: #ff4d88;  
      color: white;  
      left: 20px;  
      top: 80px;  
    }  
  
    #no {  
      background-color: #cccccc;  
      left: 160px;  
      top: 80px;  
    }  
  
    .sure {  
      position: absolute;  
      color: #ff1a66;  
      font-size: 18px;  
      animation: fade 2s forwards;  
      pointer-events: none;  
    }  
  
    @keyframes fade {  
      from { opacity: 1; }  
      to { opacity: 0; }  
    }  
  </style>  
</head>  
<body>  
  
  <h1>  
    will u be my valentine   
    <span class="aca">aca?</span>  
  </h1>  
  
  <div id="buttons">  
    <button id="yes" onclick="yesClick()">Yes</button>  
    <button id="no" onmouseover="runAway()">No</button>  
  </div>  
  
  <script>  
    function runAway() {  
      const noBtn = document.getElementById("no");  
      const x = Math.random() * (window.innerWidth - 120);  
      const y = Math.random() * (window.innerHeight - 120);  
  
      noBtn.style.left = x + "px";  
      noBtn.style.top = y + "px";  
  
      createSureText();  
    }  
  
    function createSureText() {  
      const sure = document.createElement("div");  
      sure.className = "sure";  
      sure.innerText = "are u sure?";  
  
      sure.style.left = Math.random() * window.innerWidth + "px";  
      sure.style.top = Math.random() * window.innerHeight + "px";  
  
      document.body.appendChild(sure);  
  
      setTimeout(() => {  
        sure.remove();  
      }, 2000);  
    }  
  
    function yesClick() {  
      document.body.innerHTML = `  
        <h1>YAY 💖💖💖</h1>  
        <p>best valentine ever 😘</p>  
      `;  
    }  
  </script>  
  
</body>  
</html>  
